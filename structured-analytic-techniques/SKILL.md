---
name: structured-analytic-techniques
description: |
  Acts as a meta-skill and planning consultant for Structured Analytic Techniques (SATs). When an analyst describes a task, problem, or analytical goal, this skill diagnoses the situation, recommends which SATs to use, and produces a sequenced analytic plan.

  Trigger on: "which technique should I use", "what SAT should I use", "help me plan my analysis", "how should I approach this", "what's the best SAT for", "I need to analyze X", "plan my analysis", "SAT recommendations", "analytic workflow", "which skills should I use", "where do I start", "I have a report to review", "I have an incident to analyze", "I need to do foresight", "what techniques apply here", "I don't know where to start", "help me think through", "what should I run first", "build me an analytic plan".

  Accepts a description of the analyst's task, problem, or goal. Output: inline chat (default), .docx, or HTML with visual workflow diagram.
---

# Structured Analytic Techniques — Analytic Planner

*Source: Derived from Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed. — synthesizes the full SAT taxonomy into a planning and sequencing framework*

## Purpose

The Structured Analytic Techniques Planner is a meta-skill that answers the analyst's first question: **"Where do I start — and what do I run next?"**

With 18+ SATs available, the hardest problem is not executing any one technique but selecting the right combination for the job and sequencing them in the right order. Each technique has blind spots; no single SAT covers the full analytic picture. The right sequence depends on the analyst's task, time constraints, and the intended audience for the product.

This planner addresses two persistent failure modes:
- **Over-reliance on one technique** — Running ACH on everything even when the real problem is an unexamined assumption or an adversary behavior question
- **Under-utilization** — Running a KAC but never following it with What If?, or running an AFA without first running KDG

The planner produces two options every time:
- **Quick Plan**: 1–3 techniques, designed for time-constrained operational analysis, oral briefings, or triage
- **Thorough Plan**: A complete sequenced workflow for finished intelligence, formal assessments, or products that will receive peer review or reach senior consumers

---

## How This Skill Works

1. **Ingest** the analyst's task description (Step 1)
2. **Clarify** task type, time constraints, and output format (Step 2)
3. **Classify** the task against eight scenario types (Step 3)
4. **Build the plan** — Quick and Thorough — for the identified scenario (Step 4)
5. **Deliver** the plan with rationale, time estimates, and skill invocation guidance (Step 5)

---

## Step 1: Ingest the Input

Accept any of these:

- **Task description in chat** — "I need to analyze a new phishing campaign and figure out if it's nation-state" / "I have a finished report my boss wants challenged" / "Help me think about how the ransomware landscape might evolve"
- **Pasted analysis or reporting** — Read the material and infer the task type from its content and any stated or implied gaps
- **Uploaded document** — Read the file; identify what kind of analytic product it represents and what work remains

If the task is described only vaguely, proceed to Step 2 for clarification. If the task is clear enough to classify, proceed directly to Step 3 and state the classification.

---

## Step 2: Clarify Task, Constraints, and Format

Ask a **single clarifying message** covering all three dimensions. Do not send multiple messages; do not ask questions that can be inferred from context.

> *"To build the right analytic plan, I need to understand three things: (1) What is the primary analytic goal — are you triaging an incident, attributing an attack, challenging an existing assessment, forecasting how something evolves, or something else? (2) How much time do you have — are we talking a few hours, or a full analysis with days to work? (3) What format do you want the plan in — inline chat, a Word document, or an HTML visual?*

If the context makes one or more answers clear — "quick look," "I have a deadline tomorrow," "need a formal report" — skip those and ask only what is genuinely unknown.

---

## Step 3: Classify the Task

Map the analyst's goal to one of the eight primary scenario types below. State the classification explicitly at the start of the output.

| # | Scenario Type | When It Applies |
|---|---|---|
| **1** | Incident Triage / First Look | Something new just happened — an intrusion, breach, campaign, or development — and the analyst needs a structured initial picture |
| **2** | Threat Actor Attribution | The central question is who did something, with what confidence, and what evidence supports that claim |
| **3** | Assessment / Report Review | An existing analysis, draft product, or established assessment needs to be challenged, validated, or stress-tested |
| **4** | Foresight / Futures | The question is forward-looking: how might a threat, situation, or actor evolve? What scenarios should we plan for? |
| **5** | Early Warning / Strategic Warning | Fragmentary or anomalous information may signal something bigger; the question is how seriously to take it and what to watch for |
| **6** | Adversary Behavior Prediction | The question is what a specific actor will do next, how they will respond to a given stimulus, or what courses of action they are likely to pursue |
| **7** | Strategic Decision Support | A decision needs to be made about posture, investment, policy, or action; the analysis should support and frame the options |
| **8** | Full Finished Intelligence Product | A comprehensive, polished product is needed — suitable for senior consumers, peer review, or formal publication — covering a complex topic end-to-end |

