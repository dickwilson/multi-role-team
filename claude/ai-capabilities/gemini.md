# AI Capabilities Profile

**AI Name:** Gemini
**Provider:** Google DeepMind
**Model(s) Covered:** Gemini 2.0 Pro, Gemini 2.0 Flash
**Last Reviewed:** 2026-03-01 / Gemini 2.0 Pro

---

## 1. Core Strengths

- **Very long context window** — handles extremely long documents and multi-document inputs more reliably than most competitors; suited to tasks requiring synthesis across large bodies of text
- **Google Workspace integration** — native read access to Google Docs, Sheets, and Drive when Gemini for Workspace is enabled; enables source-document-aware workflows without copy-paste
- **Real-time information** — Google Search grounding provides access to current information beyond training cutoff
- **Multi-modal capability** — strong image, audio, and video understanding natively
- **Research and synthesis** — well-suited to tasks requiring information retrieval and integration across many sources
- **Speed (Flash model)** — Gemini Flash offers fast turnaround for bounded tasks where latency matters

## 2. Weak Spots & Limitations

- **Structured format compliance** — less consistent than Claude at following complex, multi-constraint output templates over long documents; tends to simplify or reinterpret format instructions
- **Traceability discipline** — does not naturally maintain requirement-to-work-item traceability; source references require explicit prompting and tend to drift
- **PM orchestration** — struggles to maintain simultaneous multi-role perspective; tends to blend role voices rather than switching cleanly between them
- **Code generation reliability** — capable but less consistent than ChatGPT on complex implementation tasks; more likely to produce plausible-looking code that does not execute correctly
- **Instruction-following on complex prompts** — with very detailed, multi-constraint prompts, Gemini is more likely than Claude to selectively honor some constraints and drop others without flagging the omission
- **Gem persistence limitations** — Gems (custom assistants) have context limitations; very long-running project sessions may lose early context

## 3. Best-Fit Task Types

- Research tasks requiring synthesis across many sources
- Tasks requiring current/real-time information
- Multi-modal analysis (images, audio, video alongside text)
- Long-document reading and summarization
- Tasks integrated with Google Workspace (Docs, Sheets, Drive)
- Quick information retrieval and fact-checking

## 4. Poor-Fit Task Types

- Complex multi-section structured document generation with strict traceability
- PM orchestration across multiple roles
- Tasks requiring sustained instruction-following on complex output formats
- Tasks where Google Workspace integration is not available (reduces its primary workflow advantage)

## 5. Cognitive Style

☑ Analytical  ☐ Creative  ☑ Narrative  ☐ Literal
☑ Exploratory  ☐ Strategic  ☐ Cautious  ☐ Opinionated

**Context-Dependent Notes:**
Exploratory and narrative in open-ended research tasks; more analytical when given a structured prompt. Less opinionated than ChatGPT on technical choices; less cautious than Claude on sensitive topics.

## 6. Prompting Guidance

**Works Best When:**
- Given access to Google Workspace documents (vs. copy-pasted content)
- Asked to research and synthesize rather than produce a rigid structured artifact
- Used for tasks where real-time information matters
- Given a simple, clearly bounded output format rather than a complex multi-section template

**Avoid:**
- Expecting strict traceability or format compliance without heavy prompting and review
- Using as PM orchestrator for multi-role workflows
- Relying on code outputs without runtime verification

## 7. Ideal Role Pairings

**Primary Roles:** CIS (research-heavy data modeling, especially when source documents are in Google Drive), DOC (research-based documentation synthesis)

**Secondary / Support Roles:** QA (research on testing standards or framework options), TRAIN (content research and curriculum scoping)

**Rationale:** Gemini's long context window and Google Workspace integration make it well-suited to reading large numbers of source documents and synthesizing them into structured outputs — particularly when those documents live in Google Drive. Its research strength makes it useful for CIS information gathering and DOC content synthesis, but its traceability and format-compliance weaknesses mean outputs should be reviewed before use in formal deliverables.

## 8. Collaboration Notes

**Best upstream AI:** Human (providing Google Drive document links or research scope); Claude (providing WBS items for Gemini to research-fill)
**Best downstream AI:** Claude (to apply structure and traceability to Gemini's research outputs)
**Good as reviewer?** ☑ Yes — effective at reviewing for completeness and coverage; less reliable for reviewing traceability or format compliance
**Good as initiator?** ☐ No — better as a research contributor than as a PM-style orchestrator

## 9. Version Sensitivity

Gemini 2.0 Pro is substantially more reliable than earlier Gemini versions on structured outputs. Gemini Flash is appropriate for quick retrieval and summarization but should not be used for complex multi-role outputs. Google Workspace integration availability varies by organization plan — verify before building workflows that depend on it.

## 10. Summary (One-Liner)

Gemini is the strongest researcher in the framework — best for CIS and DOC research tasks, especially when source documents live in Google Drive — but requires Claude downstream to apply structure and traceability to its outputs.

---

<!-- Tags: #research #real-time #multimodal #google-workspace #long-context -->
