---
name: what-if-analysis
description: |
  Performs a structured What If? Analysis — a core Reframing SAT (Pherson & Heuer §8.2.4). Use when an analyst needs to challenge a prevailing mental model by positing that a surprising or unlikely event has already happened, then working backwards ("backwards thinking") to explain how it came about and what follows.

  Trigger on: "what if", "what if analysis", "backwards thinking", "what would have to be true for X", "how could this happen", "posit a scenario", "challenge conventional wisdom", "contingency analysis", "what if I'm wrong", "surprise scenario". Also trigger when a user asks what could go wrong with a current estimate, when a Key Assumptions Check has flagged a fragile critical assumption, or when groupthink may be suppressing a viable alternative outcome.

  Accepts a typed question, pasted reporting, or uploaded document. Output can be inline chat, Word .docx, or HTML.
---

# What If? Analysis

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §8.2.4 — based on Randolph H. Pherson, "What If? Analysis," Handbook of Analytic Tools and Techniques, 5th ed. (Tysons, VA: Pherson Associates, 2019)*

## Purpose

What If? Analysis challenges entrenched mental models and warns decision makers about events that seem unlikely but would have major consequences if they occurred. The technique does this by reframing the question: instead of asking *"Will X happen?"* — a framing that tends to trigger confirmation of the prevailing view — it stipulates *"X has just happened"* and asks analysts to explain how.

This reframe forces the mind to discover pathways it would otherwise suppress. The technique serves three distinct functions:

1. **Warning** — Prepares analysts and decision makers to recognize early signals of a scenario that the prevailing view has discounted.
2. **Contingency planning** — Gives decision makers a list of actions they could take now to prevent, mitigate, or leverage the posited development.
3. **Tactful challenge** — Provides a politically acceptable way to question a prevailing assessment without directly saying it is wrong.

**Critical distinction from High Impact/Low Probability (Hi-Lo) Analysis**: Hi-Lo Analysis starts from new or anomalous information already in hand and then projects *forward* to ask what would happen. What If? Analysis does not require new triggering information — it posits an endpoint and reasons *backward*. Both deal with unlikely events; only What If? uses backwards thinking.

---

## When to use it

What If? Analysis is most valuable when any of the following conditions are present:

- A mental model is firmly ingrained in the analytic or client community that a particular event will not occur.
- The issue is contentious and stakeholders are too focused on whether the event will happen to plan for it if it does.
- An analyst suspects the community is suppressing a viable alternative outcome due to Groupthink, anchoring on a previous assessment, or political pressure.
- A Key Assumptions Check has identified a critical assumption that is load-bearing but questionable. The natural What If? prompt: "What if this assumption is wrong?"
- An adversary or competitor with motive, opportunity, and capability to achieve a dramatic outcome has not been receiving adequate analytic attention.

> *"When analysts are too cautious in estimative judgments on threats, they brook blame for failure to warn. When too aggressive in issuing warnings, they brook criticism for 'crying wolf.'"* — Jack Davis, "Improving CIA Analytic Performance: Strategic Warning" (2002)

What If? Analysis gives analysts a disciplined, documented way to issue a warning without asserting that the event is probable.

---

## Step 1: Ingest the input

Accept any of these forms:

- **Problem statement in chat** — e.g., "Run a What If? on a successful attack on the power grid" or "What if the ceasefire collapses next month?"
- **Pasted analysis or raw reporting** — Extract the prevailing assessment and identify which aspect of it to challenge
- **Uploaded document** — Read the file and identify the key estimate, the embedded assumption to challenge, or the scenario of concern
- **KAC output as input** — If a Key Assumptions Check has been run and flagged a critical fragile assumption, the What If? scenario should be: "Assume [that assumption] is wrong. What now?"

Frame the posited event as a **specific, dated, high-impact development** — not a vague possibility. Imprecise posited events produce imprecise back stories.

---

## Step 2: Scope the analysis

Ask a single short clarifying message covering:

1. **The posited event**: Is the scenario clear enough to proceed, or does it need sharpening?
2. **Valence**: Is this a *negative* scenario (prevent/mitigate) or a *positive* opportunity (leverage)?
3. **Output format**: Inline in chat (fast), Word (.docx, formal product), or HTML (structured deliverable)?
4. **Depth**: Quick scan (1–2 pathways, key indicators only) or full analysis (3–4 pathways, full indicator set, consequence assessment)?

If the request makes the answers obvious — "quick look", a tightly framed scenario, or a follow-up to a prior KAC — skip asking and proceed, noting your assumptions.

---

## Step 3: State the posited event precisely

Phrase the scenario as if it has already occurred. The classical format is a news headline or short lead:

> *"The [source] reported [date] that [specific development]."*

**Examples:**
- *"The Washington Post reported this morning that the government of [country X] has announced a surprise unilateral ceasefire and invited international observers."*
- *"Reuters reported that a coordinated cyberattack has caused a 72-hour blackout across three northeastern U.S. power grid sectors."*
- *"The Wall Street Journal reported that [adversary firm] has acquired [target company], giving it a dominant position in the rare earth supply chain."*

