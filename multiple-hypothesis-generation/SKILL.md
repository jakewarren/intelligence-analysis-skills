---
name: multiple-hypothesis-generation
description: |
  Performs a structured Multiple Hypothesis Generation (MHG) session — a core Diagnostic SAT (Pherson & Heuer, §7.4). Generates a MECE (Mutually Exclusive, Comprehensively Exhaustive) hypothesis set using the right method for the problem: Simple Hypotheses (open brainstorming), Quadrant Hypothesis Generation (two-driver 2×2 matrix), or Multiple Hypotheses Generator® (Who/What/Why permutation attack on a dominant lead). Output feeds directly into ACH.

  Trigger on: "generate hypotheses", "what could explain this", "brainstorm hypotheses", "I need hypotheses for ACH", "run an MHG", "challenge the lead hypothesis", "what else could be going on". Also trigger when a user is about to run ACH without a defined hypothesis set, or when analysis is anchored on a single explanation.

  Accepts a typed problem statement, pasted reporting, or uploaded document. Output can be inline chat, .docx, or HTML.
---

# Multiple Hypothesis Generation (MHG)

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §7.4 — techniques developed by Pherson Associates, LLC*

## Purpose

Multiple Hypothesis Generation is a structured pre-analytic process that forces consideration of the full range of plausible explanations before the analyst commits to testing any single one. The goal is a **MECE hypothesis set**: **M**utually **E**xclusive (if one hypothesis is true, all others must be false) and **C**omprehensively **E**xhaustive (no important explanation has been left out).

The technique directly counters four of the most consequential analytic failure modes:

- **Confirmation Bias** — seeking only information consistent with the lead hypothesis
- **Anchoring Effect** — treating the lead hypothesis as the only legitimate starting point
- **Premature Closure** — stopping the search for explanations once a satisfying answer is found
- **Desire for Coherence / Uncertainty Reduction** — pattern-matching random or ambiguous events into a tidy narrative

When used properly, the quality of the hypothesis set — not the choice of a lead hypothesis — becomes the analyst's primary concern.

---

## Step 1: Ingest the input

Accept any of these forms:

- **Problem statement in chat** — e.g., "Generate hypotheses for why North Korea conducted a missile test this week"
- **Pasted analysis or raw reporting** — Extract the core question and any asserted or implied explanations
- **Uploaded document** — Read the file; identify the analytic question, any stated hypotheses, and any evidence already in hand

Frame the core question as a question that admits multiple discrete answers, not as a conclusion to confirm. If the user has stated a conclusion ("X is doing Y because of Z"), reframe it as the question underlying that conclusion ("Why is X doing Y?").

---

## Step 2: Choose the method (confirm with user)

Ask one short message covering:

1. **Method**: Which of the three methods best fits this problem? (Guidance below — recommend based on the problem structure, but defer to the user.)
2. **Output format**: Inline in chat, Word document (.docx), or HTML?

### Method selection guidance

| Condition | Recommended method |
|-----------|-------------------|
| No dominant lead hypothesis; solution space open; many possible actors, causes, or explanations | **Simple Hypotheses** |
| The outcome is driven by two identifiable key forces; need a structured 2×2 set of scenarios | **Quadrant Hypothesis Generation** |
| A lead hypothesis already dominates; need to systematically challenge it and generate plausible alternatives | **Multiple Hypotheses Generator®** |
| Planning to feed results directly into ACH and want maximum coverage | **Multiple Hypotheses Generator®** or **Simple Hypotheses** (both produce richer sets than Quadrant) |

If the request makes the method obvious — e.g., "two key drivers" → Quadrant, "challenge the lead" → MHG® — skip asking and proceed.

---

## Step 3: Apply the selected method

---

### Method A: Simple Hypotheses

*Best when: the problem is open-ended, no strong lead exists, and maximum breadth is needed.*

**Step A1 — Define the problem**
State the issue, activity, or behavior under examination as a single clear question. Determine how the hypotheses will be used: as inputs to ACH, as a basis for scenario development, or as a means to draw attention to particularly significant outcomes.

**Step A2 — Brainstorm candidate explanations**
Generate candidate explanations using three thinking modes in combination:

