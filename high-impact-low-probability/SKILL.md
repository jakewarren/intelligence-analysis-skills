---
name: high-impact-low-probability
description: |
  Performs High Impact/Low Probability (Hi-Lo) Analysis — Reframing SAT (Pherson & Heuer §8.2.5). Use when anomalous information suggests a long-shot scenario may be more likely than assessed and consequences would be severe. Projects forward from a real trigger: maps impact, pathways, indicators, and response levers.

  Trigger on: "high impact low probability", "hi-lo analysis", "run a hi-lo", "strategic surprise", "tail risk", "black swan", "nightmare scenario", "early warning", "could this be the start of something bigger", "worried about this anomaly", "unlikely but catastrophic", "long-shot threat", "sensitize decision makers", "escalating risk". Also trigger when fragmentary intel may be a precursor to a high-consequence event, or when a KAC flags a catastrophic fragile assumption. Supports the High Impact/Uncertain Probability variant when intent is established but timing or method is ambiguous.

  Accepts a typed problem, pasted reporting, or uploaded document. Output: inline chat, .docx, or HTML.
---

# High Impact/Low Probability (Hi-Lo) Analysis

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §8.2.5 — based on Randolph H. Pherson, "High Impact/Low Probability Analysis," Handbook of Analytic Tools and Techniques, 5th ed. (Tysons, VA: Pherson Associates, 2019)*

## Purpose

Hi-Lo Analysis provides decision makers with early warning that a seemingly unlikely event — one with major policy, operational, or resource consequences — may be more likely than the prevailing assessment suggests. The technique's power lies in its **forward projection**: unlike What If? Analysis (which posits an endpoint and reasons backward), Hi-Lo starts from real anomalous information already in hand and then extrapolates forward to ask: *What could this lead to? What would that look like? What can we do about it now?*

The analytic focus is never on proving the event *will* happen. It is on making a credible case that the event *could* happen, mapping the pathway in enough detail that decision makers can act before the warning window closes.

Hi-Lo Analysis counters several powerful cognitive failure modes: **Mirror Imaging** (assuming adversaries think like us), the **Anchoring Effect** (treating the prevailing low-probability estimate as a fixed starting point), **Groupthink** (suppressing minority concerns to preserve consensus), **Ignoring the Absence of Information** (not factoring in what is absent from reporting), **Lacking Sufficient Bins** (discarding fragmentary information with no analytic category to hold it), and **Expecting Marginal Change** (assuming the future will differ only incrementally from the present).

> *"Most potentially devastating threats to U.S. interests start out being evaluated as unlikely. The key to effective intelligence-policy relations in strategic warning is for analysts to help policy officials in determining which seemingly unlikely threats are worthy of serious consideration."*
> — Jack Davis, "Improving CIA Analytic Performance: Strategic Warning," Sherman Kent School (2002)

---

## When to use it

Hi-Lo is most valuable when any of the following conditions are present:

- **Anomalous trigger**: New, fragmentary, or unexpected reporting suggests a previously discounted scenario may be gaining traction. Examples: a threat actor with no prior interest in ICS/SCADA suddenly queries control system vendors; a ransomware group dissolves unexpectedly just as a geopolitical crisis heats up; a zero-day affecting widely deployed industrial firmware appears on underground markets.
- **Mainline view suppresses minority concerns**: The community or client is anchored on "this won't happen" and minority warnings are being dismissed without structured examination.
- **Decision lead-time is long**: The consequence is severe enough that waiting for high-confidence reporting may eliminate the window for effective countermeasures.
- **Upstream KAC flag**: A Key Assumptions Check has identified a load-bearing assumption whose failure would be catastrophic. Hi-Lo examines what happens downstream if that assumption breaks.
- **Variant condition — High Impact/Uncertain Probability**: Intent is established but timing or method is ambiguous (e.g., a nation-state has signaled intent to conduct a destructive cyberattack on financial infrastructure, but the vector and timeline are unknown).

Hi-Lo is NOT appropriate when: the event's probability is genuinely assessed as low AND no anomalous triggering information exists. In that case, use What If? Analysis instead, which does not require a triggering condition.

---

## Step 1: Ingest the input

Accept any of these forms:

- **Problem statement in chat** — e.g., "Run a Hi-Lo on a major ransomware group targeting water utilities" or "We just saw anomalous scanning of substation ICS — could this be the start of something?"
- **Pasted analysis or raw reporting** — Extract the triggering anomaly, the low-probability event of concern, and any existing impact estimates
- **Uploaded document** — Read the file; identify the fragmentary or anomalous item that serves as the trigger, the scenario it could precede, and what the impact would be
- **KAC or What If? output as input** — If an upstream technique has flagged a fragile critical assumption or a concerning scenario, use the identified failure mode as the Hi-Lo's focal scenario

If no triggering information is provided but the user wants to explore a low-probability scenario, pivot to **What If? Analysis** (§8.2.4) and explain the distinction to the user.

---

## Step 2: Scope the analysis

Ask one short clarifying message covering:

1. **The focal scenario**: Is the low-probability event clear? If not, what is the closest approximation the user wants to examine?
2. **Variant**: Standard Hi-Lo (probability is low, triggering info exists) or High Impact/Uncertain Probability (intent established, timing/method ambiguous)?
3. **Output format**: Inline chat (fast, conversational), Word .docx (formal product), or HTML (structured deliverable with formatted tables)?
4. **Depth**: Quick scan (event + impact + 2–3 indicators) or full analysis (pathways, full indicator set, deflection levers, monitoring regime)?

If the request makes answers obvious — e.g., "quick look," a tightly described scenario, a follow-on to a KAC — skip asking and state your assumptions.

---

## Step 3: Define the low-probability event with precision

Articulate the focal scenario in concrete, specific terms. A vague event produces vague analysis.

**Good**: *"A coordinated destructive cyberattack (wiper malware) causes simultaneous loss of visibility and control across three or more U.S. electric transmission operators, resulting in multi-day outages affecting more than 10 million customers."*

**Poor**: *"A major cyberattack on U.S. infrastructure."*

Define:
- **Who** is the threat actor (or what category of actor if unknown)?
- **What** is the specific action or event?
- **What is the impact threshold** that makes this "high-impact"?
- **Timeframe**: Is there an implicit window (next 90 days, next year)?

### Probability calibration — critical

Immediately address the probability in numeric terms. The word "unlikely" is analytically useless: depending on the reader, it can be interpreted as anywhere from 1% to 25%. "Highly unlikely" spans 1% to 10%. These ambiguities cause decision makers to discount warnings more than analysts intend.

Express probability as:
- A numeric range: *"We assess a 5–15% probability within the next 12 months"*
- Bettor's odds: *"Roughly one chance in eight"*
- An explicit qualifier: *"We are not arguing this is likely. We assess it merits serious attention because [triggering condition] raises the probability above our prior estimate of <5%."*

---

## Step 4: Build the impact assessment

Define what actually happens if this event occurs. Go beyond the immediate, direct effect.

### Primary impact
The direct, immediate consequence of the event:
- Operational disruption: systems, services, personnel affected
- Financial: losses, remediation costs, ransom
- Strategic: intelligence loss, capability degradation, public trust damage

### Secondary and tertiary effects
These often exceed the primary impact and are consistently underestimated:
- Cascading failures: what other systems or processes depend on the affected component?
- Geopolitical consequences: what responses does this trigger in allied or adversary states?
- Normative effects: does this event establish a new red line, precedent, or permission structure for adversaries?
- Public and political effects: what pressure does this create on decision makers?

**Cyber example**: A ransomware attack on a major U.S. hospital system (primary: loss of patient records and clinical systems for days) cascades to: ambulance diversion → degraded trauma care → patient deaths → legislative pressure for mandatory cyber standards → emergency regulatory action. The secondary and tertiary effects dwarf the primary breach.

---

## Step 5: Identify the triggering information

Catalog the specific new or anomalous information that elevates this from a standard low-probability scenario to one meriting a Hi-Lo analysis. This is the evidentiary foundation of the analysis — it is what makes Hi-Lo distinct from idle speculation.

For each triggering item:
- **What is it?** State the information precisely.
- **Source type and credibility**: HUMINT, SIGINT, OSINT, technical (malware sample, IOC, network telemetry), financial indicator, etc. Assess credibility as HIGH / MEDIUM / LOW.
- **Why is it anomalous?** What does it represent that is different from baseline?
- **Why does it suggest the focal scenario is more plausible than previously assessed?**

Be disciplined: if a triggering item is actually consistent with multiple explanations (including innocuous ones), note that. A single IOC match to a threat actor's toolset rarely constitutes attribution, and it rarely alone justifies a Hi-Lo. The value of Hi-Lo is in the structured reasoning that follows from fragmentary evidence — not in overstating the evidence itself.