Be precise about **what** happened, **who** is affected, and **how significant** the impact is. Vague scenarios produce unproductive back stories. Define the event tightly enough that it is unambiguous whether a proposed pathway actually leads there.

**Challenge your own framing before proceeding**: Is this the right event to posit? Is it specific enough? Is it framed so that decision makers would recognize its significance? Revise if not.

---

## Step 4: Generate the pathways (back stories)

Develop multiple chains of argument explaining how the posited event could have come about. Work backward from the event to today. Each pathway is a sequence of plausible steps — a "back story."

### Guidance

- **Aim for 2–4 distinct pathways.** A single pathway is inadequate; it anchors the analysis on one causal model. More than four risks losing rigor.
- **Each pathway must be internally coherent.** Every step must logically follow from the previous one. If a step requires a large unexplained leap, either flesh it out or split the pathway.
- **Label each pathway clearly** — not "Pathway 1" but a descriptive name that captures the causal logic, e.g., "Elite coup enabled by economic collapse," "Insider-assisted infrastructure attack," "Diplomatic miscalculation cascades."
- **Work backwards**: Start at the posited event, then ask "What had to happen immediately before this?" Continue back toward the present day.
- **Consider different trigger types** for the pathways: internal political failure, external shock, deliberate adversary action, accident or miscalculation, structural vulnerability exploitation.
- **Incorporate existing knowledge**: Known actor capabilities, historical precedents, observed trends, and structural conditions should inform which steps in a pathway are feasible.
- **Assign a relative plausibility** to each pathway (HIGH / MEDIUM / LOW) based on how many enabling conditions are already in place vs. how many large steps must occur. This is not a probability estimate — it is a feasibility assessment.

> *Tip: If pathway generation is producing only obvious or similar pathways, try Reversing Assumptions (§9.3): take each key assumption embedded in the current estimate and flip it. Each reversal can seed a distinct pathway.*

After drafting the pathways, review the set: Are there any plausible pathways that are politically uncomfortable but analytically valid? Those are the ones most likely to have been suppressed by groupthink — include them.

---

## Step 5: Identify indicators for each pathway

For each pathway, generate a list of observable indicators — things that, if detected, would signal that events are starting to unfold in the direction of that pathway.

### Indicator types

| Type | Description |
|------|-------------|
| **Precondition indicators** | Conditions that must be in place for the pathway to be viable (check these first) |
| **Process indicators** | Observable steps along the pathway that signal it is unfolding |
| **Tripwire indicators** | Single decisive observations that would confirm the pathway is active |

### Indicator quality rules
- Each indicator must be **observable** — something an analyst could actually detect from available collection or open sources, not a vague "signs of instability"
- Each indicator must be **pathway-discriminating where possible** — if an indicator would appear under *all* pathways, it adds little diagnostic value
- Indicators should be **specific** enough to be actionable: "a bilateral arms agreement between X and Y is announced" rather than "increased military cooperation"

Assign each indicator a **collection source** (HUMINT, SIGINT, OSINT, IMINT, academic/open research, financial indicators, etc.) and flag whether the indicator is currently being monitored.

After building the indicator list, flag any that are **already showing**: if indicators for a low-probability pathway are already positive, that pathway deserves elevated attention regardless of its assigned plausibility.

---

## Step 6: Prioritize the pathways

Not all pathways warrant equal analytic effort or decision-maker attention. Prioritize by combining two factors:

1. **Feasibility** — How many of the enabling steps are already in place? How hard would it be for the relevant actor(s) to execute the remaining steps?
2. **Significance** — If this pathway is how the event comes about, how severe are the consequences? How much warning time would exist?

Rank pathways HIGH / MEDIUM / LOW for both factors and identify the **priority pathways** — those that are at least moderately feasible *and* highly significant. These are the pathways decision makers should plan against.

**Also flag**:
- The pathway that is *most likely to be overlooked* by the prevailing analytic community (often the most significant finding)
- Any pathway where current collection is absent or inadequate to detect it unfolding

---

## Step 7: Assess consequences and recommended actions

For the priority pathways, develop a brief consequence assessment:

**Negative scenarios:**
- What immediate damage or disruption would result?
- How difficult would it be to reverse or mitigate?
- What are the second- and third-order effects?
- What actions could a decision maker take **now** to reduce the probability or impact?

**Positive scenarios (opportunity posits):**
- What is the potential upside if the development occurs?
- What conditions would have to hold for it to be sustained?
- What actions could a decision maker take **now** to increase the probability or exploit the opportunity?

The goal of this section is not prediction — it is **preparation**. A decision maker who has thought through the What If? scenario is far better positioned to act decisively if early indicators begin to appear.

---

## Step 8: Report the conclusions

Structure the output as follows:

---

### Required output structure

**Header**: Analytic question | Date | Analyst (if provided)

**Section 1 — The Posited Scenario**
The event stated in headline format as if it has already occurred. One short paragraph establishing why this scenario matters and what mental model it challenges.

