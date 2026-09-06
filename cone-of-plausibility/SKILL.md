---
name: cone-of-plausibility
description: |
  Performs Cone of Plausibility — Foresight SAT (Pherson & Heuer §9.5). Uses key drivers and assumptions to bound plausible futures: scenarios inside the cone are plausible; wild cards fall outside. Faster than AFA — builds a baseline first, then modifies fragile assumptions to generate alternatives. Mandatory outputs: baseline, downside risk, opportunities, and wild card. Effective for strategic warning.

  Trigger on: "cone of plausibility", "run a cone", "bound the scenarios", "baseline and alternatives", "strategic warning scenarios", "how might X evolve", "plausible futures", "what's inside the cone", "what futures should we plan for". Also trigger for CTI foresight: "how might this APT evolve", "where is ransomware headed", "scenarios for [threat actor] capability development". Use when foresight is needed but time or group size preclude full AFA, or when bounding plausible space matters.

  Input: typed topic, pasted reporting, or uploaded doc. Output: inline chat, .docx, or HTML.
---

# Cone of Plausibility

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §9.5 — widely used in Canadian and UK intelligence communities*

## Purpose

Cone of Plausibility is a structured foresight technique that generates a range of plausible future scenarios by anchoring each scenario to specific assumptions about how key drivers will behave. It is explicitly a **bounding exercise**: the cone's shape communicates that the further out in time you project, the wider the range of plausible outcomes. Futures inside the cone are plausible given the stated drivers and assumptions; wild cards fall outside the cone and are marked as High Impact/Low Probability scenarios.

The technique is distinct from Alternative Futures Analysis (AFA) in two critical ways:

- **Faster and lighter.** It does not require a 2×2 matrix or a facilitator-led group exercise. A single analyst or small team can complete it in hours.
- **Assumption-first.** Rather than defining driver spectra and combining them freely, the analyst makes an explicit **one assumption per driver** commitment. Alternative scenarios are then produced by challenging those assumptions — especially the fragile ones.

This makes Cone of Plausibility particularly powerful for **strategic warning**: it forces the analyst to articulate exactly what would have to be false about their current model to produce a very different future.

---

## When to use it

Cone of Plausibility is the right choice when:

- The analytic question requires foresight but time or resources preclude a full AFA/MSG group exercise
- The analyst needs to **bound the plausible space** (what futures are within the realm of reason, what falls outside it) and communicate that boundary to a decision maker
- The current trajectory has a clear **baseline** that most analysts agree on, and the value is in articulating divergence from it
- **Strategic warning** is the primary purpose — the exercise needs to produce one or more watchable wild-card scenarios
- A CTI analyst needs to forecast how a threat actor, campaign, or vulnerability ecosystem might evolve over the next 6–24 months
- The user wants to challenge a prevailing assessment by showing what happens when the most stable assumption turns out to be wrong

> **AFA or Cone?** If the problem involves three or more roughly equal competing drivers, and a group is available, use AFA or MSG. Use Cone when there is a clear current trajectory, when time is short, or when the goal is explicitly to warn about plausible negative divergences from the baseline.

---

## Step 1: Ingest and frame the focal question

Accept any of the following inputs:

- **Typed topic or question** — e.g., "How might Volt Typhoon's pre-positioning capabilities evolve over the next two years?" or "What scenarios exist for ransomware-as-a-service economics over the next 18 months?"
- **Pasted reporting or assessment** — Extract the analytic baseline, any stated assumptions, and any drivers already identified
- **Uploaded document** — Read the file; identify the current trajectory and key uncertainties

Frame the focal question as: *"What will [X] look like over the next [time horizon]?"* Common formulations in CTI:

- *"What will [threat actor]'s capabilities and targeting priorities look like in 18 months?"*
- *"What will the ransomware ecosystem look like in 2 years if current trends continue — and what would change that picture?"*
- *"How might [active campaign or vulnerability] develop over the next 90 days?"*

If the time horizon is not stated, default to 12–24 months for CTI topics and 3–5 years for geopolitical/strategic topics. State the assumption explicitly.

---

## Step 2: Identify 4–6 key drivers

Key drivers are the forces or factors most likely to shape the outcome over the time horizon. Write each as a **neutral, enduring label** valid throughout the period — not a directional prediction.

