---
name: analysis-of-competing-hypotheses
description: |
  Performs a full Analysis of Competing Hypotheses (ACH) — the flagship Diagnostic SAT (Pherson & Heuer). Use when the user wants to systematically evaluate multiple competing explanations for what has happened, is happening, or is likely to happen. ACH overcomes Confirmation Bias by rejecting hypotheses rather than confirming them: the lead hypothesis has the fewest inconsistencies, not the most supporting evidence.

  Trigger on: "run an ACH", "analysis of competing hypotheses", "most likely explanation", "evaluate these hypotheses", "which hypothesis fits the evidence", "build an ACH matrix", "could this be deception", "weigh the evidence against each scenario". Also trigger when a user presents a complex analytic problem with multiple plausible explanations, or follows a Key Assumptions Check by asking which hypothesis to pursue.

  Accepts a typed question, pasted reporting, or uploaded document. Output can be inline chat, Word .docx, or HTML.
---

# Analysis of Competing Hypotheses (ACH)

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §7.6 — developed by Richards J. Heuer Jr., CIA, mid-1980s*

## Purpose

ACH is a systematic process for evaluating multiple hypotheses against a full body of evidence, assumptions, and gaps — then **rejecting** the hypotheses with the most inconsistencies rather than confirming the one that looks most attractive. This directly counters the analyst's most common failure mode: Satisficing (anchoring on a favored hypothesis and cherry-picking confirming evidence). The technique applies Karl Popper's principle of falsifiability to intelligence analysis.

The scientific insight at the core of ACH: **the most likely hypothesis is the one with the least inconsistent information**, not the one with the most supporting information — because much of the evidence that appears to confirm a hypothesis is equally consistent with competing hypotheses and is therefore non-diagnostic.

---

## Step 1: Ingest the input

Accept any of these forms:

- **Problem statement in chat** — e.g., "Run an ACH on who is behind the cyberattack on the power grid"
- **Pasted analysis or raw reporting** — Extract the core question and any stated hypotheses from the material
- **Uploaded document** — Read the file and identify the key analytic question and all evidence or indicators present

The analytic question should be framed as a question with discrete possible answers, not as a judgment to confirm. If it is phrased as a conclusion ("X is doing Y"), reframe it as the question driving that conclusion ("What is X doing, and why?").

---

## Step 2: Scope the analysis (briefly confirm with user)

Ask one short clarifying message covering:

1. **Output format**: Inline in chat (fast, quick review), Word document (.docx, formal product), or HTML (rich visual matrix with color-coded scoring)?
2. **Depth**: Quick scan (3–5 hypotheses, 6–10 evidence items) or full ACH (5–8 hypotheses, 10–20 evidence items)?
3. **Deception hypothesis**: Should a "deception/denial" hypothesis be included? (Recommend yes whenever adversary intent is a factor or when the most obvious answer is suspiciously tidy.)

If the request makes the answers obvious — e.g., "quick look" → inline, "write a report" → .docx — skip asking and proceed.

---

## Step 3: Generate the hypotheses

Generate all plausible, mutually exclusive explanations that cover the full solution space. "Mutually exclusive" is the critical constraint: if one hypothesis is true, all others must be false. Hypotheses must be stated as discrete outcomes, not as ranges or spectrums.

### Guidance on hypothesis generation

- **Aim for 4–8 hypotheses.** Too few (2–3) will almost always leave out important possibilities. Too many (9+) makes the matrix unwieldy.
- **Name hypotheses clearly and specifically.** "Hypothesis 1" is not useful. State each as a brief declarative assertion.
- **Include at least one null hypothesis** — e.g., "No significant activity is occurring / this is routine."
- **Include a deception hypothesis** whenever the adversary has motive, opportunity, and means to deceive — and especially if one hypothesis already looks overwhelmingly supported by the available evidence. Obvious evidence is a classic deception indicator.
- **Cover the full solution space.** Ask: is there any possible true explanation that is not represented by one of these hypotheses? If yes, add it.
- **Consider adding a compound hypothesis** ("both X and Y") if two non-exclusive actors or causes might be jointly responsible.

> *Tip: Cluster Brainstorming or Multiple Hypothesis Generation (§7.4) can be used upstream to generate a richer hypothesis list before entering the ACH matrix.*

After generating the hypotheses, present them to the user and confirm before building the matrix. This is the highest-leverage step — a poorly formed hypothesis set cannot be rescued by good evidence rating.

---

## Step 4: Compile the evidence list

Build the list of relevant information — everything that would help evaluate the hypotheses. This includes:

- **Hard evidence** — Directly observable facts, confirmed reports, signals intelligence, imagery, etc.
- **Soft evidence** — Source reporting with uncertainty about reliability or credibility
- **Assumptions** — Things the analysis is taking for granted but that are not directly evidenced (include these explicitly — they can be as diagnostic as hard evidence)
- **Gaps / absence of evidence** — Things one would *expect* to observe if a hypothesis were true but that are not present (the "dog that didn't bark" — Sherlock Holmes). Absence of an expected indicator is often more diagnostic than the presence of confirming evidence.