**If a task spans multiple scenario types** (e.g., triaging an incident that also requires a behavioral prediction), build separate Quick and Thorough plans for each and note where the outputs of one feed into the next.

---

## Step 4: Build the Plan

Use the scenario-specific plans below as a foundation. Adjust based on what the analyst's input already provides — if they have already run Circleboarding, skip it; if ACH hypotheses are already established, enter the plan at MHG or ACH.

---

### Scenario 1: Incident Triage / First Look

*"Something just happened. I need to understand what it is, who's behind it, and what it means."*

#### Quick Plan — Triage (2–4 hours)

**Step 1 → Circleboarding** *(Exploration)*
- Invoke: `circleboarding`
- Why: Forces structured answers to Who, What, How, When, Where, and Why before any conclusions are drawn. Surfaces knowledge gaps immediately. The "So What?" forces impact articulation. In CTI this prevents jumping to attribution before the basic facts are established.
- Output: A structured picture of what is known and what is not; a gap inventory; initial So What.

**Step 2 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Why: The initial Circleboard almost always embeds unexamined assumptions, especially in the WHY and WHO dimensions. Running a KAC on the initial picture surfaces those assumptions before they harden into orthodoxy.
- Output: Ranked list of assumptions with risk ratings; RED/ORANGE assumptions that require immediate attention.

> Time estimate: 2–3 hours total. These two techniques together produce a defensible initial assessment with explicit uncertainty mapping.

---

#### Thorough Plan — Comprehensive Incident Analysis (1–3 days)

**Step 1 → Circleboarding** *(Exploration)*
- Invoke: `circleboarding`
- Build the initial structured picture. Collect all known facts. Surface gaps.

**Step 2 → Outside-In Thinking / STEMPLES+** *(Reframing)*
- Invoke: `outside-in-thinking`
- Why: Before forming hypotheses, scan the broader environment. What geopolitical, economic, legal, or technological forces shape the context? CTI analysts often miss Legal (prosecution risk) and Economic (criminal ROI) forces that explain actor behavior.

**Step 3 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Surface assumptions embedded in the Circleboard and OIT findings before they become hypotheses.

**Step 4 → Multiple Hypothesis Generation** *(Diagnostic)*
- Invoke: `multiple-hypothesis-generation`
- Why: Generate a MECE set of competing explanations for the incident. Prevents anchoring on the first plausible actor.

**Step 5 → Analysis of Competing Hypotheses** *(Diagnostic)*
- Invoke: `analysis-of-competing-hypotheses`
- Why: Test each hypothesis against the full evidence body. The hypothesis with the fewest inconsistencies survives — not the one with the most supporting evidence.

**Step 6 → Deception Detection** *(Diagnostic — conditional)*
- Invoke: `deception-detection`
- Why: Run this if the ACH deception hypothesis remains viable, if reporting seems suspiciously convenient, or if the actor has documented D&D capability. Apply MOM/POP/MOSES/EVE.

**Step 7 → Red Hat Analysis** *(Reframing)*
- Invoke: `red-hat-analysis`
- Why: Once the lead hypothesis is established, simulate adversary decision logic to understand what they were actually trying to achieve. Guards against mirror imaging in the WHY dimension.

**Step 8 → Premortem Analysis** *(Reframing)*
- Invoke: `premortem-analysis`
- Why: Pre-publication stress test. Imagine the lead assessment is wrong. What failed? Surfaced problems require caveats, collection action, or revised confidence.

> Time estimate: 1–2 days for the full chain, depending on evidence richness. Steps 1–4 can be compressed in a team setting.

---

### Scenario 2: Threat Actor Attribution

*"Who did this? How confident can I be? Can this hold up to scrutiny?"*

#### Quick Plan — Attribution Check (2–4 hours)