Good driver framing:
- ✅ "Government regulatory posture toward ransomware payments"
- ✅ "Threat actor access to zero-day vulnerabilities"
- ❌ "Increasing government regulation" (already directional)
- ❌ "The economy is declining" (already a prediction)

The technique works best with **4–6 drivers**. Fewer than four tends to produce an underdetermined baseline; more than six makes assumption-tracking unwieldy.

Use **STEMPLES+** to avoid blind spots:

| Category | CTI-relevant driver examples |
|----------|------------------------------|
| **S**ocial | Defender community trust, threat sharing norms, public tolerance for cyber disruption |
| **T**echnological | AI-assisted attack tooling, detection capability maturity, cloud adoption rates |
| **E**conomic | Criminal ecosystem profitability, victim payment rates, insurance coverage of cyber losses |
| **M**ilitary | Nation-state cyber posture, offensive TTPs, escalation thresholds |
| **P**olitical | Attribution willingness, international norms, domestic legal frameworks |
| **L**egal | Sanctions regimes, payment prohibitions, liability for insecure products |
| **E**nvironmental | Critical infrastructure dependencies, supply chain fragility |
| **S**ecurity | Defender capability, patch velocity, SOC maturity across target sectors |

For each candidate driver, ask: *Is this force genuinely uncertain over the time horizon, and does its direction materially change the outcome?* If the answer is "mostly settled" or "won't matter much," demote it to context and move on.

---

## Step 3: Generate one assumption per driver

For each driver, make a **single specific assumption** about how that driver will behave over the assessment period. This is the most consequential step — the baseline scenario is directly derived from these assumptions.

Rules for good assumptions:

- **Specific and falsifiable.** "Government regulatory enforcement will remain moderate — between 10–15 major sanctions actions per year — without a blanket payment ban" is useful. "Government regulation will stay about the same" is not.
- **One assumption per driver.** The temptation is to hedge; resist it. The discipline of single-point assumptions is what makes Cone of Plausibility work — alternatives are produced by changing these assumptions, so vague assumptions collapse the alternative space.
- **Reflect current trajectory, not preference.** The baseline assumption set should represent the most likely continuation of current conditions, not a best-case or worst-case outcome.

After generating assumptions, **mark each for fragility**:

- 🟢 **Stable** — strong evidence this assumption will hold; would take a major disruption to overturn
- 🟡 **Uncertain** — plausible but has meaningful competing evidence or depends on actors behaving consistently
- 🔴 **Fragile** — weakly supported, already showing signs of stress, or depends on a single actor or event

Fragile assumptions are the primary material for alternative scenarios. Stable assumptions are the raw material for wild cards.

---

## Step 4: Build the baseline scenario

Synthesize the driver list and assumptions into a **baseline scenario narrative** — a story written as if the future has already come to pass, describing how things unfolded given that all baseline assumptions held.

The baseline should:

- **Project the current trajectory forward** without assuming either the best or worst case
- **Reference each driver** — the narrative should explicitly show how each driver played out
- **Name the world** — give the baseline a short, evocative label (e.g., "Steady State," "The Persistent Threat," "Managed Decline")
- **Cover**: What happened? Who was affected? What is the state of the situation at the end of the time horizon?

The baseline is the center of the cone — the scenario most consistent with current evidence and trends. All other scenarios are departures from it.

---

## Step 5: Generate alternative scenarios by modifying assumptions

Construct **1–3 alternative scenarios**, each produced by changing one or more baseline assumptions — starting with the **most fragile** ones.

### How to select which assumptions to change

Start by examining your 🔴 Fragile assumptions. Ask: *If this assumption proved wrong — in either direction — what world would result?* This is essentially a What If? exercise applied to each fragile assumption.

For each alternative, document:
1. **Which assumption(s) changed** and in what direction
2. **Why this change is plausible** — what evidence or dynamics could drive it
3. **The cascade**: How does changing this assumption alter the other assumptions on the list?
4. **The resulting narrative** — written as a future that has come to pass

### Required alternative scenario types

Your alternative set should include **at least** these two:

**1. Downside risk scenario** — The assumption that deteriorates most significantly. For CTI: threat actor capability accelerates, defender posture weakens, victim compliance increases, or a geopolitical catalyst removes inhibitions on destructive attacks. This scenario defines the bottom of the plausible cone.

