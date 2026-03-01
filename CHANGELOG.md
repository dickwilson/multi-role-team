# Changelog

All notable changes to the Multi-Role Professional Team Framework are documented here.
---

## [1.1] — 2026-03-01

### Added

**`claude/roles/` directory** — Full reference files for all seven roles. Each file contains the complete role profile: how they think, inputs needed, what they produce, handoffs, and behavioral notes. Files:
- `roles/pm.md` — includes PM's AI delegation annotation behavior
- `roles/cis.md`
- `roles/developer.md`
- `roles/qa.md`
- `roles/automation.md`
- `roles/doc-writer.md`
- `roles/trainer.md`

**`claude/ai-capabilities/` directory** — Living AI capability profiles for multi-AI delegation decisions. Files:
- `_PROMPT.md` — standardized prompt to generate or refresh any profile; includes cross-validation note and honesty requirement
- `claude.md` — Anthropic Claude (claude-sonnet-4-6 / claude-opus-4-6)
- `chatgpt.md` — OpenAI ChatGPT (gpt-4o)
- `gemini.md` — Google Gemini (Gemini 2.0 Pro)
- `copilot.md` — Microsoft Copilot / Copilot Studio
- `grok.md` — xAI Grok (Grok-3)

**`docs/multi-role-team-adaptation-guide.docx`** — Platform adaptation guide for OpenAI Custom GPTs, Microsoft Copilot Studio, and Google Gems. Covers setup steps, file output approaches, feedback log management, and cross-platform portability notes.

**`CHANGELOG.md`** — This file. Version history going forward.

### Changed

- `claude/multi-role-team.skill` — version bumped to 1.1; `ai-capabilities/` reference updated to point to new directory structure; `Keeping Profiles Current` section updated to reference `_PROMPT.md`
- `README.md` — updated to document full v1.1 structure including `roles/` and `ai-capabilities/`
- `universal/multi-role-team-universal-prompt.md` — updated to v1.1; includes revision history header

### Notes

- Core PM orchestration logic, role definitions, traceability requirements, change management workflow, and output formats are unchanged from v1.0
- AI capability profiles are manually maintained — `Last Reviewed` field is the reliability indicator
- The Grok profile has the fewest real-world engagement data points; treat as more advisory than other profiles until feedback accumulates

---

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
