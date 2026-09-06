---
name: alternative-futures-analysis
description: |
  Performs structured Alternative Futures Analysis (AFA) or Multiple Scenarios Generation (MSG) — the flagship Foresight SATs (Pherson & Heuer, §9.6–9.7). AFA uses two key drivers in a 2×2 matrix to produce four scenarios. MSG handles three or more drivers across multiple paired matrices, then selects the four most attention-deserving scenarios for decision makers.

  Trigger on: "alternative futures", "multiple scenarios", "scenario generation", "futures analysis", "run an AFA", "run an MSG", "what futures are possible", "build scenarios", "scenario planning", "how might this develop", "foresight analysis", "possible trajectories", "anticipate surprise", "what could happen over the next X years". Also trigger when a user asks how a complex situation might evolve over a time horizon, or when a KAC or What If? Analysis has surfaced trajectories needing systematic development.

  Accepts a typed focal question, pasted reporting, or uploaded document. Output can be inline chat, .docx, or HTML.
---

# Alternative Futures Analysis / Multiple Scenarios Generation

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §9.6 (Alternative Futures Analysis) and §9.7 (Multiple Scenarios Generation) — techniques developed by Pherson Associates, LLC and Royal Dutch Shell Company*

## Purpose

Alternative Futures Analysis (AFA) and Multiple Scenarios Generation (MSG) are Foresight techniques that prevent strategic surprise by forcing systematic consideration of how a situation might develop across a range of plausible futures. Rather than attempting to predict a single outcome, these techniques generate a set of mutually exclusive, attention-deserving scenarios that inform decisions, plans, and actions *today*.

Both techniques counteract five of the most consequential intuitive traps in estimative analysis:

- **Assuming a Single Solution** — thinking only one likely outcome is possible when several are plausible
- **Expecting Marginal Change** — focusing on a narrow range of alternatives representing incremental rather than radical change
- **Anchoring Effect** — treating the current trajectory as the default and adjusting insufficiently from it
- **Groupthink** — failing to generate genuinely divergent futures when experts share the same mental model
- **Lacking Sufficient Bins** — failing to consider a factor or trajectory because no prior analytic category exists for it

**AFA** is the right tool when two critical drivers dominate and analysts can agree on which two. It produces exactly four scenarios — the structurally optimal number for decision-maker consumption.

**MSG** is the right tool when three or more critical drivers shape the outcome. It generates many scenario combinations across multiple 2×2 matrices, then selects the four most compelling for development. MSG virtually eliminates the chance that events will unfold in a way the analyst never imagined.

The optimal output for decision makers is **four scenarios**, because:
- One scenario is a prediction that will not come true
- Two scenarios suggest an artificial binary choice
- Three introduce the Goldilocks effect (implying the "middle" is the safe bet)
- Five or more are too many for a decision maker to process cognitively

---

## When to use it

These techniques are most valuable when any of the following conditions are present:

- The situation is genuinely uncertain with multiple plausible trajectories over a 5–10 year horizon
- Decision makers are anchored on a single expected outcome and need to plan for alternatives
- A Key Assumptions Check has identified multiple fragile critical assumptions pointing in different directions
- Collection or policy gaps suggest the analyst community is not tracking key uncertainty drivers
- The focal question involves the interaction of multiple forces (political, economic, military, social, technological) that could combine in unpredictable ways
- Analysts or decision makers need to prepare contingency plans or identify collection requirements across a range of outcomes

> **Single analyst vs. group**: AFA and MSG ideally involve diverse teams, academics, and decision makers working over several days with a facilitator. This skill adapts the process for an individual analyst or small team working in a shorter timeframe — it preserves the intellectual rigor while compressing the logistics. Flag to the user if a full group exercise would be more appropriate given the stakes.

---

## Step 1: Ingest the input

Accept any of the following:

