---
name: key-drivers-generation
description: |
  Performs Key Drivers Generation™ (KDG) and Key Uncertainties Finder™ (KUF) — the paired Foresight SATs (Pherson & Heuer, §9.1–9.2) that produce the MECE driver list required before any scenario exercise. KDG brainstorms candidate drivers via STEMPLES+; KUF converts fragile KAC assumptions into drivers. Meld both for a cross-validated list of 4–5 drivers.

  Trigger on: "key drivers", "key drivers generation", "identify the drivers", "run a KDG", "key uncertainties finder", "KUF", "what forces are shaping this", "generate drivers for scenarios", "drivers for AFA", "drivers for MSG", "scenario axes", "identify driving forces", "key uncertainties", "what factors will determine the outcome". Also trigger proactively when a user is about to run Alternative Futures Analysis or Multiple Scenarios Generation without a defined driver list.

  Accepts a focal question, pasted analysis, or uploaded document. Output: inline chat, .docx, or HTML.
---

# Key Drivers Generation™ / Key Uncertainties Finder™

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §9.1 (Key Drivers Generation™) and §9.2 (Key Uncertainties Finder™)*

## Purpose

Key Drivers Generation™ (KDG) and Key Uncertainties Finder™ (KUF) are the two standard Foresight SATs for producing a rigorous, cross-validated list of the forces and factors most likely to determine how a situation will evolve. Together they are the essential prerequisite for Alternative Futures Analysis, Multiple Scenarios Generation, and any other technique that requires analysts to define scenario axes.

A **key driver** is a basic force or factor — such as economic growth, popular support, conflict versus cooperation, or globalization — that affects behavior, performance, or strategy now or in the future. Key drivers are *not* nations, regions, or labels ("Russia," "cyber," "increased military spending"). They are fundamental dynamics that operate across actors and domains.

Both techniques counteract the same cluster of cognitive failures:

- **Anchoring Effect** — starting with a current condition and adjusting only slightly from it when imagining the future
- **Availability Heuristic** — overweighting drivers that come to mind easily (recent, vivid, familiar) and underweighting structural forces that are harder to visualize
- **Hindsight Bias** — treating the current trajectory as the only plausible one because it is the trajectory that happened to materialize from prior conditions
- **Assuming Inevitability** — failing to imagine that alternative drivers could realistically come to dominate
- **Overrating Behavioral Factors** — overweighting the role of individual leaders and personalities while underestimating situational and structural forces
- **Ignoring Base Rate Probabilities** — anchoring on a single plausible future while ignoring the statistical distribution of how similar situations have resolved historically

### Which technique — KDG or KUF?

| Situation | Recommended approach |
|-----------|----------------------|
| Starting a Foresight exercise from scratch | **KDG** (Cluster Brainstorming → candidate drivers) |
| A Key Assumptions Check has already been run | **KUF** (extract fragile assumptions → convert to drivers) |
| High-stakes product requiring comprehensive driver coverage | **Both** — meld the results into a single validated list |
| Driver list exists but feels incomplete or anchored on conventional wisdom | **KDG** as a challenge exercise |

The book's explicit recommendation: use both techniques and meld their findings. The two approaches attack the problem from different angles — KDG from creative brainstorming outward, KUF from assumption critique inward — and their convergence is a strong signal that a driver is genuinely fundamental.

---

## Step 1: Ingest the input

Accept any of the following:

- **Focal question in chat** — e.g., "What are the key drivers shaping North Korean nuclear posture over the next decade?" or "Generate drivers for an AFA on Venezuelan stability"
- **Pasted analysis or assessment** — Extract the core analytic judgment and the implicit assumptions embedded in it
- **Uploaded document** — Read the file; identify the topic, the current analytic baseline, and any drivers or assumptions already mentioned
- **Output from a prior KAC or What If? Analysis** — The fragile assumptions surfaced by a KAC are the direct input to KUF; treat them as a head start

