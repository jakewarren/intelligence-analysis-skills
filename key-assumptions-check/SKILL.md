---
name: key-assumptions-check
description: |
  Performs a structured Key Assumptions Check (KAC) — a core Diagnostic SAT (Pherson & Heuer) — on any intelligence assessment, analytic judgment, argument, or planning assumption. Use whenever the user wants to identify explicit and implicit assumptions underlying an analysis, stress-test an assessment for hidden vulnerabilities, peer-review a draft product, or examine what would have to be true for a conclusion to hold.

  Trigger on: "run a KAC", "key assumptions check", "check the assumptions", "what are we taking for granted", "stress test this", "challenge the assumptions", "peer review this", "what would have to be true", "assumption review", "how robust is this assessment". Also trigger when a user pastes or uploads analysis and asks you to examine, challenge, or scrutinize it.

  Accepts input as a typed topic/assertion, pasted text, or uploaded document. Output can be inline chat, Word .docx, or HTML — ask the user if not clear from context.
---

# Key Assumptions Check (KAC)

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., Chapter 7*

## Purpose

A Key Assumptions Check makes explicit and challenges the assumptions — both stated and unstated — that underlie an analytic assessment. Most analytic errors originate not from flawed logic but from unexamined assumptions. Approximately one in four key assumptions collapses under careful scrutiny (Pherson). The goal is to surface those assumptions, evaluate their soundness, and understand what happens to the assessment if they are wrong.

---

## Step 1: Understand and ingest the input

Accept any of these forms:

- **Topic or assertion in chat** — e.g., "Run a KAC on the assessment that Iran will not develop a deliverable nuclear weapon within 18 months"
- **Pasted analysis text or notes** — Extract the core judgment from the raw material
- **Uploaded document** — Read the file and identify the key judgments and the logic supporting them

If the core assessment or key judgment is ambiguous, ask the user to state it as a single declarative sentence before proceeding.

---

## Step 2: Confirm scope with the user (briefly)

Ask one short message covering:

1. **Output format**: Inline in chat (fast, good for quick reviews), Word document (.docx, good for formal products and peer reviews), or HTML file (rich visual table with color-coded risk)?
2. **Depth**: Standard (5–10 most critical assumptions) or deep dive (10–20 assumptions including second-order and background beliefs)?

If the request makes the answer obvious — e.g., "write me a report" → .docx, "quick check" → inline — skip asking and proceed.

---

## Step 3: State the core assessment

Begin with the key judgment under examination as a single clear sentence. This anchors the entire analysis.

> *Example: "The assessment under review: China will not conduct a military seizure of Taiwan before 2028."*

---

## Step 4: Generate the assumption set

Brainstorm broadly before curating. Use multiple elicitation devices in combination:

### 4a. Work from the prevailing analytic line
Identify every argument that supports the conclusion, then ask: what must be true for this argument to hold?

### 4b. Apply the journalistic questions
For each key player or dynamic in the assessment:
- **Who**: Are we assuming we know who all the key players are?
- **What**: Are we assuming we know the goals of the key players?
- **How**: Are we assuming we know how they are going to act?
- **When**: Are we assuming conditions have not changed since the last report, or will not change in the foreseeable future?
- **Where**: Are we assuming we know where the real action is going to be?
- **Why**: Are we assuming we understand the motives of the key players?

### 4c. Scan for linguistic cues in the source text
These phrases in any analysis almost always signal a hidden assumption worth surfacing:
- "will always" / "will never" / "would have to be" — unchallenged absolutes
- "based on" / "generally the case" / "as usual" — implicit reliance on precedent
- "obviously" / "clearly" / "of course" — assumptions so embedded they feel like facts

### 4d. Probe across assumption categories
- **Explicit assumptions** — Claims the author actually stated as conditions or caveats
- **Implicit assumptions** — Things taken for granted but never stated. Most analytically dangerous. Probe:
  - What must be true about the adversary's or actor's *capabilities*?
  - What must be true about their *intentions* or *decision calculus*?
  - What *external conditions* is this assessment silently relying on (economic stability, third-party behavior, technology state)?
  - What is assumed about *our own* knowledge, collection access, or analytical judgment?
  - What *historical patterns or precedents* are being drawn on without acknowledgment?
  - What *threshold effects or nonlinear dynamics* are assumed away?
- **Background beliefs** — Worldview assumptions so deeply held they are invisible. Examples: "rational actor" assumptions, deterrence stability, institutional continuity. Push here in deep dives.

### 4d. Final prompt
When the flow of assumptions slows, ask: *"What else seems so obvious that one would not normally think about challenging it?"* — if no more can be found, that itself is an assumption.

**Rule for stating assumptions**: Write each one as a positive declarative sentence that could in principle be false.
- ❌ "Iran's nuclear program"
- ✅ "Iran's uranium enrichment remains below weapons-grade thresholds at all declared and undeclared sites"

---

## Step 5: Evaluate each assumption on five dimensions

| Dimension | What to assess |
|-----------|----------------|
| **Type** | Explicit / Implicit / Background belief |
| **Classification** | **S** = Basically solid; **C** = Correct with caveats; **U** = Unsupported or questionable (= "key uncertainty") |
| **Confidence** | HIGH (well-supported by direct evidence), MEDIUM (partial evidence or gap), LOW (thin evidence, largely inferred) |
| **Basis** | Brief note on what supports this assumption — specific reporting, collection, historical precedent, or logical derivation |
| **Impact if wrong** | CRITICAL (the core assessment collapses or reverses), SIGNIFICANT (major hedge required, confidence must drop), MINOR (the judgment survives with modest adjustment) |