- **Focal question in chat** — e.g., "Run an AFA on the future of Taiwan Strait stability over the next decade" or "Generate scenarios for how the Venezuelan political situation could develop"
- **Pasted analysis or reporting** — Extract the analytic question, any stated assumptions about the future, and any drivers already identified
- **Uploaded document** — Read the file; identify the focal question and any prior scenario work
- **KAC or What If? output as input** — Fragile assumptions from a KAC are direct candidate drivers; What If? pathways can seed the scenario narratives

Frame the focal question as: *"What is the future of [X] over the next [time horizon]?"* If the time horizon is unstated, default to 5–10 years and note this assumption. A clear time horizon is essential — it prevents participants from extrapolating trivially from current trends.

---

## Step 2: Scope and route to the right technique

Ask a single short clarifying message covering:

1. **Time horizon**: What period should the scenarios cover? (5 years? 10 years? To a specific milestone?)
2. **Depth**: Quick scenario sketches (1–2 paragraphs per scenario) or full scenario narratives (with chronologies, implications, and full indicator sets)?
3. **Output format**: Inline in chat, Word (.docx), or HTML?

Additionally, ask or assess: **How many critical drivers does this problem have?**

- **Exactly 2 drivers that dominate and are independent** → use **Method A: Alternative Futures Analysis**
- **3 or more critical drivers, or driver count is unclear** → use **Method B: Multiple Scenarios Generation**

If the user has not identified drivers yet, proceed to Step 3 to generate them — the driver count will determine which method applies.

If the request makes scope obvious (e.g., "quick scan," tightly framed topic, follow-up to a KAC), proceed and note assumptions rather than asking.

---

## Step 3: Generate and select the key drivers

Key drivers are the forces, factors, or events most likely to shape the issue over the specified time horizon. They must be:

- **Genuinely uncertain** — not foregone conclusions or known quantities
- **Consequential** — directly determinative of the outcome in question
- **Independent** — not fully correlated with each other (correlated drivers collapse the matrix)
- **Non-obvious** — key drivers that are immediately apparent to any observer add little analytic value; the exercise should surface drivers that the community has underweighted

### How to generate candidate drivers

Use **STEMPLES+** as a stimulus checklist to ensure broad coverage:

| Category | Examples of driver types |
|----------|--------------------------|
| **S**ocial | demographic shifts, social cohesion, identity politics, migration |
| **T**echnological | emerging capabilities, disruption, adoption rates, cyber |
| **E**conomic | growth, sanctions, commodity prices, trade patterns, fiscal stress |
| **M**ilitary | force posture, capability gaps, doctrine, readiness |
| **P**olitical | leadership succession, regime stability, elections, coalition durability |
| **L**egal | international law, treaty compliance, sanctions regimes |
| **E**nvironmental | climate, resource scarcity, natural disasters |
| **S**ecurity | threat networks, alliance solidarity, intelligence capacity |
| **+** | Demographic, Religious, Psychological, Informational as applicable |

For each category, ask: *What force or factor in this domain is most uncertain and most consequential over the specified time horizon?*

### Additional driver-generation prompts

- What assumptions are embedded in the current analytic line about how this situation will develop? (Each fragile assumption may be a driver in disguise.)
- What single development would most surprise the analytic community — and what force would drive it?
- What factor is the decision-maker community currently *not* discussing that could prove decisive?
- What historical analogies suggest drivers that current analysis may be underweighting?

### Winnow to the critical drivers

From the candidate list, select the drivers that are **highest on both uncertainty and consequence**. Plot mentally or explicitly on an uncertainty × consequence matrix:

- **High uncertainty + high consequence** = candidate key driver ✓
- **Low uncertainty** (outcome largely known) = important context, not a driver — remove
- **Low consequence** (outcome matters little to the focal question) = background noise — remove

For AFA: converge on the **two** drivers with the highest combined uncertainty × consequence score that are also sufficiently independent. If analysts cannot agree on just two, use MSG instead.

For MSG: identify the **top 3–5** drivers. Document why each made the cut.

### Define the spectrum for each driver

For each selected driver, define the two extreme ends of its spectrum. These are not probabilities — they are the plausible outer boundaries of how the driver could resolve over the time horizon.