**2. Opportunities scenario** — At least one scenario should show a positive divergence from the baseline. For CTI: coordinated law enforcement disrupts the criminal ecosystem, AI-powered defenses outpace AI-powered attacks, or international norms shift toward meaningful consequences. Decision makers often need to see this scenario to know what they could achieve if they acted.

If a third alternative is developed, make it the scenario that **most challenges the prevailing analytic consensus** — the scenario the community has implicitly agreed not to consider seriously.

---

## Step 6: Generate the wild card

Produce one **wild card scenario** by taking the **most stable (🟢) assumption** — the one analysts consider virtually certain to hold — and radically overturning it.

The wild card has three defining characteristics:

1. **It falls outside the cone** — it is not "plausible" in the conventional sense, but it is possible
2. **Its impact would be severe** — if it occurred, it would change the entire analytic picture
3. **It has observable precursors** — even if improbable, there should be some collection indicators that would warn of it developing

The wild card is not developed in the same depth as alternative scenarios. Capture it in a short block:

- **Label**: A memorable name (e.g., "Black Ice," "Silent Handoff")
- **Overturned assumption**: State explicitly which stable assumption was inverted
- **Scenario sketch**: 2–4 sentences on what this world looks like
- **Key indicator**: One observable that would signal this wild card is developing
- **Why it matters**: One sentence on the implication for decision makers if it materializes

> **Wild card ≠ wild guess.** The wild card should be the scenario that genuinely shocks the analyst community because it violates a deeply held assumption — not a random improbable event. Its value lies in sensitizing decision makers to a specific structural vulnerability they are currently ignoring.

---

## Step 7: Assess and communicate

After completing the full scenario set, perform a final analyst check before reporting:

### Scenario consistency check

For each alternative and the wild card:
- Does the narrative internally cohere? (A scenario that requires three simultaneous low-probability developments in the same quarter is a sign the scenario needs revision)
- Does changing one assumption actually cascade plausibly to the narrative described? (If the assumptions are barely changed but the narrative is radically different, the causal logic needs to be shown)
- Are the scenarios **distinct from each other**? (If two scenarios look roughly the same, collapse them or differentiate more sharply)

### Cone placement check

Rank the scenarios on an informal plausibility spectrum:
1. **Baseline** — most likely, center of cone
2. **Alternatives** — plausible departures, inside cone
3. **Wild card** — possible but outside plausible boundary, outside cone

If an alternative scenario feels nearly as improbable as the wild card, either elevate the wild card or downgrade the alternative to the wild card slot.

### Decision implications

For each scenario (including the wild card), answer briefly:
- What actions available *today* would prepare the decision maker for this future?
- What single collection requirement would provide the earliest warning that this scenario is developing?

---

## Step 8: Deliver in the requested format

**Inline chat**: Markdown. Use a structured section per scenario. Show the driver/assumption table first, then the baseline, then alternatives, then wild card in a clearly marked "outside the cone" section.

**Word (.docx)**: Use the `docx` skill. Include: executive summary, driver/assumption table, cone diagram (described as text with clear labeling of inside/outside), scenario narratives with decision implications, and a wild card box set apart visually.

**HTML**: Standalone file with a visual SVG cone diagram showing scenarios plotted by plausibility and time. Baseline at center, alternatives fanning out inside the cone, wild card labeled outside the cone boundary. Scenario narratives as expandable sections. **Always use plain HTML/CSS/JavaScript — no React frameworks.**

### HTML cone diagram guidance

When producing HTML output, draw the cone as an SVG element:
- Horizontal axis = time (from "Present" to end of time horizon)
- Vertical axis = spread of possible futures
- Two diverging lines forming the cone boundary
- Baseline plotted as a dashed center line
- Alternative scenarios as labeled points or arcs inside the cone
- Wild card labeled outside/beyond the cone boundary, with a dotted connection
- Color convention: baseline = blue, alternatives = amber/green, wild card = red

---

## Output structure

