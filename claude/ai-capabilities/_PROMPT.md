# _PROMPT.md — Standardized AI Capability Profile Generation Prompt

## Purpose

This file contains the canonical prompt used to generate or refresh any AI capability profile in this directory. Paste it into the AI you are profiling, then save the output as `[ai-name].md` in this folder.

**Profiles are manually maintained.** They are not auto-generated or auto-refreshed. The `Last Reviewed` field is your reliability indicator — if it is stale, treat the profile as advisory only and use this prompt to refresh it.

**Cross-validation note:** The weak spots section of each profile should ideally be reviewed by a *different* AI or a human — the profiled AI may understate its own limitations. This is a known blind spot in self-assessment prompts.

---

## The Prompt

Paste the text below (from the horizontal rule onward) into the AI you are profiling. Replace `[AI NAME]` and `[MODEL STRING]` with the specific values for this engagement.

---

You are being asked to produce an honest, specific capability profile of yourself for use in a multi-AI professional team framework.

**The purpose of this profile:** A Project Manager agent will consult it when deciding which AI should execute which professional role (PM, CIS, Developer, QA, Automation, Doc Writer, Trainer) and how to sequence multi-AI handoffs. The profile must be useful for real delegation decisions — vague, diplomatic, or self-promotional entries defeat its purpose.

**Honesty requirement (read this first):** This profile will be used to route work to you or away from you. If you understate a weakness, work gets misrouted and produces worse results. Be specific about where you struggle. Entries like "sometimes makes mistakes" or "may have limitations in some areas" are not useful. Specific entries like "tends to over-explain simple answers, adding length without adding value" or "struggles to maintain consistent variable naming across multi-file code outputs" are useful.

**Model information for this profile:**
- AI Name: [AI NAME]
- Model string: [MODEL STRING]
- Today's date: [DATE]

Produce the profile using exactly this template. Do not add sections. Do not remove sections. Fill in every field.

---

```markdown
# AI Capabilities Profile

**AI Name:**
**Provider:**
**Model(s) Covered:**
**Last Reviewed:**

---

## 1. Core Strengths

What this AI consistently does better than others. Be specific — name the task types, not just abstract qualities.

## 2. Weak Spots & Limitations

Where this AI tends to struggle or underperform.

*(Be specific. Vague entries like "sometimes makes mistakes" are not useful. Name the failure mode and the context in which it appears.)*

## 3. Best-Fit Task Types

List the task types where this AI produces its strongest outputs.

## 4. Poor-Fit Task Types

List the task types where this AI should be avoided or used only with human review.

## 5. Cognitive Style

Check all that apply:

☐ Analytical  ☐ Creative  ☐ Narrative  ☐ Literal
☐ Exploratory  ☐ Strategic  ☐ Cautious  ☐ Opinionated

**Context-Dependent Notes:**
*(e.g., "Cautious on ethical topics, opinionated on code style")*

## 6. Prompting Guidance

**Works Best When:**

**Avoid:**

## 7. Ideal Role Pairings

**Primary Roles:** *(role names from the multi-role-team framework: PM, CIS, DEV, QA, AUTO, DOC, TRAIN)*

**Secondary / Support Roles:**

**Rationale:**

## 8. Collaboration Notes

**Best upstream AI:**
**Best downstream AI:**
**Good as reviewer?** ☐ Yes  ☐ No — *why:*
**Good as initiator?** ☐ Yes  ☐ No — *why:*

## 9. Version Sensitivity

Does output quality vary significantly between model versions? What changed between versions, and what broke?

## 10. Summary (One-Liner)

One sentence that captures this AI's most distinctive characteristic for team delegation purposes.

---

<!-- Tags: #reasoning #creative #coding #research #orchestration #real-time #multimodal -->
<!-- Apply tags that describe this AI's primary capabilities -->
```

---

**After generating the profile:** Review the Weak Spots & Limitations section yourself (or have a colleague review it) before saving. Confirm the entries are specific enough to be actionable. Save the file as `[ai-name].md` in the `ai-capabilities/` directory alongside this prompt.
