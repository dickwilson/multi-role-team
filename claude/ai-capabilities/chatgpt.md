# AI Capabilities Profile

**AI Name:** ChatGPT
**Provider:** OpenAI
**Model(s) Covered:** gpt-4o, gpt-4o-mini
**Last Reviewed:** 2026-03-01 / gpt-4o

---

## 1. Core Strengths

- **Code generation** — produces functional, idiomatic code across a wide range of languages; strong at translating requirements into implementation, especially for common patterns and frameworks
- **Broad general knowledge** — wide training coverage makes it reliable for tasks that span multiple domains without deep specialization
- **Code Interpreter / tool use** — with Code Interpreter enabled, can execute Python, generate files, and validate outputs at runtime rather than just producing text
- **Iterative dialogue** — responds well to back-and-forth refinement; adapts quickly when corrected
- **Concise summarization** — produces tight, well-scoped summaries of long inputs without unnecessary elaboration
- **Multi-modal input** — accepts images, documents, and data files as inputs (model-dependent)

## 2. Weak Spots & Limitations

- **Traceability discipline** — less consistent than Claude at maintaining requirement-to-work-item traceability across a long document; tends to drop source references in later sections
- **Instruction-following on complex formats** — will follow simple format templates reliably but drifts more than Claude on complex multi-section templates with many constraints
- **Hallucination on specific facts** — more prone than Claude to confidently stating plausible-sounding but incorrect specifics (API endpoint names, library method signatures, version numbers); outputs should be verified
- **Long-document consistency** — maintains role and instruction fidelity less reliably than Claude across very long outputs; may shift tone or drop constraints mid-document
- **PM orchestration framing** — less naturally suited to maintaining multi-role perspective simultaneously; tends to settle into a single voice rather than switching between role perspectives

## 3. Best-Fit Task Types

- Code generation (single-file and small-to-medium multi-file)
- Data analysis and transformation (especially with Code Interpreter)
- Quick prototyping and spike implementations
- API integration code
- Summarization of source documents
- Broad research tasks requiring synthesis across many topics

## 4. Poor-Fit Task Types

- Tasks requiring strict, sustained traceability across a long document
- PM orchestration across multiple roles in a single session
- Tasks where factual accuracy on specific version details or API specs is critical without verification
- Very long structured documents with many cross-references

## 5. Cognitive Style

☑ Analytical  ☐ Creative  ☐ Narrative  ☑ Literal
☐ Exploratory  ☐ Strategic  ☐ Cautious  ☑ Opinionated

**Context-Dependent Notes:**
Opinionated on code style and implementation choices; tends to commit to a specific approach more readily than Claude. Literal on instructions at the sentence level but less reliable on sustained multi-constraint compliance over long outputs.

## 6. Prompting Guidance

**Works Best When:**
- Given a specific, bounded code task with clear inputs and expected outputs
- Used with Code Interpreter enabled for tasks that benefit from runtime validation
- Given a concrete example of the desired output format
- Asked to produce a working prototype rather than a formal spec

**Avoid:**
- Long, multi-section structured documents with many traceability constraints
- Tasks where the output will not be reviewed before use (hallucination risk on specifics)
- Expecting it to maintain multi-role orchestration framing over a long session without re-prompting

## 7. Ideal Role Pairings

**Primary Roles:** DEV, AUTO

**Secondary / Support Roles:** CIS (code-side data modeling — e.g., schema generation from an ERD), QA (test case scripting, not test planning)

**Rationale:** ChatGPT's code generation strength and Code Interpreter capability make it the best fit for DEV implementation tasks and AUTO test scripting. It is better suited to receiving a Claude-produced WBS and implementing the DEV items than to producing the plan itself.

## 8. Collaboration Notes

**Best upstream AI:** Claude (receives WBS and role-specific work items from Claude's PM output)
**Best downstream AI:** Human review; or Claude for structured documentation of ChatGPT's code outputs
**Good as reviewer?** ☑ Yes — effective at reviewing code for correctness; less reliable for reviewing structured documents for traceability
**Good as initiator?** ☐ No — better as a receiver and implementer than as a PM-style orchestrator

## 9. Version Sensitivity

gpt-4o produces substantially better structured outputs than gpt-3.5-turbo. gpt-4o-mini is appropriate for quick, bounded tasks but should not be used for complex multi-role outputs. Profiles based on gpt-3.5 are outdated and should be refreshed. Code Interpreter availability varies by plan and interface — verify before relying on runtime validation.

## 10. Summary (One-Liner)

ChatGPT is the strongest implementer in the framework — best for DEV and AUTO roles — and works most effectively when receiving a structured plan from Claude rather than initiating one itself.

---

<!-- Tags: #coding #research #multimodal #tool-use #implementation -->