**Example (Taiwan Strait):**
- Driver 1 — *U.S. commitment to Taiwan*: [Strong and credible] ←→ [Weakened or ambiguous]
- Driver 2 — *PRC internal political stability*: [Consolidated and confident] ←→ [Fragmented and pressured]

Spectrum ends should be:
- **Concrete enough** to produce distinctly different worlds when combined with other drivers
- **Plausible** — not science fiction, but not inevitable either
- **Labeled memorably** — short descriptive phrases, not just "High/Low"

---

## Step 4: Construct the matrix (or matrices)

---

### Method A: Alternative Futures Analysis (2 drivers)

Draw a single 2×2 matrix:
- Driver 1 defines the **horizontal axis** (left extreme ←→ right extreme)
- Driver 2 defines the **vertical axis** (top extreme ↑ / bottom extreme ↓)

This produces **four quadrants**, each representing one scenario defined by a unique combination of the two driver extremes.

**Name each quadrant scenario** with a short, evocative label that captures the essence of that world — not a number. Good scenario names:
- Are internally consistent with what life in that quadrant would actually be like
- Are distinctive from each other (if two names sound similar, the scenarios may not be sufficiently different)
- Are memorable enough that a decision maker can refer to them by name

**Example (Cuba, from the book):**
- Drivers: "Effectiveness of Government" × "Strength of Civil Society"
- Quadrant names (illustrative): "Fortress Cuba," "Civic Bloom," "Managed Decay," "Open Transition"

---

### Method B: Multiple Scenarios Generation (3+ drivers)

With N drivers, you can form C(N,2) = N×(N−1)/2 paired matrices. For 3 drivers, this yields 3 matrices; for 4 drivers, 6 matrices; for 5 drivers, 10 matrices.

**Construct all paired matrices:**
For each pair of drivers, build a 2×2 matrix as in Method A. Name each of the four quadrant scenarios briefly.

This is the generative phase — don't evaluate or edit during this step. The goal is to populate the full space of possible future combinations. Some quadrant stories will be similar across matrices; that convergence is informative.

**Example (Iraq Insurgency, from the book):**
- Drivers: Role of neighboring states × Capability of Iraq's security forces × Political environment in Iraq
- Matrix 1: Neighboring states × Security forces → 4 scenarios
- Matrix 2: Neighboring states × Political environment → 4 scenarios
- Matrix 3: Security forces × Political environment → 4 scenarios
- Total: 12 raw scenario quadrants

For each quadrant, write one or two brief stories describing how events might unfold. Ask: *Given that Driver A resolves as [extreme 1] and Driver B resolves as [extreme 2], what does this world look like? What actors are ascendant? What is the security environment? What are the key dynamics?*

These stories need not be long — one or two concrete sentences per quadrant is sufficient in this phase. They will be developed further in Step 6.

---

## Step 5: Select the attention-deserving scenarios

From the full set of quadrant stories, select the **four** scenarios most deserving of decision-maker attention. Apply the five selection criteria from Pherson & Heuer:

| Criterion | Question to ask |
|-----------|-----------------|
| **Downside Risk** | Which scenario represents the worst plausible outcome? This becomes the "nightmare scenario" — it warrants a contingency plan. |
| **Mainline Assessment** | Which scenario is most consistent with current trends and best reflects the most likely trajectory? This is the baseline. |
| **New Opportunity** | Which scenario reveals a positive pathway that decision makers could actively shape or exploit? |
| **Emerging Trend** | Which scenario best captures a new dynamic or driver that was not previously on the decision maker's radar? |
| **Recognizable Anchor** | Which scenario resonates with the decision maker's current worldview — providing a credible entry point into the scenario set? |

**Selection rules:**
- The four selected scenarios should together span the full range of plausible futures, not cluster around the baseline
- Include at least one "nightmare scenario" — even if low probability, it represents a High Impact/Low Probability development the community would be worst served by ignoring
- Avoid selecting four scenarios that are all variations on one driver — ensure the set reflects different combinations
- If MSG generated convergent scenarios across multiple matrices, those convergent quadrants are often the most analytically significant (multiple driver combinations point to the same world)