**Step 1 → Diagnostic Reasoning** *(Diagnostic)*
- Invoke: `diagnostic-reasoning`
- Why: Start here, not with attribution. Test the key evidence items individually before building the attribution case. A code string, a C2 IP, or a TTP overlap is almost never diagnostic on its own — it is consistent with false-flag, commodity tooling, and multiple alternative actors. Establish what the evidence actually proves.

**Step 2 → Multiple Hypothesis Generation** *(Diagnostic)*
- Invoke: `multiple-hypothesis-generation`
- Why: Force a structured competing attribution set before committing to the lead. Use Method C (Multiple Hypotheses Generator®) if there is already a dominant lead attribution.

> Time estimate: 2–3 hours. These two steps together will determine whether the attribution is defensible or premature.

---

#### Thorough Plan — Rigorous Attribution Assessment (2–5 days)

**Step 1 → Diagnostic Reasoning** *(Diagnostic)*
- Invoke: `diagnostic-reasoning`
- Run on every key attribution artifact individually. Establish which items are genuinely diagnostic vs. consistent with alternatives. This prevents building an attribution case on non-discriminating evidence.

**Step 2 → Circleboarding** *(Exploration — threat actor mode)*
- Invoke: `circleboarding`
- Run in threat actor mode to build a comprehensive actor profile: TTPs, infrastructure, targeting patterns, motivation, historical precedents. This grounds the attribution in actor knowledge, not just indicator matching.

**Step 3 → Multiple Hypothesis Generation** *(Diagnostic)*
- Invoke: `multiple-hypothesis-generation`
- Generate the full competing attribution set. Include false-flag as an explicit hypothesis. Use Method C if a lead attribution already exists.

**Step 4 → Analysis of Competing Hypotheses** *(Diagnostic)*
- Invoke: `analysis-of-competing-hypotheses`
- Always include the deception hypothesis. Weight each evidence item against all hypotheses. The lead attribution hypothesis must survive the full matrix.

**Step 5 → Deception Detection** *(Diagnostic — always for high-confidence attribution)*
- Invoke: `deception-detection`
- Why: High-confidence attribution is exactly where a sophisticated adversary plants false flags. Apply MOM, POP, MOSES, EVE. The 2018 Olympic Destroyer false flag (Sandworm impersonating Lazarus) is the canonical failure mode.

**Step 6 → Argument Mapping** *(Diagnostic)*
- Invoke: `argument-mapping`
- Why: Validate the surviving attribution claim with full logical structure. Every objection requires a rebuttal. Bare red nodes — objections with no rebuttal — require caveats or a downgraded confidence qualifier.

**Step 7 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Why: Attribution claims rest on assumptions about actor capability, motive, and infrastructure exclusivity. KAC surfaces these assumptions and rates which are fragile. A HIGH confidence claim resting on RED assumptions needs to be reclassified.

**Step 8 → Premortem Analysis** *(Reframing — pre-publication)*
- Invoke: `premortem-analysis`
- Why: Before publishing, imagine the attribution is wrong. How did that happen? Surfaced failure modes require either investigation or explicit caveating.

> Time estimate: 2–5 days for the full chain. Steps 1–4 are the core attribution cycle; Steps 5–8 are the quality-assurance layer.

---

### Scenario 3: Assessment / Report Review

*"I have an analysis or report. Challenge it. Find what it's getting wrong."*

#### Quick Plan — Rapid Challenge (1–2 hours)

**Step 1 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Why: This is the single highest-leverage technique for challenging existing analysis. ~25% of key assumptions collapse under careful scrutiny (Pherson). Surface every assumption, rate it, identify RED assumptions.

**Step 2 → Premortem Analysis** *(Reframing)*
- Invoke: `premortem-analysis`
- Why: Imagine the report is spectacularly wrong, then work backward. What failed? This surfaces failure modes the KAC may miss and legitimizes dissent.

> Time estimate: 1–2 hours. This pair constitutes the minimum viable peer review.

---

#### Thorough Plan — Full Structured Peer Review (4–8 hours)

**Step 1 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- The foundation. Surface all explicit and implicit assumptions; rate them; identify RED/ORANGE risk assumptions.

**Step 2 → Diagnostic Reasoning** *(Diagnostic)*
- Invoke: `diagnostic-reasoning`
- For each key piece of evidence cited in the report, run the diagnostic test: is it actually discriminating between competing hypotheses, or merely consistent with the lead hypothesis? Most analytic overconfidence stems from non-diagnostic evidence being treated as confirmation.