> *Tip: Run Diagnostic Reasoning (§7.5) on each triggering item if there is any question about whether it is genuinely diagnostic of the focal scenario versus consistent with multiple alternative explanations.*

---

## Step 6: Postulate additional triggers and accelerators

Identify the conditions that would, if they emerged, significantly increase the probability of the focal scenario or greatly compress the timeline. These are the analytic trip-wires the decision maker should be watching for.

Categories to consider:
- **Adversary capability triggers**: Acquisition of a new tool, technique, or access vector (e.g., adversary recruits an insider at the target organization; a new zero-day is listed for sale that targets the relevant platform)
- **Adversary intent triggers**: Geopolitical escalation, leadership change, ideological radicalization, retaliation motive activated
- **Vulnerability triggers**: New exposure created by system change, third-party compromise, or patch failure
- **Structural accelerators**: A botched government response to an earlier incident that creates political pressure for more dramatic action; a leadership transition that removes a moderating actor; an economic shock that changes an actor's risk calculus
- **Cascade triggers**: An event in an adjacent domain that feeds into the focal scenario

For each trigger, assess: (a) current status — is it present, absent, or unknown? and (b) monitoring status — is anyone watching for it?

---

## Step 7: Develop forward pathways

Map one or more plausible chains of events explaining how the focal scenario could unfold from the present. Each pathway is a sequence of enabling steps, starting now and ending at the focal event.

### Guidance

- **Aim for 2–3 pathways.** A single pathway anchors analysis on one causal model. More than three becomes unwieldy for a Hi-Lo product.
- **Label each pathway descriptively** — not "Pathway A" but something that captures the causal logic: e.g., "Supply-chain compromise enables persistent access," "Insider-assisted intrusion bypasses perimeter defenses," "State-directed group leverages criminal ransomware-as-a-service infrastructure."
- **Work forward from the present**: Start from current conditions and map each step that must occur for the focal event to materialize.
- **Each step must be plausible and specific.** If a step requires an unexplained leap, either flesh it out or split the pathway.
- **Assign relative plausibility** to each pathway (HIGH / MEDIUM / LOW): How many enabling conditions are already in place? How much new capability, access, or intent shift is required?
- **Cover diverse trigger types**: One pathway might run through technical exploitation; another through insider threat; another through supply-chain compromise. Diverse pathways illuminate different collection and mitigation priorities.

**Cyber pathway example** (ransomware group targeting water utilities):

> *Pathway 1 — "Living off the Land via IT/OT Pivot" (Plausibility: MEDIUM)*
> Initial access via phishing of IT network → lateral movement to SCADA historian server → escalation to OT network via insecure IT/OT boundary → deployment of wiper on HMI workstations → operators lose visibility and control of treatment systems → water utility declares emergency.

After drafting, review: Have comfortable or politically convenient pathways been emphasized at the expense of uncomfortable ones? Adversary use of trusted vendor access, for instance, is consistently underweighted because it implicates supply-chain partners. Include it.

---

## Step 8: Generate and validate indicators

For each pathway, build a list of observable indicators — specific, detectable signals that would tell an analyst the pathway is beginning to materialize. These are the instrument panel for monitoring the scenario over time.

### Indicator types

| Type | Description |
|------|-------------|
| **Precondition indicators** | Conditions that must be in place before the pathway is viable — check these first |
| **Process indicators** | Intermediate steps along the pathway that are detectable as they occur |
| **Tripwire indicators** | A single decisive observation that confirms the pathway is actively unfolding and requires immediate escalation |

### Indicator quality rules

- **Observable**: Something an analyst can actually detect from available collection or open sources. "Signs of increased adversary activity" fails; "new C2 infrastructure registered by [actor] using historically associated registrar patterns" passes.
- **Specific enough to be actionable**: Vague indicators are never acted on. Define the threshold at which an indicator is considered "observed."
- **Pathway-discriminating where possible**: An indicator that appears under all pathways is less valuable than one that is uniquely associated with a specific pathway.
- **Sourced**: Assign a collection source (SIGINT, HUMINT, OSINT, technical/network telemetry, financial intelligence, IMINT, partner reporting, dark web monitoring, etc.)
- **Monitoring status**: Flag each as currently monitored / not monitored / unknown.

After building the indicator list, scan for **already-observed indicators**. If indicators for a nominally low-probability pathway are already showing, that pathway is no longer low-probability for practical warning purposes — escalate this finding prominently.

---

## Step 9: Identify deflection factors and response levers