**Document why each selected scenario was chosen** and why the others were set aside. Rejected scenarios that narrowly missed selection should be flagged as "watch list" scenarios worth monitoring.

---

## Step 6: Develop the scenario narratives

For each of the four selected scenarios, develop a full narrative covering:

### 6.1 — Scenario name and one-sentence summary
A memorable label and a crisp characterization of the world this scenario describes.

### 6.2 — Enabling conditions
What must be true at the outset for this scenario to be plausible? What assumptions does it rest on about current trends, actor behavior, or structural conditions? List 3–5 enabling conditions.

> *Challenge your own enabling conditions*: For each one, ask — is this actually supported by evidence, or is it an assumption we have not examined? Unexamined enabling conditions are often where scenarios fail.

### 6.3 — Narrative trajectory
A concise story — written in the present or future tense — of how events would unfold in this scenario. Include:
- What triggers or catalyzes the movement toward this scenario
- Key decision points or turning points along the way
- Which actors benefit and which are disadvantaged
- The state of the situation at the end of the time horizon

For formal products, include a **hypothetical chronology** of key dates and events. This forces internal consistency — a scenario timeline that requires too many simultaneous improbable developments needs to be revised.

Aim for 1–3 paragraphs for quick-scan products; 1–2 pages for full formal scenario narratives.

### 6.4 — Key implications
What are the 3–5 most significant consequences of this scenario for the decision maker's concerns? Distinguish:
- Immediate consequences (within 1–2 years of scenario onset)
- Second-order consequences (medium-term ripple effects)
- Strategic consequences (structural changes that would persist beyond the time horizon)

### 6.5 — Decision-maker actions
For each scenario, identify what a decision maker could do *today* to:
- **Prevent or mitigate** the scenario (if it is a negative outcome)
- **Enable or exploit** the scenario (if it is a positive opportunity)
- **Hedge** against the scenario developing without fully committing to counter it

This section is often the highest-value output for the decision maker — it converts futures analysis into an action agenda.

---

## Step 7: Generate and validate indicators

For each scenario, generate a list of **observable indicators** — signposts that would suggest events are beginning to unfold in the direction of that scenario.

### Indicator quality criteria

Each indicator must satisfy **all five** of the following:

1. **Observable** — an analyst could actually detect this from available collection or open sources (not a vague "sign of instability")
2. **Timely** — the indicator appears with enough lead time to allow decision-maker action before the scenario is fully realized
3. **Specific** — concrete enough to be actionable ("a bilateral defense agreement between X and Y is signed" rather than "increased military cooperation")
4. **Diagnostic** — where possible, the indicator should be discriminating: it should favor one scenario over the others, not appear equally under all scenarios
5. **Collectable** — the indicator is within the reach of existing collection capabilities or feasibly acquired; flag indicators that require new collection requirements

### Indicator categories

| Type | Description |
|------|-------------|
| **Precondition indicator** | Condition that must be in place for the scenario to develop at all — check these first |
| **Process indicator** | Observable step along the scenario trajectory — signals the scenario is in motion |
| **Tripwire indicator** | A single decisive observable that, if confirmed, would strongly commit analysts to that scenario |

### Indicator set requirements

- Develop at minimum **3–5 indicators per scenario**
- At least one indicator per scenario should be a **tripwire** — the single most decisive observable
- Cross-check: for each indicator, which other scenario(s) would it also support? Indicators that appear across all scenarios have low diagnostic power; flag them
- Assign a **collection source** to each indicator (HUMINT, SIGINT, OSINT, IMINT, financial, academic/open research, etc.)
- Flag which indicators are **currently being monitored** and which represent **new collection requirements**

### Indicator monitoring

After the exercise, establish a monitoring cadence. Report periodically on which scenario is most consistent with the observed indicator pattern — and update the scenario set if new drivers emerge that were not captured in the original analysis.

