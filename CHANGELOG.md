# Changelog

All notable changes to the Multi-Role Professional Team Framework are documented here.

## [1.0.0] — March 2026

### Initial Release

**Framework design:**
- PM-orchestrated, multi-role agentic workflow covering 7 professional roles
- Open-ended document intake — handles any number of source documents on any topics
- Document Registry as the backbone of all traceability
- PM methodology recommendation (Agile, Waterfall, SAFe, Kanban, Hybrid) based on project characteristics
- Work Breakdown Structure (WBS) organized by role with full traceability to source requirements
- Role-specific detailed breakdowns with step-by-step sub-tasks
- Cascading change management with formal Impact Registers and Revision History
- Session debrief feedback loop (✅ Worked well / 🔼 Do more of / 🔽 Do less of / 🔧 Could improve / ❌ Total failure)

**The 7 roles defined:**
- PM — Project Manager (orchestrator)
- CIS — Computer Information Scientist (Data & Information Architect)
- DEV — Software Developer
- QA — Software Tester
- AUTO — Automation Specialist (test automation + workflow automation)
- DOC — Documentation Writer (technical audiences)
- TRAIN — Technical Trainer (technical audiences)

**Outputs:**
- Markdown plan document
- Excel tracker (5 sheets: Document Registry, Work Items, Traceability Matrix, Effort Summary, Change Log)

**Package contents:**
- `claude/multi-role-team.skill` — Claude-native installable skill
- `universal/multi-role-team-universal-prompt.md` — Platform-agnostic system prompt
- `docs/multi-role-team-adaptation-guide.docx` — Setup guide for OpenAI, Microsoft, and Google platforms
- `LICENSE.md` — CC BY 4.0
- `feedback/feedback-log.md` — Running feedback log

**License:** Creative Commons CC BY 4.0
**Author:** Richard (Dick) Wilson