**On the S/C/U classification**: This is the book's native taxonomy. "U" assumptions — those that are unsupported or questionable — are formally "key uncertainties" and should be prioritized for collection. An assumption classified as U with CRITICAL impact is the most dangerous finding a KAC can produce.

**Temporal decay check**: For each assumption, ask — *could this have been true in the past but no longer?* Intelligence assessments often rely on precedent that has quietly expired.

---

## Step 6: Assign risk levels

Risk level = f(confidence, impact). This is a practical enhancement for prioritizing analytic attention:

| | CRITICAL impact | SIGNIFICANT impact | MINOR impact |
|---|---|---|---|
| **LOW confidence** | 🔴 RED | 🟠 ORANGE | 🟡 YELLOW |
| **MEDIUM confidence** | 🟠 ORANGE | 🟡 YELLOW | 🟢 GREEN |
| **HIGH confidence** | 🟡 YELLOW | 🟢 GREEN | 🟢 GREEN |

🔴 **RED assumptions** are load-bearing and undervalidated. Any assessment resting on RED assumptions needs explicit caveats or targeted collection before publication.

---

## Step 7: Develop watchlist items for RED and ORANGE assumptions

For each 🔴 RED and 🟠 ORANGE assumption:

- **Confirming indicator** — What observable event or reporting would validate this assumption?
- **Falsifying tripwire** — What would signal this assumption has broken down?
- **Collection requirement** — Has this "key uncertainty" become a formal intelligence collection gap?

U-classified assumptions should almost always generate a collection requirement.

---

## Step 8: Weakest-link probability calibration

Apply this before writing the robustness assessment. The principle: *the probability of your analytic conclusion being accurate cannot be greater than the weakest link in your chain of reasoning.*

For each RED assumption, estimate roughly: what is the probability this assumption holds? Multiply across the chain of critical assumptions to get a rough upper bound on the probability the overall assessment is correct. This is not a formal calculation — it is a discipline to prevent false confidence from accumulating across a chain of individually plausible but collectively fragile assumptions.

> *Example: If three RED assumptions each have ~70% probability of holding, the joint probability the assessment survives all three is at most ~34%.*

Use this to calibrate the language in the robustness assessment and to determine whether confidence language in the product is warranted.

---

## Step 9: Produce the output

### Required structure

**Header**: Assessment under review | Date | Analyst (if provided)

**Section 1 — Core Assessment**
The key judgment stated in one sentence.

**Section 2 — Assumptions Table**
All assumptions in a structured table. Sort by risk level: 🔴 RED first, then 🟠 ORANGE, 🟡 YELLOW, 🟢 GREEN.

Columns: `#` | `Assumption` | `Type` | `S/C/U` | `Confidence` | `Basis` | `Impact if Wrong` | `Risk`

**Section 3 — Red Flag Analysis**
For each 🔴 RED assumption: a short paragraph explaining why it is load-bearing, what the failure mode looks like, and what analytic consequences follow.

**Section 4 — Watchlist and Collection Requirements**
Confirming indicators, falsifying tripwires, and collection requirements for RED and ORANGE (U-classified) assumptions.

**Section 5 — Robustness Assessment**
2–3 sentences of direct judgment on how well-founded the overall assessment is. Apply the weakest-link principle. Be direct. If the analysis rests on shaky foundations, say so. Include a rough probability framing if the chain of critical assumptions warrants it.

**Section 6 — Analyst Recommendations**
Specific, actionable steps: what to caveat in the product, what to collect, what to revisit, and whether a follow-on technique is warranted (see below).

---

## Relationship to other techniques

**What If? Analysis** — When a single assumption is both RED and load-bearing, follow the KAC with a What If? on that assumption. Imagine a present or future in which it is wrong. What could have caused that? What are the consequences?

**Analysis of Competing Hypotheses (ACH)** — Key assumptions must be entered as "evidence" in any ACH matrix. An assessment's consistency with a hypothesis may depend entirely on an assumption — the KAC makes that dependency visible. When two or more competing hypotheses each rest on different assumptions, an ACH is the right next step.

**Indicators Validation** — U-classified assumptions that become collection requirements feed directly into indicator development.

---

## Output format guidance

**Inline chat**: Markdown tables and headers. Good for quick turnarounds and internal discussion.

**Word (.docx)**: Use the `docx` skill. Formatted report with proper headings, styled assumptions table, color-coded risk column, and executive summary. Appropriate for formal peer reviews and finished intelligence.

**HTML**: Standalone file with risk-level row highlighting (red/orange/yellow/green). Good when a visual artifact needs to be shared or embedded.

For peer review or report contexts, recommend a formatted file so the analyst can attach it to the product.

---

## Analyst principles

**Distinguish assumptions from facts.** If it is in raw intelligence reporting, it may be a fact. If the analyst is relying on it without direct evidence, it is an assumption.

**Implicit assumptions are the prize.** Any analyst can list the stated assumptions. The KAC's value is in surfacing what is hidden in the analytical logic.

**Watch for temporal decay.** Intelligence often relies on assumptions drawn from past behavior. The most dangerous assumptions are ones that were valid when first formed and have quietly expired.

**If the KAC surfaces no RED assumptions, look harder.** Complex assessments about adversary behavior, technology, or intent almost always have them. ~25% of key assumptions collapse on careful examination (Pherson).

**This is not a verdict.** The KAC can surface multiple RED assumptions and the assessment can still be correct. The goal is to understand the vulnerability profile of the analysis, not to falsify the conclusion. The output should illuminate risk, not determine truth.