**Step 3 → Argument Mapping** *(Diagnostic)*
- Invoke: `argument-mapping`
- Map the logical structure of the report's central claim. Build supporting arguments, identify objections, generate rebuttals. Bare red nodes are documented flaws requiring caveats.

**Step 4 → What If? Analysis** *(Reframing)*
- Invoke: `what-if-analysis`
- For the one or two most critical KAC RED assumptions: posit that those assumptions are wrong. What does the analysis look like now? What pathways lead to that outcome? What would we watch for?

**Step 5 → Premortem Analysis + Structured Self-Critique** *(Reframing)*
- Invoke: `premortem-analysis`
- Full SSC: work through all ten dimensions of analytic failure (sources of uncertainty, analytic process, critical assumptions, diagnostic evidence, information gaps, missing evidence, anomalous evidence, environmental changes, alternative decision models, deception).

**Step 6 → Deception Detection** *(Diagnostic — conditional)*
- Invoke: `deception-detection`
- Run if the SSC dimension 10 (Deception) raised concerns, if the key evidence is suspiciously convenient, or if the assessed actor has documented D&D capability.

> Time estimate: 4–8 hours. This produces a structured peer review product suitable as a formal analytical annex.

---

### Scenario 4: Foresight / Futures Analysis

*"How might this threat, situation, or actor evolve? What scenarios should we plan for?"*

#### Quick Plan — Bounded Scenarios (3–5 hours)

**Step 1 → Cone of Plausibility** *(Foresight)*
- Invoke: `cone-of-plausibility`
- Why: Faster than full AFA. Builds a baseline, generates alternatives by modifying fragile assumptions, and produces a wild card. A single analyst can complete this in hours. Always produces the mandatory four scenario types: baseline, downside risk, opportunities, and wild card.

> Time estimate: 2–4 hours for baseline + 2 alternatives + wild card. Suitable for an operational briefing or a quick estimative note.

---

#### Thorough Plan — Full Scenario Development (2–5 days)

**Step 1 → Outside-In Thinking / STEMPLES+** *(Reframing)*
- Invoke: `outside-in-thinking`
- Why: Before generating scenarios, scan the external environment. Social, technological, economic, military, political, legal, environmental, and security forces all shape how a situation will evolve. OIT ensures the driver list does not miss structural forces.

**Step 2 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Run a KAC on the current analytic baseline (the prevailing assessment about how things will develop). Fragile assumptions identified here become candidate drivers — each one represents an axis on which the future could diverge.

**Step 3 → Key Drivers Generation** *(Foresight)*
- Invoke: `key-drivers-generation`
- Synthesize the OIT candidate pool and KAC fragile assumptions into 4–6 key drivers. For each driver, define the spectrum of plausible endpoints. This is the prerequisite for AFA and MSG.

**Step 4 → Alternative Futures Analysis** *(Foresight)*
- Invoke: `alternative-futures-analysis`
- Use the two highest-uncertainty, highest-consequence drivers as matrix axes. Generate four scenarios: mainline, downside risk, opportunity, and emerging trend. Develop narratives, implications, and decision-maker actions for each.

**Step 5 → What If? Analysis** *(Reframing — for nightmare scenarios)*
- Invoke: `what-if-analysis`
- For the scenario the analytic community finds most implausible (the "nightmare" or wild card): posit it has already occurred and reason backward. Provides a credible causal backstory for a scenario that otherwise seems too alarming to take seriously.

**Step 6 → Indicators Generation, Validation, and Evaluation** *(Foresight)*
- Invoke: `indicators-generation-validation-evaluation`
- Generate observable indicators for each scenario. Validate each indicator against five quality criteria (observable, timely, specific, diagnostic, collectable). Build a monitoring matrix and collection requirements.

> Time estimate: 2–4 days for the full chain. Steps 1–3 are the foundation that most analysts skip and then regret; Steps 4–6 are the deliverable.

---

### Scenario 5: Early Warning / Strategic Warning

*"Something small caught my attention. Could it be the start of something bigger? How seriously should I take it?"*

#### Quick Plan — Warning Check (1–2 hours)

**Step 1 → Diagnostic Reasoning** *(Diagnostic)*
- Invoke: `diagnostic-reasoning`
- Why: Before escalating, test whether the anomaly is genuinely diagnostic of a larger threat or merely consistent with multiple (including benign) explanations. A single IOC, report, or development is almost never a warning in itself.