---

## Step 8: Report the conclusions

Structure the output as follows:

---

### Required output structure

**Header**: Focal question | Time horizon | Date | Analyst (if provided) | Method used (AFA or MSG)

**Executive Summary** (3–5 sentences)
A concise statement of the focal question, the method applied, the four scenarios selected, and the single most important finding (typically: which scenario the current trajectory appears to favor, and what the nightmare scenario implies for decision makers).

**Section 1 — Focal Question and Analytic Context**
The question being addressed and why it matters. State the time horizon explicitly. Briefly characterize the current analytic baseline — what the prevailing assessment says is most likely — so the scenarios can be understood as departures from or variations on it.

**Section 2 — Key Drivers**
For each driver selected:
- Driver label and brief description
- Spectrum: [Left/Low extreme] ←→ [Right/High extreme]
- Rationale for selection: why this driver meets the high uncertainty × high consequence test
- Key uncertainty: the single biggest unknown about how this driver will resolve

**Section 3 — The Four Scenarios**
For each scenario (apply the structure from Step 6):
- Scenario name and one-sentence summary
- Enabling conditions
- Narrative trajectory (with chronology for formal products)
- Key implications
- Decision-maker actions

Clearly label each scenario with its selection criterion (e.g., "Mainline," "Nightmare," "New Opportunity," "Emerging Trend," "Recognizable Anchor").

**Section 4 — Scenario Indicators**
A consolidated indicator table organized by scenario:

| Indicator | Scenario(s) | Type | Collection Source | Currently Monitored? | New Collection Req? |
|-----------|-------------|------|-------------------|----------------------|---------------------|

Flag tripwire indicators prominently. Flag indicators already showing positive for any scenario.

**Section 5 — Watch List** *(MSG only)*
A brief summary of the 2–3 scenarios that narrowly missed selection, with a note on what development would elevate them to the main set. Nightmare scenarios that were not selected for development should always appear here.

**Section 6 — Analytic Conclusions**
- Which scenario does the current trajectory most favor, and what would redirect it?
- Which scenario is most underweighted by the analytic community, and why does it deserve more attention?
- What are the most important collection gaps revealed by the indicator set?
- What analytic follow-on actions are recommended? (See relationship to other techniques below.)

---

## Step 9: Deliver in the requested format

**Inline chat**: Markdown. Use tables for drivers and indicators. Write scenario narratives as clearly labeled sections. Suitable for collaborative development and quick-iteration work.

**Word (.docx)**: Use the `docx` skill. Formatted report with proper headings, styled indicator table, scenario narratives in clearly delineated sections, and a one-paragraph executive summary at the top. Include 2×2 matrix diagrams as ASCII art or text description; note that formal products benefit from actual matrix graphics. Appropriate for formal analytic products, briefing support, and distribution to decision makers.

**HTML**: Standalone file with a structured indicator table (filterable by scenario and collection source), scenario narratives, and a visual representation of the 2×2 matrix structure. Good for team collaborative review or web publication.

> ⚠️ **Sensitive scenarios**: Scenario narratives that detail specific vulnerabilities, attack vectors, or adversary courses of action may warrant restricted distribution. Flag this prominently and recommend limiting distribution to principals only if applicable.

---

## Analyst principles

**Scenarios are not predictions — they are preparation.** A scenario that does not occur is not a failed scenario. A decision maker who prepared for four plausible futures and faced one of them is in a far stronger position than one who predicted a single outcome and was surprised by a variant. Frame the product accordingly.

**Driver selection determines everything.** The quality of the scenario set is a direct function of the quality of driver selection. Spend disproportionate time here. Drivers that are correlated, that are actually known quantities, or that are low-consequence will produce scenarios that collapse into each other or that miss the analytic question entirely.

**Four scenarios, not three and not five.** The book's guidance on this is firm and grounded in cognitive science. Three invites the Goldilocks fallacy; five exceeds what decision makers can hold simultaneously. If you find yourself with five compelling scenarios, one of them is redundant or two of them can be combined.