### Evidence statement rules
- State each item as a specific, neutral factual claim — not as a conclusion
- Rate the **credibility** of each item (HIGH / MEDIUM / LOW) — highly credible items that are inconsistent carry more weight than low-credibility inconsistencies
- Note the **source type** for each item (e.g., HUMINT, SIGINT, OSINT, own analysis/assumption, gap)

> *Tip: If a Key Assumptions Check (KAC) has already been run on this topic, the assumptions it identified should be entered as evidence items in the matrix.*

---

## Step 5: Build and score the matrix

Create a matrix with **hypotheses across the top** and **evidence items down the left side**. Score each cell with one of these ratings:

| Rating | Meaning |
|--------|---------|
| **C** | Consistent — this item is expected if the hypothesis is true |
| **CC** | Strongly Consistent — this item strongly supports and would be unusual if the hypothesis were false |
| **I** | Inconsistent — this item is not expected if the hypothesis is true |
| **II** | Strongly Inconsistent — this item sharply contradicts the hypothesis; this hypothesis struggles to accommodate this evidence |
| **NA** | Not applicable — this item has no bearing on this hypothesis |

### The diagnostic test
For each cell, ask: **"If this hypothesis were true, would I expect to see this evidence?"**
- "Yes, definitely" → C (or CC if uniquely expected)
- "No, I would not expect this" → I (or II if sharply contradictory)
- "Doesn't matter either way" → NA
- "It all depends on…" → your rating is based on an assumption; record that assumption

**Diagnostic value** is the key concept here. An item is diagnostic when it discriminates between hypotheses — ideally scoring C for one and I for others. Items that score C across all hypotheses are non-diagnostic noise; they do not help identify the correct hypothesis regardless of how compelling they feel. Identify and flag these.

### The assumption trap
When you find yourself saying "it depends on whether X is true," record X as an assumption driving that cell's rating. After completing the matrix, scan the assumptions for patterns — if the same assumption is driving multiple II ratings for your lead hypothesis, your conclusion is more fragile than it appears.

---

## Step 6: Calculate Inconsistency Scores and draw tentative conclusions

For each hypothesis, calculate the **Inconsistency Score**:

- Count all I and II ratings (counting II as 2)
- Adjust downward for any I/II ratings driven by low-confidence assumptions
- The hypothesis with the **lowest Inconsistency Score** is tentatively the most likely

**Critical principle**: Do not look for the hypothesis with the most C ratings. Look for the hypothesis that *cannot be refuted*. A hypothesis with three C ratings and zero I ratings is stronger than one with ten C ratings and three I ratings.

### Ranking the hypotheses
1. **Lead hypothesis** — lowest Inconsistency Score; tentatively most likely
2. **Viable alternatives** — low Inconsistency Scores; cannot be ruled out
3. **Unlikely** — moderate Inconsistency Score; possible but requires explaining away significant inconsistencies
4. **Refuted** — high Inconsistency Score; multiply inconsistent with the evidence body

Present the ranking and reasoning before moving to sensitivity analysis.

---

## Step 7: Sensitivity analysis

The Inconsistency Score is a tool, not an oracle. Before finalizing, stress-test the lead hypothesis by identifying which evidence items it critically depends on.

For each item that produced a **C or CC for the lead hypothesis and an I or II for all alternatives**:

1. **How credible is this item?** (High-credibility items are robust; low-credibility items are vulnerability points)
2. **What if this item were wrong, deceptive, or differently interpreted?** If the lead hypothesis collapses when a single low-credibility item is questioned, the conclusion is fragile
3. **What if the absence-of-evidence items reflect a collection gap rather than true absence?**

Also ask:
- Is there one hypothesis that has slightly elevated Inconsistency Scores but rests on firmer evidence overall?
- Are the Inconsistency Scores for the top two hypotheses close enough that they are essentially tied? If so, frame as genuine uncertainty rather than a weak lead hypothesis.
- Does the deception hypothesis remain viable? If so, what would deception look like and what would it require?

### Five pitfalls that can make the scores misleading (Pherson & Heuer)
1. **Assumptions omitted from the matrix** — If scores don't match your intuition, your logic may rest on things not yet entered as evidence
2. **Insufficient evidence to refute weak hypotheses** — Low I count for an implausible hypothesis may mean you haven't found its refuting evidence, not that it's credible
3. **Definitive source** — One highly reliable, well-placed source can outweigh a dozen routine reports; the matrix may underweight this
4. **Unbalanced evidence** — If you have 15 items on one peripheral dimension and 2 on the core question, the scores will mislead
5. **Diminishing returns** — In a large matrix (50+ items), each new item has less impact; partition older vs. newer evidence if tracking change over time