Frame the focal question using this template if one is not provided: *"What are all the forces and factors that will determine how [X] evolves over the next [time horizon]?"* If no time horizon is stated, ask or default to 5–10 years and note the assumption.

---

## Step 2: Confirm scope (briefly)

Ask a single short message covering:

1. **Which technique(s)**: KDG only, KUF only, or both and meld? (Default to both if any analysis or prior KAC output is available.)
2. **Output format**: Inline in chat, Word (.docx), or HTML?
3. **Downstream use**: Is the driver list destined for Alternative Futures Analysis (need exactly 2 drivers), Multiple Scenarios Generation (need 3–5 drivers), or standalone Foresight planning (any number)?

If the request makes these obvious — e.g., "I just ran a KAC, now I need drivers for an AFA" → KUF → 2 drivers → inline — proceed without asking.

---

## Method A: Key Drivers Generation™

KDG adapts the Cluster Brainstorming technique to surface candidate drivers from first principles. In a live group setting this involves self-stick notes and silent kinetic brainstorming; when running this analytically, the logic is identical but executed through systematic prompting rather than physical brainstorming.

### Stage I — Generate candidate ideas

The focal question should begin with: *"What are all the [things / forces and factors / circumstances] that would help explain...?"*

Work through the **STEMPLES+** framework systematically. For each category, ask: *What force or factor in this domain is most uncertain and most consequential over the specified time horizon?*

| STEMPLES+ Category | Driver-generation prompt |
|--------------------|--------------------------|
| **S**ocial | What demographic shifts, identity dynamics, social cohesion trends, or public legitimacy questions could determine outcomes? |
| **T**echnological | What technological capabilities, disruptions, adoption curves, or information environment changes could be decisive? |
| **E**conomic | What growth trajectories, resource constraints, trade patterns, sanctions regimes, or fiscal pressures are in play? |
| **M**ilitary | What capability gaps, force posture choices, doctrine shifts, or readiness questions could tip the balance? |
| **P**olitical | What leadership succession dynamics, regime stability questions, coalition durability issues, or electoral outcomes matter? |
| **L**egal | What treaty frameworks, international norms, sanctions architectures, or legitimacy questions could constrain or enable actors? |
| **E**nvironmental | What climate pressures, resource scarcity, or natural disaster risks could exert force on the situation? |
| **S**ecurity | What threat network developments, alliance solidarity questions, or intelligence capacity issues could shape outcomes? |
| **+** | What demographic, religious, psychological, or informational factors deserve attention specific to this topic? |

For each STEMPLES+ category, generate as many candidate ideas as possible without evaluating them yet. The goal is breadth. Do not suppress ideas because they seem unlikely or speculative — the Availability Heuristic will filter out non-obvious drivers unless you deliberately protect them.

### Additional prompts to surface non-obvious candidates

- What assumptions embedded in the current analytic assessment would, if wrong, produce a radically different future? (Each fragile assumption may be a driver in disguise.)
- What single development would most surprise the analytic community — and what force would drive it?
- What factor does the decision-maker community currently underweight or not discuss that could prove decisive?
- What historical analogies suggest structural forces that current analysis may be ignoring?
- What driver, if it shifted from its current trajectory, would cause analysts to fundamentally revise their assessment?

### Stage II — Group into affinity clusters

Review all candidate ideas and group them by underlying concept or dynamic. Ideas that reflect the same basic force belong together even if they are phrased differently.

Label each group with the simplest phrase that captures its underlying dynamic. These labels become the candidate drivers. A well-labeled driver:

- Describes a dynamic, not an actor or outcome ("Regime cohesion" not "the regime" or "regime collapse")
- Is framed as a dimension or spectrum, not a fixed value ("Degree of external support" not "high external support")
- Could plausibly resolve in multiple directions over the time horizon

Expect 6–10 affinity clusters. The next step winnows these.

### Stage III — Select the key drivers

From the affinity clusters, identify the 4–6 that meet all of the following criteria:

| Criterion | Test question |
|-----------|---------------|
| **Fundamental** | Does this driver directly affect performance, behavior, or strategy? Or is it a downstream consequence of another driver? (Keep causes; cut effects.) |
| **Genuinely uncertain** | Could this driver plausibly resolve in materially different ways over the time horizon? (If the outcome is largely known, it is a constraint, not a driver.) |
| **Consequential** | If this driver shifts, does the overall situation shift significantly? (If not, it may be real but peripheral.) |
| **Non-obvious** | Does at least one driver on the final list capture a dynamic that would not immediately occur to an uninformed analyst? |

Then verify the list meets structural quality standards:

- **Mutually exclusive**: Drivers should not overlap or be variants of the same underlying dynamic. If two drivers are highly correlated (when one resolves high, the other almost always does too), they are capturing the same force and one should be dropped or they should be merged.
- **STEMPLES+ coverage**: The final list should not be entirely political or entirely military. Check that the set covers multiple dimensions of the problem. If a major domain (e.g., the economic dimension) is not captured, add a driver or revise an existing one to cover it.
- **Dimensionally frameable**: Each driver should be expressible as a spectrum with two plausible extreme endpoints — this is essential for any downstream scenario matrix construction.

**Target**: 4–6 candidate drivers from KDG.

If KUF will also be run, carry this list to Step 4 for melding rather than finalizing here.

---

## Method B: Key Uncertainties Finder™

KUF transforms the results of a Key Assumptions Check into candidate key drivers. It is particularly powerful because it draws on a prior structured analysis rather than open brainstorming — the assumptions it promotes to drivers have already survived scrutiny.

### Stage I — Conduct or import a Key Assumptions Check

If a KAC has already been run on this topic, import its findings directly. If not, run a KAC now (see the `key-assumptions-check` skill).

The KAC produces a list of assumptions classified as:
- **S (Solid)** — basically well-supported
- **C (Caveated)** — correct with conditions
- **U (Unsupported/questionable)** — key uncertainties

The **U-classified assumptions** are the input to KUF. These are things the analysis has been treating as settled that are, on examination, genuinely uncertain — and genuine uncertainty is what defines a driver.

### Stage II — Convert key uncertainties into candidate drivers

For each U-classified assumption from the KAC:

1. **Ask**: Is this uncertainty a critical variable — something that, depending on how it resolves, would produce materially different futures?
2. **Reframe as a driver**: State it not as an assumption ("The government will remain unified") but as a dynamic with a spectrum ("Degree of government cohesion" → [Highly unified] ←→ [Fragmented and contested]).
3. **Check the impact**: Does this driver, if it resolves at one extreme rather than the other, produce a significantly different situation? If yes, it is a candidate driver.

Not all U-classified assumptions become drivers. Some will be too narrow, too downstream, or too low-consequence to merit inclusion. Apply the same Fundamental / Uncertain / Consequential / Non-obvious filter used in KDG Stage III.

**Target**: 4–6 candidate drivers from KUF.

### Stage III — Meld the two driver sets

If both KDG and KUF have been run, compare the two candidate lists:

- **Convergent drivers**: A driver that appears in both lists (possibly under different labels) is the strongest candidate for the final set. It has survived two independent analytical approaches. Keep it.
- **Complementary drivers**: A driver that appears in only one list but covers a dimension not represented in the other list should be included if it meets the quality criteria.
- **Redundant drivers**: Two drivers from different lists that capture the same underlying dynamic should be merged into one, using the formulation that is more precisely specified and more easily framed as a spectrum.
- **Conflicting rankings**: If KDG and KUF disagree on whether a factor is a key driver, treat this as a signal that the factor may be important but contested — investigate the disagreement rather than automatically deferring to one method.

**Target for merged list**: 4–5 key drivers.

---

## Step 3: Define the spectrum for each driver

For each final driver, define the two extreme endpoints along which it could resolve over the time horizon. This transforms the driver from an abstract label into a structurally useful dimension for scenario construction.