**Diversity defeats groupthink.** The scenarios most likely to be suppressed by groupthink are precisely the ones most analytically valuable. The nightmare scenario and the "wild card" scenario deserve a slot in the set not because they are likely, but because they represent the territory the community has collectively agreed not to look at. Disciplined scenario analysis forces that territory into view.

**Indicators already showing are the most urgent finding.** Build the indicator set, then immediately check which indicators are already positive. If the nightmare scenario has two of five indicators currently showing, that scenario is no longer negligible — escalate this finding.

**The narrative must be internally consistent.** A scenario narrative that requires three simultaneous low-probability events at the same time period is not a credible scenario — it is wishful or fearful thinking dressed as analysis. Test each narrative by asking: *What would have to happen between now and [end of time horizon] for this to be true?* If the chain of events is implausible, revise the scenario or discard it.

**Challenge your own enabling conditions.** The enabling conditions for each scenario are often unexamined assumptions in disguise. Run a quick Key Assumptions Check on them before finalizing the narratives. This is where scenarios get caught by their own hidden premises.

---

## Relationship to other techniques

**Key Drivers Generation™ (§9.1)** — The ideal predecessor. Use Key Drivers Generation™ to systematically generate and prioritize the candidate drivers before selecting the two (AFA) or three-to-five (MSG) that define the matrix. If driver selection feels contested or arbitrary, run Key Drivers Generation™ first.

**Key Uncertainties Finder™ (§9.2)** — A complementary driver-generation tool. Identifies the highest-uncertainty factors in the problem space. Combine with Key Drivers Generation™ for a cross-validated driver list.

**Key Assumptions Check (§7.1)** — Run a KAC on the current analytic assessment before starting the futures exercise. Fragile assumptions identified by the KAC are often the best source of candidate drivers. Conversely, the enabling conditions for each scenario developed in AFA/MSG should themselves be KAC-tested.

**What If? Analysis (§8.2.4)** — What If? Analysis is scenarios analysis in reverse: it posits an endpoint and reasons backward. Use What If? to develop the back story for a nightmare scenario that the MSG exercise has identified but that the community resists as implausible. The two techniques reinforce each other — MSG identifies which scenarios deserve attention; What If? explains how an unlikely one could actually come about.

**Multiple Hypothesis Generation (§7.4)** — MHG generates hypotheses about *current* or *recent* events; AFA/MSG generate scenarios about *future* developments. However, the four scenarios produced by AFA/MSG can be treated as a hypothesis set and fed directly into ACH when the analytic question is whether a *current trend* is on a trajectory toward one of the scenarios.

**Analysis of Competing Hypotheses (§7.6)** — When the scenario set is complete, ACH can be applied to ask: *Given the current evidence body, which of the four scenarios is most consistent?* Treat each scenario as a hypothesis and the current observable indicators as the evidence list.

**Indicators Generation, Validation, and Evaluation (§9.11)** — The indicator sets produced in Step 7 should feed directly into a formal indicator monitoring regime. AFA/MSG is one of the most productive generators of early-warning indicators because it develops them for futures the community considers unlikely and might not otherwise monitor.

**Premortem Analysis (§8.2.2)** — After completing the scenario narratives, apply Premortem Analysis to the mainline scenario: "Assume the mainline scenario is wrong — what happened instead?" The Premortem product will often confirm which of the alternative scenarios is the most credible challenger.

**Counterfactual Reasoning (§9.9)** — Counterfactual Reasoning asks how history could have been different and what that implies for the future. The scenarios developed in AFA/MSG can seed Counterfactual Reasoning exercises for particularly high-stakes scenarios — especially the nightmare scenario.

**Morphological Analysis (§9.8)** — MSG is a specific application of Morphological Analysis. When the number of drivers exceeds five or the combinations exceed what paired 2×2 matrices can capture, the full Morphological Analysis method (with computer assistance) is the appropriate escalation path.
