# Personalized Sailing Tutor System - Architecture

## Executive Summary

This document outlines the architecture for a **personalized, adaptive sailing education platform** built on the existing 45-skill sailing-claude-plugins foundation. The system will track individual user competencies, identify strengths and weaknesses, and guide sailors through customized learning paths toward RYA/ASA YachtMaster certification.

**Key Features**:
- Individual user accounts with persistent competency profiles
- Skill-by-skill mastery tracking across all 14 navigation domains
- Adaptive difficulty and personalized learning paths
- Progress dashboard with readiness assessment
- Interactive quizzing with performance analytics
- Exam preparation and weak-area remediation

---

## System Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                   User Interface Layer                       │
│  (Claude Code CLI / Web Interface / Mobile App)              │
└─────────────────────────────────────────────────────────────┘
                              │
┌─────────────────────────────────────────────────────────────┐
│              Personalized Tutor Orchestrator                 │
│  - User session management                                   │
│  - Skill invocation and context management                   │
│  - Competency tracking engine                                │
│  - Adaptive learning path generator                          │
└─────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┴─────────────────────┐
        │                                             │
┌───────▼──────────┐                   ┌─────────────▼────────┐
│  User Profile DB  │                   │  Skill Library       │
│  - User accounts  │                   │  - 45+ skills        │
│  - Competencies   │                   │  - 14 tutor agents   │
│  - History        │                   │  - Test scenarios    │
│  - Preferences    │                   │  - Resources         │
└──────────────────┘                   └──────────────────────┘
```

---

## 1. User Profile & Account System

### 1.1 User Data Model

```yaml
user_profile:
  user_id: "uuid-v4"
  personal_info:
    name: "Jonathan Smith"
    email: "jon@example.com"
    target_cert: "RYA YachtMaster Offshore"
    experience_level: "intermediate"  # beginner | intermediate | advanced
    start_date: "2025-11-10"
    target_exam_date: "2026-06-01"

  competency_profile:
    overall_readiness: 67  # percentage (0-100)
    plugin_scores:
      - plugin_id: "01-chart-basics"
        mastery_level: 85
        skills_mastered: 15
        skills_total: 17
      - plugin_id: "02-tides"
        mastery_level: 72
        skills_mastered: 6
        skills_total: 8
      # ... all 14 plugins

    skill_competencies:
      - skill_id: "datum-guardian"
        plugin_id: "01-chart-basics"
        mastery_level: 95  # 0-100
        attempts: 12
        successful_attempts: 11
        last_practiced: "2025-11-09T14:30:00Z"
        time_spent_minutes: 45
        difficulty_rating: "easy"  # easy | medium | hard | mastered
        notes: "Strong on WGS-84, needs review on ED-50 edge cases"
      # ... all 45+ skills

  learning_history:
    sessions:
      - session_id: "uuid"
        date: "2025-11-09T14:00:00Z"
        duration_minutes: 60
        skills_practiced: ["datum-guardian", "tide-calculator"]
        quiz_scores:
          - skill_id: "datum-guardian"
            score: 8
            total: 10
        notes: "Good session, struggled with ED-50 examples"

    quiz_performance:
      total_quizzes_taken: 147
      average_score: 78.5
      improvement_trend: +12  # percentage points over last month

    weak_areas:
      - skill_id: "tidal-curve-graphical-analysis"
        reason: "3 failed attempts, low confidence"
        recommended_review: true
      - skill_id: "velocity-triangle-plotter"
        reason: "Last practiced 3 weeks ago"
        recommended_review: false

  preferences:
    learning_style: "visual"  # visual | procedural | conceptual
    session_length_minutes: 30
    difficulty_preference: "adaptive"  # easy | adaptive | challenging
    quiz_frequency: "high"  # low | medium | high
    notifications_enabled: true
```

### 1.2 Authentication & Authorization

- **Account Creation**: Email/password or OAuth (GitHub, Google)
- **Role-Based Access**:
  - `student`: Access own profile, skills, progress tracking
  - `instructor`: Access multiple student profiles, assign exercises
  - `admin`: System management, skill authoring
- **Data Privacy**: User data encrypted at rest, GDPR/CCPA compliant

---

## 2. Competency Tracking Engine

### 2.1 Skill Mastery Calculation

Each skill has a **mastery level (0-100)** calculated from:

```python
def calculate_mastery(skill_history):
    """
    Calculate skill mastery from user interaction history.
    """
    # Factors (weighted):
    success_rate = (successful_attempts / total_attempts) * 40  # 40%
    recency_bonus = calculate_recency_decay(last_practiced)    # 20%
    time_spent = normalize_time_investment(total_minutes)      # 15%
    quiz_performance = average_quiz_score * 0.25               # 25%

    mastery = success_rate + recency_bonus + time_spent + quiz_performance
    return min(100, max(0, mastery))

