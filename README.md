# ⛵ Sailing Curriculum – Claude Plugin Marketplace

**One-command access to the full RYA/ASA navigation syllabus inside Claude Code.**

This plugin suite provides 14 specialized agents, turning your Claude Code environment into a comprehensive, interactive tutor for sailing navigation and theory.

---

## 🚀 Installation

Adding the entire curriculum to your Claude workspace is simple and requires just one command in the Code Interpreter environment:

```bash
/claude-code> /marketplace add https://github.com/ZenterFlow/sailing-claude-plugins
```

That's it! The 14 topic agents are now instantly available in every chat session.

## 📚 What You Get: The 14 Topic Agents

The curriculum is broken down into the following specialized agents, each covering a core area of the RYA/ASA syllabus:

| Agent Name | Covers |
| :--- | :--- |
| **`chart-basics`** | Chart datum, symbols, Mercator projection, compass errors |
| **`tides`** | Tide tables, curves, secondary ports, tidal diamonds, stream calculations |
| **`positioning`** | Estimated Position (EP), visual fixes, leeway, cross-track error |
| **`course-to-steer`** | Calculation of Course to Steer (CTS), incorporating leeway, worked examples |
| **`electronic-nav`** | GPS, radar, electronic instruments, navigation abbreviations |
| **`ec-plotting`** | Chart-plotter operation, electronic chart self-tests and validation |
| **`passage-making`** | Comprehensive planning, watch systems, monitoring and log-keeping |
| **`visual-aids`** | Buoys (IALA), lights, ranges, transits and leading lines |
| **`pilotage`** | Leading lines, clearing bearings, harbor entry plans, fog procedures |
| **`meteorology`** | Weather forecasts, cloud types, sea-breeze effects, synoptic charts |
| **`irpcs`** | International Regulations for Preventing Collisions at Sea (Rules, shapes, lights, collision cases) |
| **`safety-environment`** | Safety briefs, Mayday procedures, vessel stability, environmental regulations |
| **`collision-regs`** | Conduct in sight of other vessels and in restricted visibility |
| **`nav-lights-flip`** | A rapid-fire quiz agent focused on identifying navigation lights and shapes |

## 💡 Usage Examples

The agents are designed to auto-trigger when you ask a relevant question in plain English.

| Query | Agent Triggered |
| :--- | :--- |
| `>> how do I tie a bowline?` | *Safety-Environment (for general seamanship)* |
| `>> what is the tide at Wicklow on 15 Nov 2025 14:30?` | *Tides* |
| `>> show me a port-hand lateral buoy` | *Visual-Aids* |

## ⚠️ Status

🚧 **Early Beta**

The agents currently contain **skeleton prompts**; content and code are actively being developed and filled in.

**Star** or **watch** the repository to receive updates as each topic goes live and the curriculum becomes fully operational.

## 🤝 Contribute

We welcome contributions from the sailing community!

*   **Found a mistake** in the theory or code?
*   **Want an extra port** added to the tidal examples?

Please feel free to **open an issue** or submit a **Pull Request (PR)**. The structure is designed for easy collaboration: one plugin folder per topic.

## 📄 Licence

This project is licensed under the **MIT License**.

&copy; ZenterFlow