For each priority pathway, identify:

**Negative scenario (threat)**:
- What **structural or contextual factors** could deflect the scenario — e.g., a deterrence action, an adversary leadership change, a successful defensive posture improvement, a geopolitical development that removes the motive?
- What actions could a decision maker take **now** to reduce the probability of the focal event occurring?
- What actions could reduce the **impact** if the event does occur (resilience, continuity, response pre-positioning)?

**Positive scenario (opportunity)**:
- What conditions would enable the positive outcome to materialize?
- What actions could a decision maker take now to increase the probability or magnitude of the positive outcome?

The goal of this section is **preparation and leverage**, not prediction. A decision maker who has thought through deflection options before the scenario materializes is far better positioned to act during the warning window.

---

## Step 10: Design the monitoring regime

This step is what transforms Hi-Lo from a one-time product into a living warning function. It is the step most commonly omitted from weak Hi-Lo analyses — and the book identifies it as the most important.

Define:

1. **Review frequency**: How often should indicators be checked? (Daily for high-priority scenarios; weekly or monthly for lower-priority ones.)
2. **Reporting threshold**: What indicator combination or tripwire should trigger an immediate escalation product rather than waiting for the next scheduled review?
3. **Responsible collection**: Who is tasked with monitoring which indicators?
4. **Probability recalibration**: At each review, reassess the probability estimate in light of new observations. Document changes to the estimate with rationale — this audit trail protects the analyst and improves institutional memory.
5. **Escalation path**: If the tripwire is activated, what is the next analytic product (a formal warning memo, a briefing, an ACH update)?

---

## Step 11: Report the conclusions

Structure the output as follows:

---

### Required output structure

**Header**: Focal scenario | Classification (if applicable) | Date | Analyst (if provided)

**Executive Summary** (2–3 sentences)
The focal scenario, current probability estimate in numeric terms, and the single most important action implication for the decision maker.

**Section 1 — The Focal Scenario**
The low-probability event defined precisely. Probability expressed numerically. One paragraph on why this merits analytic attention despite the low probability.

**Section 2 — Triggering Information**
The specific anomalous information that elevates this scenario. Each item listed with source type, credibility assessment, and why it is analytically significant.

**Section 3 — Impact Assessment**
Primary impact, then secondary and tertiary cascading effects. Organize by consequence category (operational, financial, strategic, geopolitical, normative).

**Section 4 — Additional Triggers and Accelerators**
A list of conditions that would materially increase probability or compress the timeline, with current status (present / absent / unknown) and monitoring status.

**Section 5 — Forward Pathways**
For each pathway (2–3 total):
- Descriptive label
- Step-by-step forward causal chain from present to focal event
- Enabling conditions already in place
- Relative plausibility (HIGH / MEDIUM / LOW) with brief rationale
- Key uncertainty: the single biggest unknown that could invalidate this pathway

**Section 6 — Indicators**
A consolidated indicator table organized by pathway, showing: indicator description, type (precondition / process / tripwire), collection source, current status (observed / not observed / unknown), monitoring priority (HIGH / MEDIUM / LOW). Flag any already-observed indicators with emphasis.

**Section 7 — Deflection Factors and Response Levers**
For priority pathways: probability-reduction actions and impact-mitigation options the decision maker could take now.

**Section 8 — Monitoring Regime**
Review frequency, escalation threshold, responsible parties, and the next scheduled reassessment date.

**Section 9 — Analytic Confidence and Key Uncertainties**
State overall confidence in the analysis (HIGH / MEDIUM / LOW). Identify the 2–3 biggest gaps or uncertainties that, if resolved, would most significantly change the assessment. Flag what collection would address them.

---

## Step 12: Deliver in the requested format

**Inline chat**: Use markdown. Tables for the indicator matrix. Suitable for fast turnaround and conversational review.

**Word (.docx)**: Use the `docx` skill. Formatted report with proper headings, a styled indicator table, and a one-paragraph executive summary at the top. Appropriate for formal analytic products and distribution to decision makers.

**HTML**: Standalone file with structured, filterable indicator table (by pathway, type, monitoring status). Good for collaborative review.

> ⚠️ **Handling sensitive scenarios**: Hi-Lo analyses that map specific attack vectors, exploit methods, or adversary capabilities often warrant restricted distribution. If the scenario describes a vulnerability an adversary could exploit, flag this prominently in the header and recommend limiting circulation to principals.

---

## Analyst principles