**Section 2 — Pathways Analysis (Back Stories)**
For each pathway (2–4 total):
- **Pathway label** — descriptive name
- **Causal chain** — step-by-step account from present to posited event, working backwards (then presented in forward narrative order for readability)
- **Enabling conditions** — what must already be true for this pathway to be feasible
- **Relative plausibility** — HIGH / MEDIUM / LOW with brief rationale
- **Key uncertainties** — the single biggest assumption or unknown that could invalidate this pathway

**Section 3 — Indicators**
A consolidated indicator table organized by pathway, flagging:
- Indicator description
- Pathway(s) it applies to
- Collection source
- Current status (observed / not observed / unknown)
- Monitoring priority (HIGH / MEDIUM / LOW)

**Section 4 — Priority Assessment**
Ranking of pathways by feasibility × significance. Explicit identification of which pathways deserve immediate collection or monitoring attention and which are worth flagging to decision makers.

**Section 5 — Consequences and Decision-Maker Actions**
For priority pathways: damage assessment for negative scenarios or opportunity assessment for positive scenarios, and a short list of actions the decision maker could take now.

**Section 6 — Analytic Conclusions**
A direct statement of the analytic value of this What If? exercise: What does this analysis reveal about the fragility of the current estimate? What is being monitored that previously was not? What should be escalated?

---

## Step 9: Deliver in the requested format

**Inline chat**: Markdown. Use tables for the indicator section. Suitable for quick analysis and conversational review.

**Word (.docx)**: Use the `docx` skill. Formatted report with proper headings, styled indicator table, and a one-paragraph executive summary at the top. Appropriate for formal analytic products, peer review, and distribution to decision makers.

**HTML**: Standalone file with a structured indicator table (filterable by pathway and monitoring priority). Good for collaborative review.

For any formal product distributed to decision makers, .docx is recommended.

> ⚠️ **Handling sensitive scenarios**: What If? analyses that identify specific attack vectors, exploit methods, or adversary vulnerabilities often warrant restricted distribution. If the scenario describes a vulnerability an adversary could exploit, flag this prominently and recommend limiting distribution to principals only.

---

## Analyst principles

**The scenario has already happened — commit to it.** The power of the technique depends entirely on this mental shift. If the analyst is hedging ("...but this probably won't happen..."), the reframe has failed. Work from the endpoint backwards with full conviction that the event has occurred.

**Multiple pathways are not optional.** A single pathway is just a story. Multiple pathways reveal which enabling conditions are *common across all of them* — those conditions are the highest-priority items for monitoring regardless of which pathway is ultimately correct.

**Indicators that are already positive are the most urgent finding.** If you build an indicator set for a low-probability pathway and two of the five indicators are already green, the scenario is no longer low-probability for practical purposes. Flag this immediately.

**The technique is not a probability estimate.** What If? Analysis is about *possibility and preparation*, not about revising the probability of the posited event. The output is: "Here is how it could happen, here is what to watch for, and here is what to do about it." It is explicitly not: "This will now happen."

**Challenge your own pathway selection.** After generating 2–4 pathways, ask: which pathways have been left out because they are politically uncomfortable, embarrassing to the current assessment, or imply collection failure? Those omitted pathways are often the most analytically valuable.

**The "NYT headline" discipline keeps the scenario grounded.** If you cannot write a crisp, specific, plausible news headline stating that the event has occurred, the scenario is not yet well-defined enough to analyze.

---

## Relationship to other techniques

**Key Assumptions Check (KAC, §7.1)** — The natural predecessor. When KAC identifies a critical fragile assumption, What If? Analysis examines what happens if that assumption is wrong. Run KAC first; use its most fragile assumptions as inputs to frame the What If? scenario.

**High Impact/Low Probability Analysis (§8.2.5)** — The closest relative, but fundamentally different. Hi-Lo starts from anomalous information already in hand and projects *forward*. What If? requires no triggering information — it posits an endpoint and reasons *backward*. Use Hi-Lo when you have an anomaly that demands explanation; use What If? when you need to challenge a prevailing view that dismisses an outcome as impossible.

**Analysis of Competing Hypotheses (ACH, §7.6)** — Use ACH when multiple explanations for a *current* situation are in competition. Use What If? when the goal is to challenge *certainty* about a *future* outcome. The two can be sequenced: ACH to determine the current state, What If? to challenge the estimate about where things are heading.

**Premortem Analysis (§8.2.6)** — Similar reframing logic: "Assume we were wrong — how did that happen?" Premortem focuses specifically on an analyst's *own* prior assessment; What If? focuses on any specific future development the community has discounted. Premortem is the more introspective tool; What If? is the more externally focused warning tool.

**Indicators Generation, Validation, and Evaluation (§9.11)** — The indicators produced in Step 5 should feed directly into a formal indicators monitoring regime. What If? Analysis is one of the best generators of early-warning indicators precisely because it develops them for scenarios the community considers unlikely and therefore might otherwise not monitor.

**Counterfactual Reasoning (§9.9)** — What If? Analysis is sometimes described as the first stage of Counterfactual Reasoning: develop the back story (What If? Analysis) and then explore the full implications of that alternate history (Counterfactual Reasoning). For a quick-turnaround warning product, What If? alone is usually sufficient.