def calculate_recency_decay(last_practiced_date):
    """
    Skills decay over time without practice.
    """
    days_since = (today - last_practiced_date).days
    if days_since < 7:
        return 20  # Full recency bonus
    elif days_since < 30:
        return 15  # Slight decay
    elif days_since < 90:
        return 10  # Moderate decay
    else:
        return 5   # Significant decay - needs review
```

### 2.2 Competency Levels

| Mastery Score | Level | Description | Action |
|---------------|-------|-------------|--------|
| 0-25 | Novice | Little to no exposure | Introduce fundamentals |
| 26-50 | Learning | Basic understanding, many errors | Guided practice |
| 51-75 | Competent | Reliable with guidance | Independent practice |
| 76-90 | Proficient | Confident and accurate | Challenging scenarios |
| 91-100 | Mastered | Expert-level performance | Maintain with review |

### 2.3 Prerequisite Tracking

Skills have dependencies that must be satisfied:

```yaml
skill_dependencies:
  ep-calculator:
    requires:
      - visual-fix-calculator  # must be at 60%+ mastery
      - tidal-diamond-reader   # must be at 60%+ mastery
      - compass-error-corrector # must be at 60%+ mastery
    recommended:
      - leeway-applicator
      - time-zone-converter

  cts-calculator:
    requires:
      - velocity-triangle-plotter
      - magnetic-variation-calculator
      - tidal-diamond-reader
    recommended:
      - ep-calculator
```

**Locking Mechanism**:
- Skills with unmet prerequisites are **locked** until dependencies reach 60%+ mastery
- Users see lock icon with explanation: "Master visual-fix-calculator first (currently 45%)"
- Recommended skills are unlocked but system suggests completing dependencies first

---

## 3. Adaptive Learning System

### 3.1 Personalized Learning Paths

The system generates custom learning paths based on:

1. **User Goals**: Target certification and exam date
2. **Current Competencies**: Existing mastery across all skills
3. **Weak Areas**: Skills below 60% mastery
4. **Time Constraints**: Available study hours per week
5. **Learning Style**: Visual vs procedural vs conceptual

**Example Learning Path**:

```yaml
learning_path_generated:
  user_id: "uuid"
  goal: "RYA YachtMaster Offshore"
  exam_date: "2026-06-01"
  weeks_remaining: 29
  estimated_hours_needed: 87

  phases:
    - phase: "Foundation (Weeks 1-8)"
      focus: "Chart basics and tidal fundamentals"
      skills_to_master:
        - datum-guardian
        - charted-height-interpreter
        - tide-calculator
        - depth-datum-flipper
        - magnetic-variation-calculator
        - compass-error-corrector
      weekly_hours: 4
      success_criteria: "All skills at 75%+ mastery"

    - phase: "Core Navigation (Weeks 9-16)"
      focus: "Position fixing and course calculations"
      skills_to_master:
        - visual-fix-calculator
        - ep-calculator
        - cts-calculator
        - velocity-triangle-plotter
        - cross-track-error-monitor
      weekly_hours: 4
      success_criteria: "All skills at 80%+ mastery"

    - phase: "Advanced Techniques (Weeks 17-24)"
      focus: "Pilotage and passage planning"
      skills_to_master:
        - clearing-bearing-calculator
        - harbor-entry-planner
        - restricted-visibility-navigator
        - almanac-navigator
      weekly_hours: 3
      success_criteria: "All skills at 80%+ mastery"

    - phase: "Exam Preparation (Weeks 25-29)"
      focus: "Weak area remediation and mock exams"
      activities:
        - review_weak_skills: true
        - mock_exams: 4
        - timed_scenarios: 12
      weekly_hours: 5
      success_criteria: "90%+ overall readiness"
```

### 3.2 Dynamic Difficulty Adjustment

The system adapts question difficulty based on performance:

```python
def adjust_difficulty(user, skill):
    """
    Dynamically adjust scenario difficulty for optimal learning.
    """
    mastery = user.get_skill_mastery(skill)
    recent_performance = user.get_recent_quiz_average(skill, last_n=5)

    # Zone of Proximal Development targeting
    if recent_performance > 85 and mastery > 75:
        return "challenging"  # Push the user
    elif recent_performance < 60 or mastery < 50:
        return "easy"  # Build confidence
    else:
        return "medium"  # Optimal learning zone

    # Example difficulty levels:
    # Easy: "Simple 3-bearing fix, 90° apart, calm conditions"
    # Medium: "4-bearing fix, 45° apart, tidal stream, moderate visibility"
    # Challenging: "Running fix in fog, single object, strong cross-tide, time pressure"