**The triggering information is the foundation — treat it with appropriate skepticism.** Hi-Lo Analysis does not become more credible by overstating the anomaly that triggered it. Apply Diagnostic Reasoning (§7.5) to assess whether the triggering information is genuinely diagnostic of the focal scenario or merely consistent with it alongside many alternatives. A Hi-Lo analysis built on non-diagnostic evidence is a story, not an assessment.

**Probability must be numeric.** Vague words like "unlikely" or "improbable" communicate different things to different readers. Express probability as a range or bettor's odds every time. Document the prior estimate and explain specifically why the new triggering information shifts it — even modestly.

**Both primary and secondary effects must be assessed.** Decision makers consistently underweight cascading consequences. A wiper attack on a hospital is not just an IT problem. A supply-chain compromise affecting ICS firmware is not just a cybersecurity problem. Follow the cascade.

**Already-observed indicators are the most urgent finding.** If you build an indicator set and discover that two or three indicators are already green, the scenario's probability has just changed significantly. This finding must be flagged prominently — not buried in the indicator table.

**The monitoring regime is the product's longevity.** A Hi-Lo analysis without a monitoring plan is a one-time warning product that decays rapidly. The structured periodic review of indicators — and the explicit reassessment of the probability estimate at each review — is what makes Hi-Lo an early warning system rather than a snapshot.

**Multiple pathways are not optional.** A single pathway overfits the available evidence. Multiple pathways reveal which enabling conditions are common across all of them — those are the highest-priority monitoring targets regardless of which pathway is ultimately correct. They also expose which pathways are being suppressed due to political inconvenience.

**This is not a prediction and should not be presented as one.** Hi-Lo Analysis is about *possibility and preparation*, not about revising the mainline estimate. Frame the output explicitly as: "This is how the scenario could unfold; here is what to watch for; here is what we can do about it." Never frame it as "We now believe this will happen."

---

## Relationship to other techniques

**What If? Analysis (§8.2.4)** — The closest relative, but structurally distinct. What If? requires no triggering information — it posits that a surprising event has already occurred and reasons backward. Hi-Lo requires anomalous triggering information already in hand and projects forward. Use Hi-Lo when you have an anomaly that demands forward extrapolation; use What If? when you need to challenge a prevailing view that dismisses an outcome as impossible without any new triggering evidence.

**Key Assumptions Check (KAC, §7.1)** — A natural predecessor. When KAC identifies a critical load-bearing assumption whose failure would be catastrophic, Hi-Lo examines what that failure looks like, how it could occur, and what can be done about it. KAC identifies fragility; Hi-Lo maps the consequences of that fragility.

**Diagnostic Reasoning (§7.5)** — Apply to each triggering item before proceeding with Hi-Lo. The central question: "If an alternative, more benign explanation were true, would I still see this evidence?" If yes, the trigger is non-diagnostic and the Hi-Lo rests on shaky ground. Calibrate accordingly.

**Analysis of Competing Hypotheses (ACH, §7.6)** — If the triggering information could reflect multiple explanations (not just the focal scenario), run an ACH first to determine which explanation best fits the evidence body before investing in a full Hi-Lo on the focal scenario.

**Alternative Futures Analysis (§9.6)** — Hi-Lo analysis is one productive output of an AFA exercise: once the 2×2 matrix is populated, the cell representing the radical departure from expected trends — the "wild card" quadrant — is precisely the Hi-Lo candidate. Treat that scenario with the Hi-Lo method.

**Indicators Generation, Validation, and Evaluation (§9.11)** — The indicators produced in Step 8 should be formally validated using the IGVE framework (observable, valid, reliable, diagnostic, collection-feasible) and entered into the active monitoring regime. Hi-Lo is one of the best generators of early-warning indicators for scenarios the community considers unlikely and would otherwise not monitor.

**Premortem Analysis (§8.2.2)** — Use Premortem to stress-test the Hi-Lo analysis itself before delivering it. The Premortem question: "Assume this Hi-Lo analysis was wrong and we missed the scenario anyway — how did that happen?" This surfaces gaps in indicator coverage, collection blind spots, and over-reliance on assumptions.

**Deception Detection (§7.8)** — For Hi-Lo scenarios involving sophisticated adversaries, ask whether the triggering information could itself be planted. A sophisticated adversary aware of your analytic processes might manufacture an anomaly precisely to trigger a Hi-Lo that wastes resources, exposes collection methods, or redirects attention. Apply the MOM/POP/MOSES/EVE framework if deception is plausible.