**Step 2 → High Impact / Low Probability Analysis** *(Reframing)*
- Invoke: `high-impact-low-probability`
- Why: If the triggering information passes the diagnostic test, Hi-Lo projects forward: how could this anomaly lead to the high-impact scenario? What pathways exist? What indicators would signal it developing?

> Time estimate: 1–2 hours. Produces a defensible early warning note with specific monitoring indicators.

---

#### Thorough Plan — Strategic Warning Assessment (1–3 days)

**Step 1 → Diagnostic Reasoning** *(Diagnostic)*
- Invoke: `diagnostic-reasoning`
- Test each anomalous trigger item. Establish what it does and does not prove.

**Step 2 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Run on the current prevailing assessment (the "this won't happen" view). Identify the specific assumption that the anomalous information is challenging.

**Step 3 → What If? Analysis** *(Reframing)*
- Invoke: `what-if-analysis`
- Posit that the large-consequence event has already occurred. Work backward to explain how. Produces multiple pathways and a precondition indicator set. Provides a framework for the Hi-Lo analysis.

**Step 4 → High Impact / Low Probability Analysis** *(Reframing)*
- Invoke: `high-impact-low-probability`
- Build the full forward-looking warning product: triggering information, impact assessment (primary + cascading), additional triggers and accelerators, forward pathways, indicators, deflection factors, and monitoring regime.

**Step 5 → Indicators Generation, Validation, and Evaluation** *(Foresight)*
- Invoke: `indicators-generation-validation-evaluation`
- Formalize the indicator set from Hi-Lo into a validated, collection-ready monitoring regime.

> Time estimate: 1–2 days. The chain from Diagnostic Reasoning through Hi-Lo constitutes a complete strategic warning product.

---

### Scenario 6: Adversary Behavior Prediction

*"What will this actor do next? How will they respond to X? What are their likely courses of action?"*

#### Quick Plan — Behavioral Forecast (2–3 hours)

**Step 1 → Red Hat Analysis** *(Reframing)*
- Invoke: `red-hat-analysis`
- Why: Red Hat forces the analyst to step into the adversary's frame — their values, constraints, risk tolerance, and operational culture — and simulate their decision logic. Produces Most Likely COA (MLCOA) and Most Dangerous COA (MDCOA). The MLCOA tells defenders how to allocate resources now; the MDCOA tells them what to prepare for as a contingency.

> Time estimate: 2–3 hours with reasonable actor knowledge. The single most targeted technique for behavioral prediction questions.

---

#### Thorough Plan — Comprehensive Behavioral Assessment (1–2 days)

**Step 1 → Circleboarding** *(Exploration — threat actor mode)*
- Invoke: `circleboarding`
- Build a comprehensive actor profile before the Red Hat shift: TTPs, infrastructure, organizational structure, motivation, historical decisions under pressure.

**Step 2 → SWOT Analysis** *(Decision Support — adversary mode)*
- Invoke: `swot-analysis`
- Run in Mode 2 (adversary assessment). Maps the actor's confirmed strengths and exposed weaknesses alongside the external opportunities and threats they face. Provides the strategic context for the Red Hat simulation.

**Step 3 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Run a KAC on the actor profile assumptions before the Red Hat shift. Fragile assumptions about actor motivation or constraints will corrupt the simulation if unchallenged.

**Step 4 → Red Hat Analysis** *(Reframing)*
- Invoke: `red-hat-analysis`
- Full Red Hat with the actor profile, SWOT context, and validated assumptions as inputs. Generate the first-person adversary analysis. Produce MLCOA and MDCOA with rationale, enabling conditions, and key assumptions.

**Step 5 → Indicators Generation, Validation, and Evaluation** *(Foresight)*
- Invoke: `indicators-generation-validation-evaluation`
- Convert the COAs from Red Hat into collection-ready behavioral indicators. For each COA, what observable would signal it is already underway?

> Time estimate: 1–2 days. This chain produces a behavioral intelligence product suitable for operational planning and defensive posture decisions.

---

### Scenario 7: Strategic Decision Support

*"We need to make a decision about posture, investment, policy, or action. Help us think through it."*

#### Quick Plan — Strategic Framing (2–4 hours)