- **Theory-based**: What does the study of similar events suggest about plausible explanations? Draw on historical patterns and general knowledge of the domain.
- **Historical analogy**: What precedents from analogous cases point to alternative explanations that might otherwise be overlooked?
- **Situational logic**: What does the constellation of known facts, actors, interests, and situational pressures suggest? Reason from the ground up.

Prompt creative expansion by asking:
- What explanation would a skeptic offer?
- What would a hostile actor *want* us to believe?
- What is the simplest possible explanation?
- What is the most alarming possible explanation?
- What explanation would be most embarrassing to the analyst or institution if correct?

**Step A3 — Aggregate into affinity groups**
Cluster candidate explanations by theme or mechanism. Label each cluster. Within each cluster, identify the best representative explanation and note key variants.

**Step A4 — Apply journalistic stress-test**
For each candidate hypothesis, interrogate it with the journalist's questions:
- **Who** is the actor? Are we assuming we know all relevant actors?
- **What** is actually happening? Have we characterized the activity correctly?
- **How** is it being done? Does our explanation require capabilities we haven't confirmed?
- **When** is this occurring? Are timing assumptions baked in?
- **Where** is this happening or originating?
- **Why** — what motive or interest drives this explanation?

**Step A5 — Consider the opposite**
For each leading explanation, explicitly state its opposite. Ask: under what conditions would the opposite be true? If those conditions are plausible, add the opposite as a candidate hypothesis.

**Step A6 — Draft the final hypothesis set**
Consolidate, eliminate duplicates, and draft the final set. Apply the MECE test and the STOP criteria (see below). Aim for 4–8 hypotheses; flag if fewer than 4 were achievable.

---

### Method B: Quadrant Hypothesis Generation

*Best when: the outcome of the situation will be determined by two identifiable key driving forces.*

**Step B1 — Identify the two key drivers**
Using brainstorming or expert elicitation, identify the two forces most likely to determine the outcome. Each driver should be:
- A genuine source of uncertainty (not a known or fixed quantity)
- Independent of the other driver (or at least not fully correlated)
- Directly consequential for the outcome in question

If more than two plausible drivers exist and analysts cannot agree on which two dominate, this method is less appropriate — use Method A or C instead.

**Step B2 — Construct the 2×2 matrix**
Draw a matrix with Driver 1 as the horizontal axis and Driver 2 as the vertical axis. Place the extreme conditions of each driver at the ends of each axis (high/low, strong/weak, centralized/decentralized, etc.).

**Step B3 — Characterize each quadrant**
For each of the four cells, describe the end state that would result from the combination of the two extreme conditions. Be specific: what does this world look like? Who wins, who loses? What behaviors are observable?

**Step B4 — State the hypotheses**
Translate each quadrant into a formal hypothesis using the STOP criteria. Each quadrant must yield exactly one hypothesis. The four hypotheses are, by construction, mutually exclusive and comprehensively exhaustive of the two-driver space.

**Step B5 — Develop signposts**
For each hypothesis, identify 2–3 observable indicators or signposts that would suggest events are moving toward that quadrant. These become direct inputs to an ACH evidence list or to an indicator monitoring regime.

---

### Method C: Multiple Hypotheses Generator®

*Best when: a dominant lead hypothesis exists and must be systematically challenged. Particularly powerful as an ACH preparation tool.*

**Step C1 — Identify and state the lead hypothesis**
State the currently dominant explanation as a declarative hypothesis. Confirm it satisfies STOP criteria.

**Step C2 — Decompose into Who / What / Why**
Break the lead hypothesis into its three core components:
- **Who** — the actor(s) responsible
- **What** — the action, activity, or behavior being explained
- **Why** — the motive, intent, or driver behind it

For each component, generate 3–5 mutually exclusive alternatives. Ask:
- What variations could challenge the assumption about [WHO]?
- What different activities or interpretations could replace [WHAT]?
- What alternative motives or drivers could replace [WHY]?

Keep alternatives within each column mutually exclusive.

**Step C3 — Generate permutations**
Systematically cross all combinations: each Who × each What × each Why = one permutation. For 3 Whos × 3 Whats × 3 Whys, this produces 27 permutations. For 3×3×4, it produces 36.