**Spectrum endpoint requirements:**
- Both endpoints must be **plausible** — not science fiction, but not foregone conclusions either
- Endpoints should be **consequentially different**: if the situation were at one extreme versus the other, the overall assessment would look materially different
- Label each endpoint with a short descriptive phrase, not just "High/Low" or "Strong/Weak"

**Example:**
> Driver: *U.S. security commitment to the region*
> Spectrum: [Credible, forward-deployed, treaty-backed] ←→ [Retrenched, ambiguous, and transactional]

**Example:**
> Driver: *Regime internal cohesion*
> Spectrum: [Unified leadership with clear succession path] ←→ [Fractured elite, contested authority, institutional breakdown]

The spectrum definition is not a prediction about which endpoint is more likely — it is a structural description of the space the driver could occupy.

---

## Step 4: Validate the final driver list

Before delivering the output, run the following validation checks:

### Mutual exclusivity check
For each pair of drivers, ask: *If Driver A resolves at its high extreme, does that force Driver B to a particular extreme as well?* If yes, the two drivers are correlated and may be capturing the same underlying dynamic. Consider merging them or replacing one with a more independent force.

### Comprehensiveness check (STEMPLES+ audit)
Map each final driver to one or more STEMPLES+ categories. If a major domain (e.g., Economic, Military) has no driver covering it, ask whether the omission is justified (that domain genuinely does not shape the focal question) or whether a driver should be added.

### Non-obviousness check
Is at least one driver on the list a force or factor that would not immediately occur to an analyst working from conventional wisdom? A driver set that consists entirely of the most salient factors in the public debate is a warning sign — the Availability Heuristic may have dominated the brainstorming.

### Narrative coherence check
For each driver, ask: *Can I write a credible scenario in which this driver resolves at each extreme?* If a driver's high or low extreme produces a scenario that is internally incoherent or requires too many implausible simultaneous developments, the driver may be too abstract or the endpoints may be poorly calibrated.

---

## Step 5: Produce the output

### Required output structure

**Header**: Topic | Time horizon | Date | Analyst (if provided) | Method used (KDG / KUF / Both)

**Section 1 — Focal Question**
The question stated precisely, with the time horizon explicit.

**Section 2 — Key Drivers**
Present each final driver in a structured block:

```
Driver [N]: [Label]
Definition: [One sentence describing what this dynamic measures]
Spectrum: [Left/low extreme] ←→ [Right/high extreme]
Why it qualified:
  - Fundamental: [how it directly shapes behavior/performance/strategy]
  - Uncertain: [why it could plausibly resolve at either extreme]
  - Consequential: [what changes materially depending on how it resolves]
  - Non-obvious element: [what makes this driver analytically valuable beyond the obvious]
STEMPLES+ category: [one or more]
Source: [KDG / KUF / Both]
```

**Section 3 — Driver Interaction Notes**
A brief note on any important relationships or tensions *between* drivers. Drivers should be mutually exclusive, but they are not independent in the real world. Understanding their interactions helps scenario builders construct coherent narratives. Note especially:
- Driver pairs that are partially correlated (and why they remain distinct enough to keep separate)
- Driver pairs whose combination produces especially extreme or unexpected scenario worlds

**Section 4 — STEMPLES+ Coverage Map**
A simple table showing which STEMPLES+ categories are covered and which are not — and the rationale for gaps.

**Section 5 — Recommendations for Downstream Use**

*If the downstream technique is Alternative Futures Analysis (2 drivers needed)*: Identify the two drivers with the highest combined uncertainty × consequence score that are also sufficiently independent. Explain the selection and note which drivers were set aside and why.

*If the downstream technique is Multiple Scenarios Generation (3–5 drivers)*: Rank all drivers by uncertainty × consequence and recommend the top 3–5.

*If producing a standalone driver list*: Flag which drivers most urgently require additional collection or assessment before being used as scenario axes.

---

## Output format guidance

**Inline chat**: Markdown. Use a structured block for each driver (as above), a summary table for quick reference, and brief interaction notes. Good for collaborative development and rapid iteration before a scenario exercise.

