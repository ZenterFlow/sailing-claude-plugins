# Sailing Tutor Voice Application - Architecture

## Overview
Voice-enabled sailing education platform leveraging the 15 specialized Claude AI tutor agents for real-time guidance and instruction.

## System Components

### 1. Frontend Application (Mobile-First)
**Primary**: Progressive Web App (PWA) - Next.js 14 + TypeScript
**Future**: React Native (iOS/Android native apps)

**Mobile-First Design Principles**:
- Touch-optimized UI (large buttons, swipe gestures)
- Portrait and landscape orientations
- One-handed operation mode
- Dark mode for night sailing
- Minimal data usage (optimized API calls)
- Works on 3G/4G connections
- Battery-efficient (reduced animations)

**Features**:
- Voice interface (Web Speech API / native speech)
- Large push-to-talk button (easy to press while sailing)
- Real-time conversation display with large text
- Swipe gestures for navigation
- Quick-access emergency button
- Offline mode with syncing
- GPS location awareness
- Landscape mode for tablet use

**Voice Interface**:
- **Speech-to-Text**: Web Speech API (`SpeechRecognition`)
- **Text-to-Speech**: Web Speech API (`SpeechSynthesis`)
- Push-to-talk button for clarity in noisy marine environments
- Visual feedback during speech recognition
- Conversation transcript with timestamps

### 2. Backend API
**Technology**: Node.js + Express + TypeScript
**Database**: PostgreSQL (user data) + Redis (session cache)

**API Endpoints**:
```
POST   /api/auth/register        - Create user account
POST   /api/auth/login           - Authenticate user
POST   /api/auth/logout          - End session
GET    /api/auth/me              - Get current user

POST   /api/conversations        - Start new conversation
GET    /api/conversations        - List user conversations
GET    /api/conversations/:id    - Get conversation details
DELETE /api/conversations/:id    - Delete conversation

POST   /api/chat                 - Send message to tutor agent
POST   /api/chat/voice           - Stream voice response
GET    /api/agents               - List available agents
GET    /api/agents/:id/skills    - Get agent skills
```

### 3. Claude AI Integration
**API**: Anthropic Claude API (Messages API)
**Model**: Claude 3.5 Sonnet

**Agent Routing System**:
1. User question → Navigation Master (Plugin 00)
2. Master analyzes and routes to specialist agent(s)
3. Specialist responds with expertise
4. Multi-agent orchestration for complex queries

**Context Management**:
- Maintain conversation history (last 10 messages)
- Include user profile (experience level, certification goals)
- Agent-specific context from plugin skills
- Real-time data injection (weather, position if available)

### 4. Database Schema

**Users Table**:
```sql
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email VARCHAR(255) UNIQUE NOT NULL,
  password_hash VARCHAR(255) NOT NULL,
  full_name VARCHAR(255),
  experience_level VARCHAR(50), -- beginner, intermediate, advanced
  certification_goal VARCHAR(100), -- e.g., "YachtMaster Offshore"
  created_at TIMESTAMP DEFAULT NOW(),
  last_login TIMESTAMP
);
```

**Conversations Table**:
```sql
CREATE TABLE conversations (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  title VARCHAR(255),
  agent_id VARCHAR(100), -- plugin name (e.g., "navigation-master")
  started_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  metadata JSONB -- additional context, tags, location, etc.
);
```

**Messages Table**:
```sql
CREATE TABLE messages (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  conversation_id UUID REFERENCES conversations(id) ON DELETE CASCADE,
  role VARCHAR(20) NOT NULL, -- 'user' or 'assistant'
  content TEXT NOT NULL,
  voice_enabled BOOLEAN DEFAULT FALSE,
  timestamp TIMESTAMP DEFAULT NOW(),
  metadata JSONB -- agent used, response time, etc.
);
```

### 5. Voice Processing Pipeline

**User Speech → Response Flow**:
1. User presses "Talk" button
2. Browser captures audio via Web Speech API
3. Real-time transcription displayed
4. On speech end, send text to backend `/api/chat`
5. Backend routes to appropriate tutor agent via Claude API
6. Response streamed back to frontend
7. Text-to-speech converts response to audio
8. Audio plays with synchronized text highlighting

**Voice Settings**:
- Adjustable speech rate (0.5x - 2x)
- Voice selection (if multiple available)
- Auto-play responses vs manual trigger
- Background noise cancellation preferences

### 6. Real-Time Features

**On-Water Guidance** (Future Enhancement):
- GPS integration for position-based advice
- Weather API integration (wind, visibility, sea state)
- Real-time routing through agent with current conditions
- Emergency procedures with quick voice access
- Offline mode with cached essential skills