**Step 1 → SWOT Analysis** *(Decision Support)*
- Invoke: `swot-analysis`
- Why: SWOT maps the current strategic landscape — internal strengths and weaknesses, external opportunities and threats — and extends into a TOWS matrix that generates concrete strategic options. The TOWS (SO/WO/ST/WT) combinations prevent tunnel vision on a single option.

> Time estimate: 2–3 hours. Produces a structured decision support product with prioritized strategic options.

---

#### Thorough Plan — Full Decision Analysis (1–3 days)

**Step 1 → Outside-In Thinking / STEMPLES+** *(Reframing)*
- Invoke: `outside-in-thinking`
- Scan the external environment before forming strategic options. Opportunities and Threats in the SWOT are only as good as the analyst's external situational awareness.

**Step 2 → SWOT Analysis** *(Decision Support)*
- Invoke: `swot-analysis`
- Full SWOT with TOWS matrix, drawing on the OIT findings to populate the Opportunities and Threats quadrants.

**Step 3 → Key Assumptions Check** *(Diagnostic)*
- Invoke: `key-assumptions-check`
- Run KAC on the top strategic options. Every option rests on assumptions about what conditions will hold. RED assumptions beneath a strategy constitute hidden strategic risk.

**Step 4 → What If? Analysis** *(Reframing)*
- Invoke: `what-if-analysis`
- For the most concerning failure mode identified in the KAC: posit that it has occurred. What would the decision landscape look like? Does the preferred strategy still hold?

**Step 5 → Cone of Plausibility** *(Foresight)*
- Invoke: `cone-of-plausibility`
- Project how the external environment might evolve. A strategy that only works in the baseline scenario is a fragile strategy. The Cone shows which strategies remain viable across the plausible range of futures.

> Time estimate: 2–3 days. The chain from OIT through Cone produces a strategy that is robust across multiple plausible futures.

---

### Scenario 8: Full Finished Intelligence Product

*"I need a comprehensive, polished assessment suitable for senior consumers, peer review, or formal publication."*

A full finished product requires the complete analytic cycle: exploration, diagnostic evaluation, reframing, and pre-publication quality assurance.

#### Recommended Sequence (4–8 days)

**Phase 1 — Scoping and Exploration (Day 1)**

1. **Outside-In Thinking / STEMPLES+** → `outside-in-thinking`
   - Environmental scan before any hypotheses are formed. Ensures the analysis does not miss structural forces.

2. **Circleboarding** → `circleboarding`
   - Map everything known about the topic (Who/What/How/When/Where/Why). Surface gaps explicitly.

**Phase 2 — Diagnostic Analysis (Days 2–4)**

3. **Key Assumptions Check** → `key-assumptions-check`
   - Surface and rate all assumptions underlying the emerging assessment. RED assumptions are analytic vulnerabilities.

4. **Multiple Hypothesis Generation** → `multiple-hypothesis-generation`
   - Generate the MECE hypothesis set. Include at least one null hypothesis and one deception hypothesis.

5. **Analysis of Competing Hypotheses** → `analysis-of-competing-hypotheses`
   - Build the full evidence matrix. The hypothesis with the fewest inconsistencies is the lead assessment.

6. **Diagnostic Reasoning** → `diagnostic-reasoning`
   - For each key evidence item: test whether it discriminates between hypotheses or is merely consistent with all. Non-diagnostic evidence cannot carry the weight analysts routinely assign it.

7. **Deception Detection** → `deception-detection` *(conditional)*
   - Run if the ACH deception hypothesis survived, if the actor has documented D&D capability, or if a single source is load-bearing.

**Phase 3 — Reframing (Days 4–5)**

8. **Red Hat Analysis** → `red-hat-analysis`
   - For any assessment involving adversary behavior or intent: simulate the adversary's perspective. Guards against mirror imaging in the WHY dimension.

9. **What If? Analysis** → `what-if-analysis`
   - For the most fragile KAC assumption: posit it is wrong. Builds the dissent case into the product.

**Phase 4 — Quality Assurance (Day 6–7)**

10. **Argument Mapping** → `argument-mapping`
    - Validate the lead assessment with full logical structure. Bare red nodes require explicit caveats before publication.

11. **Premortem Analysis + Structured Self-Critique** → `premortem-analysis`
    - Pre-publication stress test across all ten dimensions. No finished product of consequence should skip this step.

**Phase 5 — Indicators and Monitoring (Day 7–8)**