```

### 3.3 Spaced Repetition Algorithm

Skills are scheduled for review using spaced repetition:

```python
def calculate_next_review_date(skill, mastery_level, last_practiced):
    """
    Calculate optimal review date based on Ebbinghaus forgetting curve.
    """
    # Base interval increases with mastery
    if mastery_level >= 90:
        base_interval_days = 30  # Mastered skills: monthly review
    elif mastery_level >= 75:
        base_interval_days = 14  # Proficient: bi-weekly
    elif mastery_level >= 60:
        base_interval_days = 7   # Competent: weekly
    else:
        base_interval_days = 3   # Learning: every 3 days

    next_review = last_practiced + timedelta(days=base_interval_days)
    return next_review
```

---

## 4. Progress Dashboard & Analytics

### 4.1 Dashboard Components

**Main Dashboard View**:

```
╔══════════════════════════════════════════════════════════════╗
║  🎓 Jonathan's YachtMaster Journey                          ║
║  Target Exam: June 1, 2026 (29 weeks remaining)             ║
╠══════════════════════════════════════════════════════════════╣
║  Overall Readiness: 67% ████████████░░░░░░░░                ║
║  Skills Mastered: 32 / 45                                    ║
║  Current Streak: 12 days 🔥                                  ║
║  Total Study Time: 47 hours                                  ║
╠══════════════════════════════════════════════════════════════╣
║  📊 Plugin Mastery Breakdown                                 ║
║  ✅ 01. Chart Basics        85% ████████████████░░          ║
║  ✅ 02. Tides               72% ██████████████░░░░          ║
║  ⚠️  03. Positioning         58% ███████████░░░░░░          ║
║  ⚠️  04. Course to Steer     54% ██████████░░░░░░░          ║
║  📚 08. Visual Aids         88% █████████████████░          ║
║  ... (more plugins)                                          ║
╠══════════════════════════════════════════════════════════════╣
║  🎯 Today's Focus                                            ║
║  • Practice: visual-fix-reliability (15 min)                ║
║  • Review: tidal-curve-graphical-analysis (weak area)       ║
║  • Quiz: 5 questions on positioning                          ║
╠══════════════════════════════════════════════════════════════╣
║  ⚠️  Weak Areas (needs attention)                            ║
║  • velocity-triangle-plotter (45% mastery, 3 failed)        ║
║  • secondary-port-calculations (not practiced in 21 days)   ║
║  • restricted-visibility-navigator (52% on last quiz)       ║
╠══════════════════════════════════════════════════════════════╣
║  📈 Progress Chart (Last 30 Days)                            ║
║  100│                                              ░░        ║
║   75│                              ░░░░░░░░░░░░░░░░          ║
║   50│              ░░░░░░░░░░░░░░░░                          ║
║   25│  ░░░░░░░░░░░░                                          ║
║    0│───────────────────────────────────────────────────    ║
║      Oct 10        Oct 25         Nov 10                     ║
║                                                               ║
║  Trend: +15% improvement over last month 📈                  ║
╚══════════════════════════════════════════════════════════════╝
```

### 4.2 Detailed Skill View

When user clicks on a specific skill:

```
╔══════════════════════════════════════════════════════════════╗
║  📍 SKILL: visual-fix-reliability                           ║
║  Plugin: 03-positioning                                      ║
╠══════════════════════════════════════════════════════════════╣
║  Mastery Level: 58% ███████████░░░░░░░░ (Competent)         ║
║  Status: ⚠️ Needs Practice                                   ║
║                                                               ║
║  Performance Metrics:                                        ║
║  • Attempts: 8 (6 successful, 2 failed)                     ║
║  • Success Rate: 75%                                         ║
║  • Average Quiz Score: 6.5 / 10                             ║
║  • Time Spent: 32 minutes                                    ║
║  • Last Practiced: 4 days ago                                ║
║  • Next Review Due: In 3 days                                ║
║                                                               ║
║  Recent Attempts:                                            ║
║  Nov 06: ✅ 8/10 - Good cocked hat assessment               ║
║  Nov 05: ❌ 4/10 - Struggled with bearing spread angles     ║
║  Nov 03: ✅ 7/10 - Improved time pressure scenarios         ║
║                                                               ║
║  Weaknesses Identified:                                      ║
║  • Bearing spread geometry (30-150° acceptable range)       ║
║  • Time pressure scenarios (>3 min between bearings)        ║
║                                                               ║
║  Recommended Actions:                                        ║
║  1. Review bearing geometry fundamentals                     ║
║  2. Practice 5 timed scenarios (2 min limit)                ║
║  3. Take focused quiz on spread angles                       ║
║                                                               ║
║  [Start Practice Session]  [Take Quiz]  [Review Theory]     ║
╚══════════════════════════════════════════════════════════════╝
```

### 4.3 Analytics & Insights

**Weekly Summary Email**:

```
Subject: Your Weekly Sailing Progress - 12 hours practiced! 🎓

