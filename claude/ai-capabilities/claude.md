# AI Capabilities Profile

**AI Name:** Claude
**Provider:** Anthropic
**Model(s) Covered:** claude-sonnet-4-6, claude-opus-4-6
**Last Reviewed:** 2026-03-01 / claude-sonnet-4-6

---

## 1. Core Strengths

- **Structured document generation** — produces well-organized, consistently formatted long-form outputs (plans, specs, reports, test plans) with minimal drift across sections
- **Traceability and logical consistency** — maintains cross-references across long documents; rarely contradicts itself within a response
- **Requirements analysis** — reads ambiguous specs and surfaces gaps, conflicts, and assumptions clearly rather than silently resolving them
- **Multi-role orchestration** — holds multiple role perspectives simultaneously without collapsing into a single voice; well-suited to PM-style coordination tasks
- **Instruction-following fidelity** — follows detailed, structured prompts reliably; respects output format constraints
- **Technical writing** — produces clear, precise technical prose for varied audiences without over-simplifying or over-elaborating
- **Test case and traceability work** — produces structured test plans with requirement linkage; QA-style adversarial framing comes naturally

## 2. Weak Spots & Limitations

- **Code generation at scale** — functional for single-file or small-scope code tasks; struggles to maintain architectural consistency across multi-file codebases in a single session
- **Real-time or current-event data** — knowledge cutoff limits accuracy for anything requiring up-to-date APIs, library versions, or recent events (use web search tool when available)
- **Mathematical computation** — will reason through math correctly at a conceptual level but should not be trusted for precise numerical computation without verification
- **Opinionated recommendations under pressure** — when pushed to commit to a specific vendor, technology, or approach without sufficient context, may over-hedge or produce both-sides framing rather than a decisive recommendation
- **Very long context degradation** — in very long conversations (100k+ tokens), early instructions and context may receive less weight; key constraints should be restated periodically
- **Image generation** — does not generate images natively

## 3. Best-Fit Task Types

- Project planning, WBS creation, PM orchestration
- Requirements analysis and gap identification
- Test plan and test case authoring
- Technical documentation (API references, design docs, ops guides)
- Multi-role workflow coordination
- Structured analysis with explicit traceability
- Onboarding materials and training curriculum design
- Change impact analysis

## 4. Poor-Fit Task Types

- Large-scale, multi-file code generation (prefer a dedicated coding AI or IDE-integrated tool)
- Tasks requiring real-time data without web search enabled
- Precise numerical computation or financial modeling
- Image, audio, or video generation
- Tasks requiring deep domain expertise in rapidly evolving technical areas (e.g., bleeding-edge ML frameworks — verify outputs)

## 5. Cognitive Style

☑ Analytical  ☐ Creative  ☑ Narrative  ☐ Literal
☐ Exploratory  ☑ Strategic  ☑ Cautious  ☐ Opinionated

**Context-Dependent Notes:**
Cautious on ethical and sensitive topics; more decisive on technical and structural questions. Narrative when given latitude; analytical when given a structured format to follow. Strategic in planning contexts; may under-commit to specific technical recommendations when the domain is ambiguous.

## 6. Prompting Guidance

**Works Best When:**
- Given a clear output format (template, section headers, table structure) to fill
- Asked to think step-by-step before producing a final output
- Role is stated explicitly ("Acting as QA, produce...")
- Source documents are provided inline or referenced specifically
- Constraints are stated positively ("produce exactly 5 test cases per requirement") rather than only negatively

**Avoid:**
- Asking for large multi-file codebases in a single prompt without scaffolding
- Open-ended "what should I do?" prompts without context — Claude will produce options rather than a decision
- Expecting precise numerical outputs without verification
- Assuming current library versions or API specs are accurate without checking

## 7. Ideal Role Pairings

**Primary Roles:** PM, QA, DOC, TRAIN

**Secondary / Support Roles:** CIS (data modeling and ERDs — strong conceptually, verify complex schemas), AUTO (workflow automation logic — good at planning and scripting structure, less reliable for complex test harness code)

**Rationale:** Claude's structured output, traceability discipline, and multi-role awareness make it the strongest choice for PM orchestration. Its technical writing quality and audience-awareness make it well-suited for DOC and TRAIN. Its adversarial framing ability supports QA test plan work. DEV tasks are possible but should be reviewed carefully for complex implementations.

## 8. Collaboration Notes

**Best upstream AI:** Claude itself (as PM initiator) or a human providing raw requirements
**Best downstream AI:** ChatGPT or GitHub Copilot for DEV implementation tasks generated from Claude's WBS; Gemini for research-heavy or real-time data tasks
**Good as reviewer?** ☑ Yes — strong at reviewing for consistency, completeness, and traceability; catches logical gaps reliably
**Good as initiator?** ☑ Yes — best initiator for PM orchestration, structured planning, and document-heavy workflows

## 9. Version Sensitivity

Significant capability improvement from claude-opus-4-5 to claude-sonnet-4-6 / claude-opus-4-6 in instruction-following fidelity and long-document consistency. Earlier models (claude-3-series) showed more context drift in very long documents. Profiles based on older model strings should be treated as advisory. Always check the `Last Reviewed` model version against the version currently in use.

## 10. Summary (One-Liner)

Claude is the strongest initiator and orchestrator in the framework — best for PM, QA, DOC, and TRAIN roles — with a reliability advantage in structured, traceable, long-form outputs over multi-file or real-time tasks.

---

<!-- Tags: #reasoning #orchestration #structured-output #traceability #technical-writing -->