12. **Indicators Generation, Validation, and Evaluation** → `indicators-generation-validation-evaluation`
    - Generate collection-ready indicators for the lead assessment and key alternative hypotheses. Build a monitoring and review regime.

> Total time estimate: 4–8 analyst-days depending on topic complexity, evidence richness, and team size. Steps can be parallelized in a team setting. In a one-analyst sprint, phases 2–3 can be compressed to 2–3 days.

---

## Step 5: Deliver the Plan

Format the output as follows:

### Required Structure

**Section 1 — Task Classification**
One sentence: what type of analysis this is, and why.

**Section 2 — Quick Plan**
For each technique in sequence:
- Technique name (with skill invocation command)
- Why this technique for this task
- What input it needs
- What output it produces
- Rough time estimate

**Section 3 — Thorough Plan**
Same structure, with phase labels for multi-day workflows. Include a critical path note: which steps are load-bearing and should not be skipped, even under time pressure.

**Section 4 — Entry Point Check**
Note which work has already been done (based on what the analyst described) and where the analyst should enter the recommended plan.

**Section 5 — Key Warning Signs to Watch For**
Based on the task type, note 2–3 cognitive traps or analytic failure modes that are most likely to derail this type of analysis.

---

## Output Format Guidance

**Inline chat**: Structured markdown with sections as above. Include a summary table of the recommended techniques in sequence.

**Word (.docx)**: Use the `docx` skill. Formatted analytic planning document with a workflow table, phase descriptions, and technique summaries. Appropriate when the plan itself is a deliverable to be shared with a team.

**HTML**: Standalone file with a visual workflow diagram showing technique sequence as a linear flow with phase labels. Each technique box links to a brief description. Color-coded by SAT family (Exploration = blue, Diagnostic = green, Reframing = amber, Foresight = purple, Decision Support = teal). Show Quick Plan and Thorough Plan as parallel tracks.

---

## Complete SAT Reference Catalog

The 18 currently available skills, organized by analytic function:

### Exploration
| Skill | Trigger Command | Primary Use |
|---|---|---|
| Circleboarding™ | `circleboarding` | Map Who/What/How/When/Where/Why for any topic, incident, or threat actor |
| Outside-In Thinking / STEMPLES+ | `outside-in-thinking` | Environmental scan before hypotheses; surfaces forces that specialty analysis misses |

### Diagnostic
| Skill | Trigger Command | Primary Use |
|---|---|---|
| Key Assumptions Check | `key-assumptions-check` | Surface and rate hidden assumptions; challenge any assessment |
| Multiple Hypothesis Generation | `multiple-hypothesis-generation` | Build MECE hypothesis set before ACH |
| Diagnostic Reasoning | `diagnostic-reasoning` | Test whether a single piece of evidence actually discriminates between hypotheses |
| Analysis of Competing Hypotheses | `analysis-of-competing-hypotheses` | Systematic matrix evaluation; reject hypotheses by inconsistency |
| Deception Detection | `deception-detection` | MOM/POP/MOSES/EVE checklist for possible manipulation of reporting |
| Argument Mapping | `argument-mapping` | Logical validation of a single claim; identify bare red nodes (uncontested objections) |

### Reframing
| Skill | Trigger Command | Primary Use |
|---|---|---|
| Red Hat Analysis | `red-hat-analysis` | Simulate adversary decision-making; produce MLCOA and MDCOA |
| What If? Analysis | `what-if-analysis` | Backwards thinking from a posited endpoint; challenge prevailing views |
| High Impact / Low Probability | `high-impact-low-probability` | Forward projection from anomalous trigger; strategic warning product |
| Premortem Analysis | `premortem-analysis` | Pre-publication stress test; Structured Self-Critique across 10 failure dimensions |
| SWOT Analysis | `swot-analysis` | Strategic assessment (self or adversary); generates TOWS strategic options |

### Foresight
| Skill | Trigger Command | Primary Use |
|---|---|---|
| Key Drivers Generation™ | `key-drivers-generation` | Identify and prioritize forces shaping future development; prerequisite for AFA |
| Alternative Futures Analysis | `alternative-futures-analysis` | Four scenarios from two key drivers (AFA) or three-plus drivers (MSG) |
| Cone of Plausibility | `cone-of-plausibility` | Fast bounded scenarios; assumption-first; baseline + alternatives + wild card |
| Indicators Generation, Validation, and Evaluation | `indicators-generation-validation-evaluation` | Collection-ready indicator sets; monitoring regime |