Hi Jonathan,

Great week! Here's your progress summary:

📊 This Week's Stats:
• Study Time: 12 hours (↑3 from last week)
• Skills Practiced: 8
• Quiz Scores: 82% average (↑5%)
• New Skills Unlocked: 2

🎯 Achievements:
✅ Mastered "magnetic-variation-calculator" (95%)
✅ 7-day learning streak completed
✅ Positioning plugin reached 60% mastery

⚠️ Areas Needing Attention:
• velocity-triangle-plotter: Dropped to 45% (review recommended)
• Haven't practiced tides this week (consider 20-min session)

📅 Next Week's Suggested Focus:
1. Course to Steer deep dive (3 sessions, 4 hours)
2. Review velocity triangles (weak area)
3. Take mock positioning exam

🎓 Exam Readiness: 67% (↑2% from last week)
   On track for June 2026 exam!

Keep up the excellent work!
Your Sailing Tutor
```

---

## 5. Interactive Quiz & Assessment System

### 5.1 Quiz Types

1. **Skill-Specific Quizzes**: 5-10 questions focused on single skill
2. **Plugin Comprehensive**: 20 questions across entire plugin
3. **Mock Exams**: 50-question RYA/ASA style exam simulation
4. **Weak Area Remediation**: Adaptive quiz targeting user's low-scoring topics
5. **Rapid-Fire Flashcards**: Quick recall for terminology and symbols

### 5.2 Question Bank Structure

```yaml
question:
  question_id: "uuid"
  skill_id: "visual-fix-calculator"
  plugin_id: "03-positioning"
  difficulty: "medium"
  type: "multiple_choice"  # or calculation | scenario | true_false

  prompt: |
    You take three bearings in quick succession:
    - Lighthouse A: 045°C
    - Buoy B: 110°C
    - Church spire C: 160°C

    Compass deviation: 2°W
    Variation: 5°E

    The resulting cocked hat triangle has sides of 150m, 200m, and 180m.
    What is the quality rating of this fix?

  options:
    A: "EXCELLENT - suitable for critical navigation"
    B: "GOOD - acceptable for general navigation"
    C: "ACCEPTABLE - use with caution"
    D: "POOR - fix unreliable, seek better bearings"

  correct_answer: "B"

  explanation: |
    Cocked hat assessment:
    - Size: 150-200m (within 0.5 NM acceptable range) ✅
    - Bearing spread: 045-110-160 = 65° and 50° (suboptimal but workable) ⚠️
    - Time: Quick succession assumed <2 min ✅

    Rating: GOOD
    - Small cocked hat indicates good precision
    - Bearing spread not ideal (prefer 60-90° apart)
    - Suitable for general navigation, but not critical pilotage

  references:
    - skill: "visual-fix-reliability"
      section: "Quality Criteria"
    - resource: "cocked-hat-assessment-guide.md"

  tags: ["cocked-hat", "fix-quality", "bearing-geometry"]
  author: "ZenterFlow"
  last_updated: "2025-11-10"
```

### 5.3 Adaptive Quiz Engine

```python
def generate_adaptive_quiz(user, focus_area=None):
    """
    Generate personalized quiz based on user competency profile.
    """
    if focus_area:
        # Focused quiz on specific plugin or skill
        questions = select_questions(focus_area, difficulty=user.level)
    else:
        # Adaptive quiz covering weak areas
        weak_skills = user.get_skills_below_mastery(threshold=70)
        questions = []

        for skill in weak_skills[:5]:  # Top 5 weak areas
            # Select 2-3 questions per weak skill
            q = question_bank.filter(skill_id=skill.id,
                                     difficulty=user.calculate_optimal_difficulty(skill))
            questions.extend(random.sample(q, min(3, len(q))))

    # Ensure variety of question types
    questions = balance_question_types(questions)

    # Add some mastered skills for confidence building (20% of quiz)
    mastered = user.get_skills_above_mastery(threshold=85)
    confidence_questions = sample_questions_from_skills(mastered, count=int(len(questions) * 0.2))

    questions.extend(confidence_questions)
    random.shuffle(questions)

    return Quiz(questions=questions, user=user, adaptive=True)