**Word (.docx)**: Use the `docx` skill. A formatted analytic product suitable for distribution to a scenario team. Include a one-paragraph executive summary, the full driver blocks, the STEMPLES+ coverage table, and recommendations for downstream use.

**HTML**: Standalone file with a sortable driver table and spectrum visualization. Suitable for sharing with a scenario team working asynchronously.

---

## Analyst principles

**Drivers are dimensions, not predictions.** The most common error is confusing a driver with a forecast. "China will expand its naval presence" is a prediction. "Trajectory of Chinese naval expansion" is a driver — it describes the dimension along which uncertainty runs, and the scenario exercise will explore both extremes. Reframe predictions into dimensions before finalizing the list.

**Cause, not effect.** Downstream consequences of other forces should not appear on the driver list. If "escalating regional instability" is actually caused by "degree of external state sponsorship of armed groups," keep the latter and drop the former. The driver list should describe the causal levers, not the dependent variables.

**Non-obvious drivers are the analytic prize.** A driver set that consists entirely of the factors already dominating the policy debate has added little value. The Availability Heuristic will ensure that high-salience, recent, and vivid factors get onto any list. The analytical work is in protecting drivers that are structural, slow-moving, or uncomfortable — the forces that will shape the future but that are not currently prominent in reporting.

**Four to five drivers, not eight.** The book's guidance is firm: the number of mutually exclusive key drivers rarely exceeds four or five. If you have seven or eight candidate drivers, they are not all truly independent and fundamental. Meld, prioritize, and drop until the list is clean.

**Mutual exclusivity is a structural requirement, not an aspiration.** If two drivers on the list are strongly correlated — when one moves, the other tends to follow — they will collapse the scenario matrix. Two quadrants will be uninhabitable and the exercise will produce fewer distinct scenarios than intended. Test every driver pair for correlation before finalizing.

**The driver list is a hypothesis, not a verdict.** The scenario exercise itself will reveal whether the chosen drivers are the right ones. If, in building scenario narratives, a driver turns out not to produce meaningfully different worlds at its two extremes, it was not a genuine driver — revise and repeat. Treat the first driver list as a working hypothesis that the downstream exercise will validate or challenge.

---

## Relationship to other techniques

**Alternative Futures Analysis (§9.6)** and **Multiple Scenarios Generation (§9.7)** — The primary downstream consumers of the key driver list. KDG/KUF output feeds directly into these techniques. AFA requires exactly two drivers as its matrix axes; MSG uses three or more. The recommendation for which downstream technique is appropriate follows from the driver count (see Step 5).

**Key Assumptions Check (§7.1)** — The upstream input to KUF. Run a KAC on the current assessment first; its U-classified assumptions are the direct raw material for driver generation. Conversely, after completing the driver list, any driver whose spectrum runs from "current assumption holds" to "current assumption breaks" should be flagged back to the KAC as a red-priority uncertainty.

**Cluster Brainstorming (§6.2)** — The methodological foundation of KDG. The brainstorming technique used in Stage I is Cluster Brainstorming applied specifically to the driver-generation focal question.

**Simple Scenarios (§9.4)** and **Cone of Plausibility (§9.5)** — Simpler scenario techniques that also use key drivers. A KDG/KUF driver list can feed these lighter-weight methods when the resource requirements of a full AFA or MSG are not warranted.

**Indicators Generation, Validation, and Evaluation (§9.11)** — After completing a scenario exercise using these drivers, the indicators generated for each scenario should be validated against the driver set. An indicator that responds to a driver that is not on the final list may be monitoring noise rather than signal.

**What If? Analysis (§8.2.4)** — A driver that has been defined but whose extreme endpoints seem implausible is a natural input to What If? Analysis: posit that the extreme has already occurred and reason backward to understand how it came about. This can both validate the driver (if the backward-reasoning chain is credible) and populate a scenario narrative (the chain of events becomes the scenario backstory).