---

## Natural Technique Sequences

These are the validated pairings and chains that appear most frequently across the scenario plans:

| First Technique | Natural Follow-on | Logic |
|---|---|---|
| Circleboarding | Key Assumptions Check | WHY and WHO dimensions always embed implicit assumptions worth challenging |
| Key Assumptions Check | What If? Analysis | RED assumptions become What If? posits — imagine the assumption is wrong |
| Key Assumptions Check | Key Drivers Generation | U-classified assumptions are candidate drivers for scenario exercises |
| Multiple Hypothesis Generation | Analysis of Competing Hypotheses | MHG produces the hypothesis set that ACH tests against evidence |
| Analysis of Competing Hypotheses | Argument Mapping | ACH identifies the lead hypothesis; Argument Mapping validates it logically |
| Analysis of Competing Hypotheses | Deception Detection | If the deception hypothesis survives ACH, escalate to formal D&D analysis |
| Red Hat Analysis | Indicators Generation | COAs from Red Hat become behavioral indicators for monitoring |
| Outside-In Thinking | Key Drivers Generation | OIT candidate pool feeds directly into KDG winnowing |
| Key Drivers Generation | Alternative Futures Analysis | KDG produces the driver list; AFA builds the 2×2 scenario matrix |
| High Impact/Low Probability | Indicators Generation | Hi-Lo forward pathways generate the indicator set for monitoring |
| What If? Analysis | High Impact/Low Probability | What If? explains the backstory; Hi-Lo projects the forward pathway |
| Premortem Analysis | Key Assumptions Check | SSC Dimension 3 (Critical Assumptions) generates KAC inputs if not already run |
| SWOT Analysis | Red Hat Analysis | Mode 2 SWOT (adversary) + Red Hat = capability profile + behavioral simulation |

---

## SAT Family Selection Principles

**Start with Exploration when**: the topic is new, the team lacks a shared understanding of the basic facts, or the problem has not yet been bounded. *Circleboarding* or *Outside-In Thinking* belongs at the beginning of nearly every serious analytic effort.

**Use Diagnostic techniques when**: you need to evaluate evidence, test hypotheses, or challenge an existing assessment. *ACH* is the flagship; *KAC* is its essential companion. *Diagnostic Reasoning* should be applied to every key evidence item before it is used to update an assessment.

**Apply Reframing techniques when**: you need to break out of an entrenched mental model, simulate the adversary's perspective, or stress-test a near-final conclusion. *Red Hat* belongs in every adversary behavior product; *Premortem* belongs before every finished product is published.

**Run Foresight techniques when**: the question is forward-looking. The natural sequence is OIT → KDG → AFA/Cone → IGVE. Skipping KDG and going straight to AFA typically produces scenarios that are poorly grounded in the most consequential uncertainties.

**Use Decision Support techniques when**: the output needs to frame options for a decision-maker, not just describe a situation. *SWOT* bridges the gap between intelligence product and actionable strategy.

---

## Five Signs You Need This Skill

1. **You have run the same technique on every problem for the last month.** Most analysts default to ACH (or KAC, or Red Hat) regardless of what the problem actually requires. Technique monotony is its own analytic failure mode.

2. **You're not sure where to start.** Especially in a new or fast-moving situation, the instinct to "just start analyzing" without a plan leads to disorganized products that lack internal coherence.

3. **You've finished one technique and don't know what to do with the output.** KAC produces RED assumptions — but many analysts don't know those belong in ACH as evidence items, or should trigger a What If?

4. **Your team is doing analysis in parallel with no shared framework.** Different analysts running different techniques on the same problem with no sequencing plan produce redundant or incompatible outputs.

5. **You have a finished product to produce and no analytic plan.** The eight-day full finished intelligence workflow above is worth reviewing before any major analytical undertaking.

---

## Relationship to Other Techniques

This skill is a meta-skill — it does not perform analysis itself. It consults on which techniques will best serve the analyst's goal, in what order, with what sequencing logic.

Every other skill in the SAT library is subordinate to this one from a planning perspective. Use this skill at the start of any analytic effort where the right approach is not immediately obvious, and return to it when a technique's output points toward a natural next step that wasn't in the original plan.

The most valuable use of this skill is **at the moment of uncertainty**: when the analyst has completed one technique and is unsure what to do next. The natural technique sequences table above was designed specifically for that moment.