**Step C4 — Prune implausible permutations**
Discard any permutation that is logically incoherent or requires capabilities/conditions that are directly contradicted by known facts. Document the reason for each discard — these reasons may themselves be unexamined assumptions worth noting.

Do not discard a permutation merely because it is uncomfortable, unfamiliar, or inconsistent with the lead hypothesis. That is precisely the bias this method exists to defeat.

**Step C5 — Score remaining permutations on credibility**
For each surviving permutation, assign a credibility score (1–5 scale, where 1 = very low credibility, 5 = high credibility):
- Score each component (Who, What, Why) individually on plausibility
- Challenge the key assumption underlying each component: is it actually supported by evidence, or is it taken for granted?
- The composite score is a rough product, not a sum — a permutation with one deeply implausible component scores low overall

**Step C6 — Re-sort and select**
Rank permutations from most to least credible. Select the top candidates — typically the highest-scoring 4–8 permutations — for restatement as formal hypotheses.

**Step C7 — Restate as hypotheses**
Convert each selected permutation into a formal hypothesis using the STOP criteria. The resulting set will challenge the lead hypothesis with alternatives that have been generated by logic rather than by intuition.

---

## Step 4: Apply MECE and STOP quality tests

Before finalizing any hypothesis set, apply both quality tests.

### MECE test

**Mutually Exclusive**: For any two hypotheses in the set, ask — if hypothesis A is true, can hypothesis B also be true? If yes, one of the following is required:
- Merge them into a single hypothesis
- Restate them to make the distinction clear and exclusive
- Add a compound hypothesis ("both A and B simultaneously") as a separate entry

**Comprehensively Exhaustive**: Ask — is there any logically possible true explanation that is not represented by one of these hypotheses? If yes, it must be added or explicitly ruled out with justification.

A useful completeness check: have you included a **null hypothesis** ("nothing significant is actually happening; this is routine or coincidence")? If not, add one unless it can be ruled out by direct evidence.

### STOP criteria for each hypothesis

Each hypothesis must satisfy all four criteria:

- **S**tatement, not a question — declarative, not interrogative
- **T**estable and falsifiable — it must be possible in principle to find evidence that would refute it
- **O**bservation- and knowledge-based — grounded in what is actually known, not in pure speculation
- **P**redicts anticipated results clearly — states what evidence one would expect to observe if the hypothesis is true

Any hypothesis that fails the STOP test must be revised or replaced.

---

## Step 5: Stress-test for intuitive traps

Before finalizing, explicitly check whether any of four classic intuitive traps may have constrained the hypothesis set:

- **Single Solution Trap**: Does the set genuinely cover the full range of actors, causes, and methods — or does it tacitly assume only one actor type is plausible? Have we included the possibility that an actor we have not focused on is responsible?
- **Small Sample Overinterpretation**: Is the hypothesis set shaped by a very limited number of recent reports or a single compelling source? If so, are there hypotheses that cannot be distinguished based on the available evidence — and should the set reflect that ambiguity rather than collapsing to a false choice?
- **Past Experience Projection**: Does the set draw too heavily on how similar situations resolved in the past? Would a different historical analogy suggest an alternative explanation that is missing?
- **First Impression Reliance**: Does the hypothesis set look like what a first-read of the reporting would suggest? If so, what explanation would only emerge from slower, more deliberate reasoning?

If any trap is identified, add at least one hypothesis that the trap was suppressing.

---

## Step 6: Finalize and deliver the hypothesis set

### Required output structure

**Header**: Problem statement | Date | Analyst (if provided) | Method used

**Section 1 — Analytic Question**
The question being addressed, framed as a single clear sentence.

**Section 2 — Hypothesis Set**
All hypotheses numbered and stated in full declarative form. For each hypothesis:
- The hypothesis statement
- Brief rationale for inclusion (what logic, evidence, or analogy supports treating this as a plausible explanation)
- STOP compliance note if any hypothesis required revision

**Section 3 — MECE Assessment**
A brief statement confirming the set is mutually exclusive and comprehensively exhaustive — or noting where borderline cases required judgment calls and why they were resolved as they were.

**Section 4 — Recommended Priority Order**
If a preliminary credibility ranking is appropriate (especially after Method C), list hypotheses from most to least initially plausible. Be explicit that this ranking is provisional and is subject to revision by formal evidence testing.

