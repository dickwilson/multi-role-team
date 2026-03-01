# Multi-Role Professional Team Framework

**A PM-orchestrated, multi-role AI framework for technology product development.**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

---

## What This Is

The Multi-Role Professional Team framework transforms an AI assistant into a coordinated team of seven professional roles, working together under Project Manager orchestration. It was designed for technology product development projects where:

- Multiple teams work from multiple source documents
- Requirements evolve and specs get revised mid-project
- Every piece of work needs to trace back to a documented requirement
- Change impacts need to cascade transparently across all roles

**Primary platform:** This framework is designed and recommended for use with **[Claude](https://claude.ai) (Anthropic)**. The `.skill` file in the `claude/` folder installs directly into Claude. For situations where other platforms are in use, see the [Universal Prompt](#other-platforms) section below.

---

## The Seven Roles

| Role | Abbrev. | Primary Responsibility |
|---|---|---|
| Project Manager | PM | Orchestrates the process, recommends methodology, owns the WBS |
| Computer Information Scientist | CIS | Data & information architecture — models, flows, data dictionary |
| Software Developer | DEV | Code design, implementation, API development, integration |
| Software Tester | QA | Test planning, test cases, acceptance criteria, defect tracking |
| Automation Specialist | AUTO | Test automation and workflow/process automation |
| Documentation Writer | DOC | Technical reference material for technical audiences |
| Technical Trainer | TRAIN | Instructional content and curriculum for technical audiences |

---

## How It Works

1. **PM reads** any number of source documents (Marketing Requirements, Software Specs, Hardware Specs, Regulatory Docs, etc.) and builds a **Document Registry**
2. **PM recommends** a methodology (Agile, Waterfall, SAFe, Kanban, or Hybrid) based on the project
3. **PM produces** a **Work Breakdown Structure (WBS)** organized by role, with priorities, estimates, and traceability
4. **Each role expands** its own work items into detailed, sequential sub-tasks
5. **Every work item** traces to its source document and section — full auditability
6. **When requirements change**, cascading impact analysis identifies all directly and indirectly affected work items across all roles

**Outputs:** A Markdown plan document + an Excel tracker (Document Registry, Work Items, Traceability Matrix, Effort Summary, Change Log)

---

## Quick Start — Claude

1. Download `claude/multi-role-team.skill`
2. Double-click to install in Claude (Cowork or Claude Code)
3. Start a conversation — the framework activates automatically when you describe a project, ask for a work breakdown, mention a spec change, or ask how a PM would approach something

**Example prompts to get started:**
- *"We're starting a new product called XYZ. Here are the requirements: [paste]. As PM, build a Document Registry and WBS with full traceability."*
- *"The Software Spec was updated from v1.0 to v2.0. Section 4.2 changed from X to Y. Process this change and show all cascading impacts."*
- *"As QA, create a test plan for these requirements: [paste]. Trace every test case to its source."*

---

## Other Platforms

The framework is portable. The `universal/multi-role-team-universal-prompt.md` file contains the complete framework as a plain-text system prompt — copy and paste it into any AI assistant that accepts custom instructions.

The `docs/multi-role-team-adaptation-guide.docx` provides step-by-step setup instructions for:
- **OpenAI** — Custom GPT (ChatGPT)
- **Microsoft** — Copilot Studio (with SharePoint integration)
- **Google** — Gemini Gem

---

## Feedback & Improvement

This framework is designed to improve with real-world use. After each project engagement, the built-in session debrief prompts for structured feedback:

- ✅ Worked well
- 🔼 Do more of
- 🔽 Do less of
- 🔧 Could improve
- ❌ Total failure

Feedback is logged in `feedback/feedback-log.md` and drives the next revision cycle. See [CHANGELOG.md](CHANGELOG.md) for version history.

---

## Repository Contents

```
multi-role-team/
├── README.md
├── LICENSE.md                              CC BY 4.0
├── CHANGELOG.md                            Version history
├── claude/
│   └── multi-role-team.skill              Claude-native installable skill
├── universal/
│   └── multi-role-team-universal-prompt.md  Platform-agnostic system prompt
├── docs/
│   └── multi-role-team-adaptation-guide.docx  Setup guide for other platforms
└── feedback/
    └── feedback-log.md                    Running real-world feedback log
```

---

## License & Attribution

**[Creative Commons CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)** — Free to use, share, and adapt with attribution.

**Conceived and developed by Richard (Dick) Wilson**
- 📧 [wilson.richard.d@icloud.com](mailto:wilson.richard.d@icloud.com)
- 💼 [linkedin.com/in/wilsonrichard](https://www.linkedin.com/in/wilsonrichard)
- 🐙 [github.com/dickwilson](https://github.com/dickwilson)

Developed in collaboration with Claude (Anthropic), March 2026.

**To attribute this work:**
> *Multi-Role Professional Team Framework by Richard (Dick) Wilson (github.com/dickwilson/multi-role-team), licensed under CC BY 4.0.*