```

### 5.4 Quiz Results & Feedback

After quiz completion:

```
╔══════════════════════════════════════════════════════════════╗
║  📝 Quiz Results: Positioning Fundamentals                   ║
╠══════════════════════════════════════════════════════════════╣
║  Score: 7 / 10 (70%) ⚠️                                      ║
║  Time: 18 minutes                                            ║
║  Difficulty: Medium                                          ║
╠══════════════════════════════════════════════════════════════╣
║  ✅ Correct Answers (7)                                      ║
║  Q1: Visual fix bearing spread - Correct                     ║
║  Q2: Cocked hat assessment - Correct                         ║
║  Q4: Running fix advancement - Correct                       ║
║  ... (7 total)                                               ║
║                                                               ║
║  ❌ Incorrect Answers (3)                                    ║
║  Q3: EP tidal vector application                             ║
║      Your answer: Applied tide BEFORE leeway                 ║
║      Correct: Apply leeway first, THEN tidal vector          ║
║      ➜ Review: ep-calculator skill, "Order of Operations"   ║
║                                                               ║
║  Q7: Circle of error calculation                             ║
║      Your answer: 5% of distance                             ║
║      Correct: 10% of accumulated distance                    ║
║      ➜ Review: "Circle of Error" section in EP skill        ║
║                                                               ║
║  Q9: Time pressure fix quality                               ║
║      Your answer: >5 min still acceptable                    ║
║      Correct: >3 min degrades fix reliability                ║
║      ➜ Practice: Timed visual fix scenarios                 ║
╠══════════════════════════════════════════════════════════════╣
║  📊 Competency Impact                                        ║
║  • visual-fix-reliability: 58% → 62% (+4%)                  ║
║  • ep-calculator: 71% → 68% (-3%) ⚠️                        ║
║                                                               ║
║  Recommendation: Review EP skill section on tidal vectors    ║
║  before practicing more EP scenarios.                        ║
║                                                               ║
║  [Review Mistakes]  [Retake Quiz]  [Practice EP Skill]      ║
╚══════════════════════════════════════════════════════════════╝
```

---

## 6. Technical Implementation

### 6.1 System Components

**Backend Stack**:

```yaml
architecture:
  api_layer:
    framework: "FastAPI (Python)"
    endpoints:
      - /api/v1/auth/*          # Authentication
      - /api/v1/users/*         # User profile management
      - /api/v1/skills/*        # Skill catalog
      - /api/v1/progress/*      # Competency tracking
      - /api/v1/quiz/*          # Quiz generation and results
      - /api/v1/learning-path/* # Adaptive path generation

  database:
    primary: "PostgreSQL"
    schema:
      - users (profiles, auth)
      - competencies (skill mastery tracking)
      - sessions (learning history)
      - quiz_results (performance data)
      - questions (quiz bank)
      - learning_paths (personalized paths)

  cache: "Redis"
    use_cases:
      - Session management
      - Frequently accessed competency data
      - Question bank caching

  agent_orchestration:
    framework: "LangChain / Claude SDK"
    components:
      - Tutor agent router (selects appropriate agent)
      - Context manager (maintains conversation state)
      - Skill invocation handler
      - Progress tracker integration

  analytics:
    tool: "Metabase / Superset"
    dashboards:
      - User progress overview
      - Weak area identification
      - Quiz performance trends
      - Engagement metrics
```

**Frontend Stack**:

```yaml
frontend:
  primary_interface: "Claude Code CLI"
    features:
      - Text-based interactive sessions
      - Progress dashboard (ASCII art)
      - Quiz interface
      - Skill practice mode

  web_interface: "Next.js + React"
    pages:
      - Dashboard (progress overview)
      - Skill browser (catalog with filters)
      - Quiz interface (interactive)
      - Learning path view
      - Analytics (charts and graphs)

  mobile_app: "React Native (future)"
    features:
      - On-the-go quizzing
      - Flashcard mode
      - Progress notifications
      - Offline skill reference
```

### 6.2 Data Flow Example: Quiz Session

```
User: "Take a quiz on positioning"
   │
   ▼
┌──────────────────────────────────┐
│  Tutor Orchestrator              │
│  - Fetch user competency profile │
│  - Identify weak positioning     │
│    skills (visual-fix: 58%)      │
└────────────┬─────────────────────┘
             │
             ▼
┌──────────────────────────────────┐
│  Adaptive Quiz Engine            │
│  - Select 10 questions:          │
│    • 6 from weak skills          │
│    • 2 from medium skills        │
│    • 2 from mastered (confidence)│
│  - Balance difficulty: 60% med   │
└────────────┬─────────────────────┘
             │
             ▼
┌──────────────────────────────────┐
│  Question Bank                   │
│  - Query questions matching:     │
│    skill_ids, difficulty         │
│  - Randomize, avoid repeats      │
└────────────┬─────────────────────┘
             │
             ▼
┌──────────────────────────────────┐
│  Quiz Presentation (CLI/Web)     │
│  - Display questions one-by-one  │
│  - Collect user answers          │
│  - Track time per question       │
└────────────┬─────────────────────┘
             │
             ▼
┌──────────────────────────────────┐
│  Results Processor               │
│  - Calculate score (7/10)        │
│  - Identify incorrect answers    │
│  - Generate feedback             │
└────────────┬─────────────────────┘
             │
             ▼
┌──────────────────────────────────┐
│  Competency Tracker              │
│  - Update skill mastery scores   │
│  - Record quiz performance       │
│  - Adjust learning path          │
│  - Trigger spaced repetition     │
└────────────┬─────────────────────┘
             │
             ▼
┌──────────────────────────────────┐
│  Results Display + Recommendations│
│  - Show score and breakdown      │
│  - Highlight weak areas          │
│  - Suggest next practice session │
└──────────────────────────────────┘
```

### 6.3 Integration with Existing Skill Framework

**Current Structure**:
```
01-chart-basics/
  skills/
    datum-guardian/
      SKILL.md
      manifest.json
      instructions.md
      tests/
        sample-prompts.md
      resources/
        datum-table.csv
```

**Extended Structure for Personalized System**:
```
01-chart-basics/
  skills/
    datum-guardian/
      SKILL.md
      manifest.json
      instructions.md

      # NEW: Competency tracking metadata
      competency.yml:
        difficulty_level: "medium"
        estimated_time_to_mastery_minutes: 60
        prerequisites: []
        recommended_before: ["charted-height-interpreter"]
        common_mistakes:
          - "Confusing WGS-84 with ED-50"
          - "Not checking datum compatibility"

      # NEW: Quiz questions
      questions/
        question_001.yml
        question_002.yml
        ... (10+ questions per skill)

      # NEW: Practice scenarios with difficulty levels
      scenarios/
        easy_01_simple_wgs84.md
        medium_01_ed50_shift.md
        hard_01_mixed_datum_passage.md

      tests/
        sample-prompts.md

      resources/
        datum-table.csv
```

---

## 7. Key Features Detail

### 7.1 Intelligent Skill Recommendations

**Algorithm**:

```python
def recommend_next_skills(user):
    """
    AI-powered recommendation of what to practice next.
    """
    # Factors considered:
    recommendations = []

    # 1. Weak areas below 70% mastery
    weak_skills = user.get_skills_below_mastery(70)
    for skill in weak_skills[:3]:
        recommendations.append({
            'skill': skill,
            'reason': f'Needs improvement ({skill.mastery}% mastery)',
            'priority': 'high',
            'estimated_time': calculate_time_to_mastery(skill, user)
        })

    # 2. Skills not practiced recently (>14 days)
    stale_skills = user.get_skills_not_practiced_since(days=14)
    for skill in stale_skills[:2]:
        recommendations.append({
            'skill': skill,
            'reason': f'Last practiced {days_ago(skill.last_practiced)} days ago',
            'priority': 'medium',
            'estimated_time': 20  # Quick review
        })

    # 3. Next logical skill in learning path
    learning_path = user.get_current_learning_path()
    next_skill = learning_path.get_next_unlocked_skill()
    if next_skill:
        recommendations.append({
            'skill': next_skill,
            'reason': 'Next in your learning path',
            'priority': 'medium',
            'estimated_time': next_skill.estimated_time
        })

    # 4. Quick wins (skills close to mastery, 70-85%)
    almost_mastered = user.get_skills_in_range(70, 85)
    for skill in almost_mastered[:1]:
        recommendations.append({
            'skill': skill,
            'reason': f'Close to mastery ({skill.mastery}%) - finish strong!',
            'priority': 'low',
            'estimated_time': 15
        })

    return sorted(recommendations, key=lambda x: priority_score(x))
```

### 7.2 Exam Readiness Calculator

```python
def calculate_exam_readiness(user, target_cert="RYA YachtMaster Offshore"):
    """
    Calculate user's readiness for target certification exam.
    """
    # Certification requirements mapping
    cert_requirements = {
        "RYA YachtMaster Offshore": {
            "required_plugins": [
                {"id": "01-chart-basics", "min_mastery": 80, "weight": 15},
                {"id": "02-tides", "min_mastery": 85, "weight": 20},
                {"id": "03-positioning", "min_mastery": 80, "weight": 15},
                {"id": "04-course-to-steer", "min_mastery": 85, "weight": 20},
                {"id": "09-pilotage", "min_mastery": 80, "weight": 15},
                {"id": "11-irpcs", "min_mastery": 75, "weight": 10},
                {"id": "12-safety", "min_mastery": 75, "weight": 5},
            ],
            "critical_skills": [
                "visual-fix-calculator",
                "ep-calculator",
                "cts-calculator",
                "tide-calculator",
                "clearing-bearing-calculator"
            ],
            "min_overall_score": 80
        }
    }

    requirements = cert_requirements[target_cert]

    # Calculate weighted score
    total_score = 0
    total_weight = 0
    gaps = []

    for req_plugin in requirements["required_plugins"]:
        user_mastery = user.get_plugin_mastery(req_plugin["id"])
        weight = req_plugin["weight"]

        total_score += user_mastery * weight
        total_weight += weight

        if user_mastery < req_plugin["min_mastery"]:
            gap = req_plugin["min_mastery"] - user_mastery
            gaps.append({
                "plugin": req_plugin["id"],
                "current": user_mastery,
                "required": req_plugin["min_mastery"],
                "gap": gap
            })

    weighted_average = total_score / total_weight if total_weight > 0 else 0

    # Check critical skills
    critical_gaps = []
    for skill_id in requirements["critical_skills"]:
        skill_mastery = user.get_skill_mastery(skill_id)
        if skill_mastery < 80:
            critical_gaps.append({
                "skill": skill_id,
                "mastery": skill_mastery,
                "required": 80
            })

    # Overall readiness
    readiness = {
        "overall_score": round(weighted_average, 1),
        "ready": weighted_average >= requirements["min_overall_score"] and len(critical_gaps) == 0,
        "confidence_level": calculate_confidence(weighted_average),
        "plugin_gaps": gaps,
        "critical_skill_gaps": critical_gaps,
        "estimated_study_hours_remaining": estimate_hours_needed(gaps, critical_gaps),
        "recommended_exam_date": suggest_exam_date(weighted_average, gaps)
    }

    return readiness
```

### 7.3 Social & Gamification Features

**Leaderboard** (optional, privacy-respecting):
```
╔══════════════════════════════════════════════════════════════╗
║  🏆 Weekly Leaderboard - November Week 2                    ║
╠══════════════════════════════════════════════════════════════╣
║  1. 🥇 SailorMike      92% readiness  |  15 hours this week ║
║  2. 🥈 NavMaster_99    89% readiness  |  12 hours           ║
║  3. 🥉 Jonathan (You)  67% readiness  |  12 hours           ║
║  4.    TidalTina       64% readiness  |  8 hours            ║
║  5.    ChartChampion   58% readiness  |  10 hours           ║
╠══════════════════════════════════════════════════════════════╣
║  Your Progress: +2 positions from last week! 📈             ║
║  Most Improved: +15% readiness gain                          ║
╚══════════════════════════════════════════════════════════════╝
```

**Achievements/Badges**:
- 🎓 **Chart Master**: 100% mastery in Chart Basics plugin
- 🌊 **Tide Whisperer**: Perfect score on tidal calculations quiz
- 🔥 **30-Day Streak**: Practiced every day for 30 days
- 📍 **Position Pro**: Mastered all positioning skills
- ⚓ **YachtMaster Ready**: 90%+ exam readiness achieved
- 🚀 **Quick Learner**: Mastered 5 skills in one week
- 📚 **Knowledge Sharer**: Helped 3 other students (if social features enabled)

---

## 8. Implementation Phases

### Phase 1: Foundation (Months 1-2)

**Goals**:
- Build core user profile and competency tracking system
- Integrate with existing 45 skills

**Deliverables**:
- User authentication and profile management
- PostgreSQL schema for competencies and history
- Competency tracking engine (mastery calculation)
- Basic dashboard showing skill mastery levels
- Quiz engine with 10 questions per skill (450 questions total)

**Success Metrics**:
- 10 beta users creating profiles
- Competency tracking working for all 45 skills
- Users complete 50+ quizzes in testing

---

### Phase 2: Adaptive Learning (Months 3-4)

**Goals**:
- Build adaptive quiz and learning path systems
- Implement spaced repetition

**Deliverables**:
- Adaptive quiz generator (difficulty adjustment)
- Learning path generation algorithm
- Spaced repetition scheduler
- Weak area identification and recommendations
- Enhanced dashboard with progress trends

**Success Metrics**:
- 80% of users follow generated learning paths
- Average quiz scores improve by 15% over 2 weeks
- Users report finding weak area recommendations helpful

---

### Phase 3: Exam Preparation (Months 5-6)

**Goals**:
- Build exam readiness features
- Create mock exam system

**Deliverables**:
- Exam readiness calculator
- Mock RYA/ASA exam simulator (50 questions, timed)
- Detailed results analysis
- Remediation recommendations
- Study plan generator for target exam date

**Success Metrics**:
- 5 users complete full mock exams
- Exam readiness scores correlate with actual exam results
- Users feel confident about exam preparation

---

### Phase 4: Social & Gamification (Months 7-8)

**Goals**:
- Add optional social and gamification features
- Build community engagement

**Deliverables**:
- Leaderboards (opt-in)
- Achievements and badges
- Weekly progress emails
- Study buddy matching
- Discussion forums per skill

**Success Metrics**:
- 40% of users opt into leaderboards
- 20% increase in weekly study time
- Active discussions on 50% of skills

---

### Phase 5: Mobile & Expansion (Months 9-12)

**Goals**:
- Launch mobile app
- Add remaining skeleton plugin skills
- Expand to ASA-specific content

**Deliverables**:
- React Native mobile app (iOS/Android)
- 20 additional skills implemented (Plugins 05-14)
- ASA certification paths
- Offline mode for skill reference
- Export progress reports (PDF)

**Success Metrics**:
- 1000+ mobile app downloads
- 70% of users access via mobile weekly
- 90% skill coverage across all 14 plugins

---

## 9. Success Metrics & KPIs

### User Engagement
- **Daily Active Users (DAU)**: Target 60% of user base
- **Session Length**: Average 30 minutes per session
- **Weekly Study Time**: Average 4 hours per user
- **Retention Rate**: 80% active after 30 days

### Learning Outcomes
- **Average Mastery Improvement**: +10% per month
- **Quiz Score Improvement**: +15% over first 4 weeks
- **Exam Pass Rate**: 90% of users at 85%+ readiness pass real exam
- **Time to Competency**: Average 6 months from 0% to 80% readiness

### Platform Health
- **Question Bank Size**: 1000+ questions (20+ per skill)
- **Quiz Completion Rate**: 85% of started quizzes completed
- **Weak Area Remediation**: 70% of flagged weak areas improved within 2 weeks
- **Learning Path Adherence**: 75% of users follow suggested path

---

## 10. Technical Considerations

### Security
- User data encrypted at rest and in transit
- Password hashing (bcrypt)
- Rate limiting on API endpoints
- GDPR/CCPA compliance (data export, deletion)

### Scalability
- Horizontal scaling via load balancers
- Database read replicas for quiz queries
- Redis caching for frequent lookups
- CDN for static resources

### Performance
- Target: <200ms API response times
- Dashboard loads in <2 seconds
- Quiz questions preloaded for smooth UX
- Background jobs for analytics processing

### Monitoring
- Error tracking (Sentry)
- Performance monitoring (DataDog)
- User analytics (Mixpanel)
- Uptime monitoring (PingDOM)

---

## 11. Future Enhancements

### AI-Powered Features
- **Personalized Explanations**: Claude generates custom explanations based on user's learning style
- **Voice Mode**: Voice-guided practice sessions for hands-free learning
- **Image Recognition**: Upload chart photos for instant scenario creation
- **Natural Language Practice**: Conversational practice instead of structured quizzes

### Advanced Analytics
- **Predictive Modeling**: Predict exam readiness date based on current trajectory
- **Cohort Analysis**: Compare performance with similar users
- **Learning Style Detection**: Automatically detect and adapt to user's learning style
- **Time Investment Optimization**: Suggest optimal study schedule based on retention curves

### Content Expansion
- **Video Tutorials**: Instructor-led videos for complex topics
- **Virtual Reality**: VR chart table practice
- **Live Instructor Sessions**: Optional 1-on-1 tutoring with certified instructors
- **Community-Contributed Questions**: Users submit quiz questions for review

---

## 12. Conclusion

This architecture provides a comprehensive foundation for building a **world-class personalized sailing education platform**. By combining:

1. **Existing 45-skill foundation** with proven pedagogical content
2. **Sophisticated competency tracking** that knows each user's strengths and weaknesses
3. **Adaptive learning paths** that optimize time to mastery
4. **Engaging quiz and assessment system** with immediate feedback
5. **Data-driven insights** to guide study sessions

...we can create a system that **dramatically improves YachtMaster exam pass rates** while providing an engaging, personalized learning experience.

**Next Steps for You (as the Guinea Pig)**:
1. Review this architecture and provide feedback
2. Help prioritize features for Phase 1 MVP
3. Participate in user testing as features are built
4. Track your own learning journey to validate competency tracking algorithms
5. Provide insights on what metrics actually predict exam success

**Key Questions to Answer**:
- Which dashboard metrics are most motivating for you?
- What would make you open the app/CLI daily?
- How do you prefer to receive feedback (immediate, weekly summary, etc.)?
- What's your ideal quiz length (5, 10, 20 questions)?
- Would you use social features (leaderboards, study buddies)?

Let's build this together! ⛵🎓

---

**Document Version**: 1.0
**Date**: 2025-11-10
**Author**: Claude Code (ZenterFlow)
**Status**: Architecture Proposal