**Section 5 — Signposts and Indicators** *(Method B only; optional for Methods A and C)*
For each hypothesis, 2–3 observable indicators that would suggest movement toward or away from that explanation.

**Section 6 — Recommended Next Step**
State explicitly which technique should be applied next:
- If 4–8 mutually exclusive hypotheses are ready: **Analysis of Competing Hypotheses (ACH)** — the hypothesis set feeds directly into ACH Step 3
- If key assumptions underlying the hypotheses are unclear: **Key Assumptions Check (KAC)** first, then ACH
- If the hypothesis set points to potential deception: **Deception Detection (§7.8)** alongside ACH

---

## Output format guidance

**Inline chat**: Markdown tables and numbered lists. Good for collaborative hypothesis development and rapid iteration.

**Word (.docx)**: Use the `docx` skill. Formatted report with proper headings, hypothesis table, MECE assessment, and a clean handoff document for the ACH analyst. Appropriate when this work will be reviewed or approved before proceeding.

**HTML**: Standalone file with the hypothesis set in a clean, printable format. Useful for team review or embedding in a product annex.

---

## Analyst principles

**The hypothesis set is the highest-leverage output.** An ACH run on a poorly constructed hypothesis set will produce a precise answer to the wrong question. Invest the effort here — a well-constructed MECE set often reveals the answer before the matrix is built.

**Breadth before pruning.** The most common error is premature narrowing. Generate more hypotheses than you think you need, then prune. Never prune during generation.

**The null hypothesis earns its place.** Including "nothing significant is actually happening" as a hypothesis is not intellectual timidity — it is a safeguard against pattern-matching noise into meaning. Eliminate it only when evidence directly contradicts it.

**Discomfort is signal.** If a hypothesis feels unlikely and also slightly threatening to the current analytic consensus, that is a reason to include it — not exclude it. Deception hypotheses and embarrassing-if-true hypotheses almost always deserve a slot in the set.

**MECE is a discipline, not a guarantee.** Achieving perfect mutual exclusivity in complex real-world problems is often impossible. Document where overlap remains and ensure the ACH matrix can handle it (by treating the overlapping hypotheses as competing despite partial overlap, or by creating a compound hypothesis).

**A strong prior is not evidence.** "Everyone knows X is responsible" is an assumption, not a hypothesis-eliminating fact. Track it as an assumption in the KAC; do not let it foreclose the hypothesis set.

---

## Relationship to other techniques

**Analysis of Competing Hypotheses (ACH, §7.6)** — The primary downstream consumer of MHG output. The hypothesis set produced here is entered directly into ACH Step 3. MHG and ACH together constitute the complete diagnostic cycle: MHG generates the candidates; ACH tests them against the evidence body.

**Key Assumptions Check (KAC, §7.1)** — Run a KAC before or alongside MHG when the problem involves a contested assessment. Assumptions surfaced by the KAC often reveal alternative hypotheses that would not otherwise be generated. Conversely, the act of generating alternative hypotheses in MHG frequently surfaces assumptions embedded in the lead hypothesis.

**Cluster Brainstorming (§6.2)** — A useful upstream tool for Simple Hypotheses (Method A). When the analyst lacks starting material, Cluster Brainstorming generates candidate explanations that MHG then structures and quality-tests.

**Quadrant Crunching™ (§8.1) / Morphological Analysis (§9.8)** — Quadrant Hypothesis Generation (Method B) is a specific application of the broader Morphological Analysis method. When the problem involves more than two key drivers, Morphological Analysis or Quadrant Crunching™ can generate a richer matrix.

**Alternative Futures Analysis / Multiple Scenarios Generation (§9.6–9.7)** — These foresight techniques produce outputs that can be treated as a set of alternative hypotheses. When the problem is forward-looking (assessing possible futures rather than explaining past events), these techniques are often preferable to Method B.

**Deception Detection (§7.8)** — When the MHG process consistently surfaces one overwhelmingly supported hypothesis that makes competing hypotheses seem implausible, consider whether the evidence pattern itself could be manufactured. The deception hypothesis should be explicitly added to the ACH matrix and escalated to formal Deception Detection if it survives initial testing.
