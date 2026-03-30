---
name: critique-partner
description: Use when you need to evaluate a design artifact — concept, scope doc, sharing draft, or any output — against its stated intent and constraints
---

## 1. Ingest

Read the artifact to be critiqued. This can be provided as `$ARGUMENTS` (a file path, pasted content, or description) or identified from conversation context.

Scan `design-artifacts/` and one level of subfolders for the **upstream artifacts** that define intent — briefs (`*--brief.md`), sensemaking (`*--sense.md`), strategy (`*--strategy.md`), scope (`*--scope.md`), concepts (`*--concept.md`), and prior critiques (`*--critique.md`). Read whatever establishes the criteria this artifact should be evaluated against: the problem statement, success criteria, constraints, acceptance criteria, or strategic questions.

If no upstream artifact exists and the user hasn't stated criteria, ask: **what should this be evaluated against?** Don't critique in a vacuum — evaluation without criteria is just opinion.

## 2. Evaluate

Assess the artifact against its stated intent. For each finding, name:

- **What** — the specific element being evaluated (quote or reference directly)
- **Against** — which criterion, constraint, or stated intent it's measured against
- **Finding** — whether it delivers, partially delivers, misses, or contradicts
- **Why it matters** — downstream impact if unaddressed

Organize findings by significance, not by location in the artifact. Lead with what matters most.

**Findings are:**
- **Hits** — where the artifact delivers on intent. Don't skip these — confirming what works is as valuable as flagging what doesn't.
- **Gaps** — where stated criteria aren't addressed
- **Tensions** — where the artifact partially delivers but creates tradeoffs
- **Contradictions** — where the artifact works against its own stated intent

Present the evaluation. **Stop and wait.**

## 3. Heuristic review (opt-in)

After presenting the criteria-based evaluation, offer: **"Want me to also review against general design heuristics — accessibility, consistency, cognitive load, edge cases, error states?"**

If the user opts in, apply heuristics relevant to the artifact type. Don't run a generic checklist — select the 3-5 heuristics most likely to surface real issues for this specific artifact. Flag only findings that would materially affect the design, not theoretical concerns.

If the user declines or doesn't respond, skip to Recommend.

## 4. Recommend

Based on findings, propose concrete next steps:

- **Fix** — specific changes to the artifact that would resolve gaps or contradictions
- **Revisit upstream** — if the problem is in the brief, scope, or strategy, name it. Don't patch downstream artifacts to work around upstream issues.
- **Next skill** — if critique reveals the need for more research, rethinking, or re-scoping, name the skill explicitly

Present recommendations. **Stop and wait** for the user to confirm before saving.

## 5. Save

Save to `design-artifacts/<descriptive-name>--critique.md`, where `<descriptive-name>` is 2-4 hyphenated words describing the artifact's focus (e.g., `design-artifacts/onboarding-flow--critique.md`).

Start the file with an H1 title: `# Critique: <title>` (e.g., `# Critique: Onboarding Flow Concept`).

Structure:

- **Artifact evaluated** — what was critiqued, with reference to the source artifact
- **Criteria** — what it was evaluated against (upstream artifact or stated intent)
- **Findings** — hits, gaps, tensions, contradictions (compressed from the evaluation)
- **Heuristic review** — if conducted, key findings (omit section if not)
- **Recommendations** — proposed next steps
- **Open threads** — anything surfaced but not resolved

The artifact must be **self-contained** — readable without conversation context.

**Anti-pattern: "Everything needs improvement."** Critique that flags everything is as useless as critique that flags nothing. If you can't rank findings by significance, you haven't done the evaluative work — you've made a list. Lead with what matters most and be honest when something works well.

**Anti-pattern: "The brief didn't mention it, so it's fine."** Explicit criteria come first, but obvious structural problems (a flow with no error handling, a concept that ignores a primary user group) should be flagged even if the brief was silent. Use judgment — this is evaluation, not compliance checking.

## Artifact Directory

Skills save artifacts to `design-artifacts/`. Create the directory if it doesn't exist. When scanning for existing artifacts, check `design-artifacts/` and one level of subfolders — users may manually organize artifacts into subfolders. Before writing, check if an artifact already exists at the target path. If it does, read it — the current run's output should reflect awareness of prior work, not blindly replace it.

## Rules

- Be direct. No preamble, no filler.
- Quote or reference the specific artifact content being evaluated — don't make vague claims.
- Every finding traces back to a named criterion. If you can't name what it's evaluated against, it's opinion, not critique.
- Hits matter. Confirming what works prevents unnecessary rework and builds trust in the critique.
- Rank by significance. The user should know what to fix first.
- If the problem is upstream, say so. Don't recommend patching a concept when the brief is the issue.
- Heuristic review is opt-in, not default. Don't sneak it in.
- Artifacts must be self-contained. Someone reading the file with no conversation context should understand the evaluation.

$ARGUMENTS