---

## Step 8: Report the conclusions

Structure the output as follows:

### Required output structure

**Header**: Problem statement | Date | Analyst (if provided)

**Section 1 — Analytic Question**
The question being evaluated, stated as a single clear sentence.

**Section 2 — Hypothesis Set**
All hypotheses numbered and named. Note any deception hypothesis explicitly.

**Section 3 — ACH Matrix**
The full matrix with evidence items, ratings, credibility, and source type. Color-coding or formatting should visually distinguish C/CC (support) from I/II (inconsistency) from NA (neutral).

**Section 4 — Inconsistency Scores and Ranking**
Ranked list of hypotheses by Inconsistency Score with brief rationale for each ranking. Explicitly address any cases where scores are close and genuine uncertainty exists.

**Section 5 — Sensitivity Analysis**
Identify the 2–4 most critical evidence items that are load-bearing for the lead hypothesis. State what the analysis would conclude if those items were wrong or reinterpreted.

**Section 6 — Lead Assessment**
A direct statement of the most likely hypothesis with a confidence level (HIGH / MEDIUM / LOW) and the primary evidentiary basis. If two hypotheses are essentially tied, say so.

**Section 7 — Indicators for Future Monitoring**
Two lists:
- **Confirming indicators** — future events or reporting that would increase confidence in the lead assessment
- **Falsifying tripwires** — events or reporting that would indicate the lead hypothesis is wrong and a different hypothesis is gaining validity

---

## Step 9: Confirm output format and deliver

Deliver the output in the requested format:

**Inline chat**: Use markdown tables for the matrix. Suitable for quick-turnaround analysis and internal discussion.

**Word (.docx)**: Use the `docx` skill. Formatted report with proper headings, styled matrix table, and an executive summary. Appropriate for formal analytic products and peer review.

**HTML**: Standalone file with color-coded matrix cells (green for C/CC, red for I/II, gray for NA) and sortable rows. Good for collaborative review or sharing.

For any formal product, a .docx output is recommended so the analyst can attach the ACH as an annex.

---

## Analyst principles

**The diagnostic discipline is everything.** The most seductive trap in ACH is focusing on all the evidence that supports the favored hypothesis. Force attention instead to what is *inconsistent*. One strong II counts more than three C ratings.

**Include assumptions as evidence.** If the matrix only contains hard facts, it is not an accurate reflection of the analyst's actual reasoning. Hidden assumptions that drive the analysis belong in the matrix, labeled as assumptions, so they can be scrutinized.

**The absence of expected evidence is evidence.** If a hypothesis predicts you should see X, and X is not present, that absence is I (inconsistent). Do not ignore what is missing.

**Obvious answers warrant extra scrutiny.** If one hypothesis is overwhelmingly supported and the others are weak, ask: is this what deception would look like? The most obvious explanation is precisely what a sophisticated adversary would try to engineer.

**ACH does not make the judgment for you.** The Inconsistency Score is a structured input to judgment, not a mechanical answer. Override the score — and document why — when definitive sourcing, unbalanced evidence, or known gaps justify it.

**Record where analysts disagree.** In a team setting, the most valuable output of ACH is often not the lead hypothesis but the precise cells where analysts rated the same evidence differently. Those disagreements reveal different assumptions about the adversary, the operating environment, or collection reliability — and those assumptions deserve explicit examination.

---

## Relationship to other techniques

**Key Assumptions Check (KAC)** — Run a KAC before or during ACH. KAC assumptions should be entered as evidence items in the matrix. Conversely, the "it all depends on…" observations from ACH cell-rating become the KAC's most productive inputs. These two techniques are natural complements.

**Multiple Hypothesis Generation (§7.4)** — Use upstream of ACH when the hypothesis set is unclear. Quadrant Hypothesis Generation and the Multiple Hypotheses Generator® are structured brainstorming tools that feed directly into Step 3 of ACH.

**Diagnostic Reasoning (§7.5)** — Incorporated within ACH. Each cell-rating in the matrix is an application of Diagnostic Reasoning — evaluating a single item of evidence against a single hypothesis.

**Argument Mapping (§7.9)** — Use downstream of ACH. Once ACH has identified the most likely hypothesis, Argument Mapping develops and evaluates the evidentiary case *for* that specific conclusion in a more formal logical structure. ACH = early stage (which hypothesis?); Argument Mapping = later stage (how well does the case hold?).

**Deception Detection (§7.8)** — Enter deception indicators (adversary motive, opportunity, means, past deception practices) as evidence items in the ACH matrix. If the deception hypothesis remains viable after full ACH, escalate to formal Deception Detection.

**Indicators Generation (§9.11)** — The indicators produced in Step 9 of ACH become direct inputs to formal Indicator validation and monitoring.