```
FOCAL QUESTION
Time horizon | Date | Analyst (if provided)

EXECUTIVE SUMMARY (3-5 sentences)
Focal question, key drivers, baseline assessment, most important divergence risk, wild card flag.

SECTION 1 — Drivers and Assumptions
Table: Driver | Assumption | Stability (🟢🟡🔴)

SECTION 2 — Baseline Scenario
Label | Narrative (2-4 paragraphs)
All baseline assumptions held. Describes most likely future.

SECTION 3 — Alternative Scenarios
For each alternative:
  Label
  Changed assumption(s) and rationale
  Narrative (2-3 paragraphs)
  Key decision implication
  Lead collection indicator

[Clearly mark: INSIDE THE CONE]

SECTION 4 — Wild Card [OUTSIDE THE CONE]
Label
Overturned stable assumption
Scenario sketch (2-4 sentences)
Key indicator
Why it matters

SECTION 5 — Analyst Observations
- Which scenario does current evidence favor?
- Which assumption, if wrong, would most rapidly shift the picture?
- Most important collection gaps revealed
```

---

## Analyst principles

**The baseline is not a prediction — it is a reference point.** The baseline scenario is the scenario most consistent with current trends, but "most consistent" is not the same as "will definitely happen." Frame the baseline as the center of a distribution, not a forecast.

**Assumption fragility determines analytic priority.** The 🔴 Fragile assumptions are where the intelligence collection effort should be concentrated. If an assumption is fragile and its failure would shift you from the baseline to a downside scenario, that fragile assumption is a collection requirement waiting to be named.

**The wild card must surprise, or it isn't a wild card.** If the analyst doesn't feel at least slightly uncomfortable writing it — because it violates something the community has treated as settled — it probably isn't radical enough. The discomfort is the signal that it belongs outside the cone.

**One assumption per driver is a discipline, not a limitation.** Hedging ("the economy will be between 1–5% growth") removes the falsifiability that makes scenario comparison meaningful. Commit to a specific assumption, flag the fragility level, and let the alternative scenarios show what happens if you were wrong.

**Include the opportunities scenario.** Intelligence analysis has a well-documented negativity bias — the downside risk scenario is always easier to write. Force yourself to develop the positive alternative. Decision makers need it; it shows what is achievable, not just what is to be feared.

**The cone gets wider over time — account for it.** Assumptions that seem solid for a 6-month horizon are significantly more fragile at a 24-month horizon. When calibrating fragility, always ask: *solid at what time scale?* A 🟢 stable assumption for 3 months may be 🟡 uncertain at 18 months and 🔴 fragile at 5 years.

---

## Relationship to other techniques

**Key Drivers Generation™ (§9.1)** — The ideal predecessor to Steps 2–3. If the analyst is uncertain which forces should serve as drivers, run KDG first to systematically surface and prioritize candidate drivers using STEMPLES+.

**Key Assumptions Check (§7.1)** — A KAC on the existing analytic assessment is the best way to populate the fragility ratings in Step 3. Assumptions already flagged as fragile by a KAC are automatic candidates for the alternative scenarios.

**What If? Analysis (§8.2.4)** — What If? is a close cousin to the wild card step. When the wild card scenario needs a credible causal back story ("how could this conceivably happen?"), apply What If? to it: posit that the wild card has already occurred and reason backward.

**Alternative Futures Analysis / MSG (§9.6–9.7)** — AFA/MSG is the heavyweight alternative. Use Cone when a single analyst needs results quickly; use AFA/MSG when a structured group can devote time to building fully symmetric scenarios. Cone of Plausibility outputs can seed an AFA exercise by providing a validated driver list and preliminary narrative material.

**High Impact/Low Probability Analysis (§8.2.5)** — The wild card scenario in Cone of Plausibility is structurally a Hi-Lo scenario. If the wild card warrants deeper development — because of the severity of its impact — run a full Hi-Lo Analysis on it as a follow-on.

**Indicators Generation, Validation, and Evaluation (§9.11)** — After completing the cone, generate a formal indicator set for monitoring. Each scenario's lead collection indicator (identified in Step 7) seeds the IGVE exercise. The most diagnostically valuable indicators will distinguish between baseline and downside alternative.

**Premortem Analysis (§8.2.2)** — Apply Premortem to the baseline before finalizing: "Assume the baseline is wrong — which alternative scenario is it? Why?" This disciplines the baseline narrative and often reveals that a 🟡 assumption deserves 🔴 treatment.