**Progressive Web App (PWA)**:
- Install as mobile app
- Offline access to conversation history
- Background sync when connection restored
- Push notifications for reminders/updates

## Security Considerations

**Authentication**:
- JWT tokens (15min access, 7day refresh)
- Secure password hashing (bcrypt)
- HTTPS only in production
- Rate limiting on API endpoints

**Data Privacy**:
- User conversations encrypted at rest
- Optional conversation deletion
- GDPR compliance (data export, right to deletion)
- No conversation data used for training without consent

## Deployment Architecture

**Development**:
- Frontend: `localhost:3000` (Next.js dev server)
- Backend: `localhost:8000` (Express)
- Database: Docker Compose (PostgreSQL + Redis)

**Production**:
- Frontend: Vercel (Next.js optimized)
- Backend: Railway/Fly.io (containerized Node.js)
- Database: Supabase (managed PostgreSQL) or Railway
- CDN: Cloudflare (static assets, API caching)
- Monitoring: Sentry (errors) + PostHog (analytics)

## Technology Stack Summary

| Layer | Technology | Purpose |
|-------|-----------|---------|
| Frontend | Next.js 14 + TypeScript | React framework with SSR |
| UI Library | Tailwind CSS + shadcn/ui | Styling and components |
| State | Zustand | Client state management |
| Voice | Web Speech API | Speech recognition & synthesis |
| Backend | Node.js + Express | REST API server |
| Database | PostgreSQL | User data & conversations |
| Cache | Redis | Session storage & rate limiting |
| AI | Claude API (Anthropic) | Tutor agent intelligence |
| Auth | JWT + bcrypt | Authentication & security |
| Deployment | Vercel + Railway | Hosting infrastructure |

## Development Phases

### Phase 1: MVP (Weeks 1-2)
- [ ] Basic authentication (register/login)
- [ ] Single-agent text chat interface
- [ ] Conversation history storage
- [ ] Claude API integration
- [ ] Deploy to staging

### Phase 2: Voice Interface (Weeks 3-4)
- [ ] Web Speech API integration
- [ ] Push-to-talk UI
- [ ] Text-to-speech responses
- [ ] Voice settings panel
- [ ] Mobile-responsive voice UI

### Phase 3: Multi-Agent System (Weeks 5-6)
- [ ] Navigation Master routing
- [ ] All 15 agents integrated
- [ ] Agent selector UI
- [ ] Multi-domain orchestration
- [ ] Skills browser

### Phase 4: Real-Time Features (Weeks 7-8)
- [ ] PWA conversion
- [ ] Offline mode
- [ ] GPS integration
- [ ] Weather API integration
- [ ] Emergency quick-access

### Phase 5: Polish & Launch (Weeks 9-10)
- [ ] User onboarding flow
- [ ] Progress tracking dashboard
- [ ] Performance optimization
- [ ] Security audit
- [ ] Production deployment

## API Integration with Tutor Agents

**Example: Routing through Navigation Master**

```typescript
// Backend: /api/chat endpoint
async function handleChat(userId: string, message: string) {
  // Load user context
  const user = await getUser(userId);
  const conversationHistory = await getRecentMessages(userId, 10);

  // Build Claude API request
  const response = await anthropic.messages.create({
    model: "claude-3-5-sonnet-20241022",
    max_tokens: 2048,
    system: `${loadAgentPrompt('navigation-master')}

User Profile:
- Experience: ${user.experience_level}
- Goal: ${user.certification_goal}`,
    messages: [
      ...conversationHistory.map(m => ({
        role: m.role,
        content: m.content
      })),
      { role: "user", content: message }
    ]
  });

  return response.content[0].text;
}
```

## Cost Estimation

**Claude API Costs** (Claude 3.5 Sonnet):
- Input: $3 per million tokens
- Output: $15 per million tokens
- Avg conversation: 2K input + 1K output = ~$0.02 per exchange
- 1000 users × 10 conversations/month × 20 exchanges = $4,000/month

**Infrastructure**:
- Vercel (Frontend): $20/month (Pro plan)
- Railway (Backend + DB): $20/month (Hobby plan)
- Total: ~$4,040/month for 1000 active users

**Revenue Model**:
- Free tier: 50 messages/month
- Pro: $9.99/month (unlimited messages)
- Team: $29.99/month (multi-user, progress tracking)

## Next Steps

1. Initialize Next.js frontend
2. Set up Express backend with TypeScript
3. Configure PostgreSQL database
4. Implement authentication flow
5. Create first agent integration (Navigation Master)
6. Build voice interface
7. Deploy MVP

---

**Version**: 1.0.0
**Last Updated**: 2025-11-10
**Status**: Architecture Design Complete
