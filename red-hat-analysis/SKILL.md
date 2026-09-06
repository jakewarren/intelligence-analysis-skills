---
name: red-hat-analysis
description: |
  Performs Red Hat Analysis — Reframing SAT (Pherson & Heuer §8.1.3, T25). Simulates adversary decision-making by adopting their cultural frame, values, and constraints. Primary defense against Mirror Imaging.

  Trigger on: "red hat", "red hat analysis", "think like the attacker", "adversary mindset", "adversary perspective", "how would [actor] respond", "what would [actor] do", "mirror imaging", "simulate the adversary", "threat actor decision making", "MLCOA", "MDCOA", "adversary courses of action", "what is the attacker thinking", "how would APT respond", "how would ransomware group respond". Also trigger when forecasting adversary behavior without accounting for adversary culture or constraints — CTI attribution, threat actor profiling, campaign forecasting, or incident response planning.

  Accepts a typed problem, pasted reporting, or uploaded document. Output: inline chat, Word .docx, or HTML.
---

# Red Hat Analysis

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §8.1.3 (T25) — based on Randolph H. Pherson, Handbook of Analytic Tools and Techniques, 5th ed. (Tysons, VA: Pherson Associates, 2019)*

## Purpose

Red Hat Analysis forces an analyst to temporarily *become* the adversary — adopting their decision-making logic, value system, operational constraints, and cultural frame — rather than asking "what would I do if I were them?" (which almost always produces Mirror Imaging). The technique demands a prior self-assessment: before stepping into the adversary's shoes, the analyst must first articulate what *they* would do, and *why*, so the delta between the two perspectives becomes visible.

**The core cognitive move**: Most forecasting errors about adversary behavior come not from lack of information but from projecting one's own logic onto actors who do not share it. An adversary that looks "irrational" is almost always an adversary whose decision framework has not been correctly understood. Red Hat Analysis systematically surfaces that framework.

**Why this matters especially in cyber threat intelligence**: Threat actors operate within distinct professional cultures, technical constraints, organizational incentive structures, and risk tolerances. A ransomware affiliate operates under completely different logic than a nation-state operator, who differs from a hacktivist, who differs from an insider. Defaulting to analyst-centric reasoning ("I wouldn't risk that exposure, so they won't either") produces dangerously inaccurate threat assessments.

**What Red Hat Analysis protects against**:
- **Mirror Imaging** — Assuming the adversary thinks and values what the analyst thinks and values (primary target)
- **Anchoring Effect** — Locking on a prior estimate of adversary behavior without adjusting for new situational factors
- **Overrating Behavioral Factors / Fundamental Attribution Error** — Attributing all adversary behavior to malevolent intent while underestimating situational and structural pressures
- **Ignoring the Absence of Information** — Failing to ask what the adversary would *not* do and what that silence signals
- **Rejecting Evidence** — Holding to a prior behavioral prediction when the adversary's observed actions contradict it

**Important scope note**: Red Hat Analysis produces better forecasts for specific individuals with decision-making authority (authoritarian leaders, ransomware operators, insider threats) and small cohesive groups (APT teams, terrorist cells). Accuracy decreases significantly when the decision is made by consensus, constrained by a legislature, or dispersed across competing factions. When operating in those lower-confidence zones, hedge your language: "could," "possibly," "may" rather than "likely" or "will."

---

## Step 1: Ingest the input

Accept any of these forms:

- **Problem statement in chat** — e.g., "Run a Red Hat on how Sandworm would respond if their C2 infrastructure was burned by a major defender disclosure"
- **Pasted analysis or raw reporting** — Extract the analytic question about adversary behavior from the material
- **Uploaded document** — Read the file, identify the actor(s) of interest, the situation or stimulus, and the behavior to be forecasted
- **Post-ACH or post-KAC** — If a prior technique has flagged adversary intent as a key uncertainty, Red Hat Analysis is the natural follow-on to pressure-test the behavioral assumptions embedded in that analysis

The analytic question should be framed as: **"Given [stimulus or situation], what would [specific actor] do, and why?"**

---

## Step 2: Scope the analysis

Ask a single clarifying message covering only what is not already clear from the input:

1. **Actor specificity**: Is this a named APT group, a category of actor (e.g., "a ransomware-as-a-service affiliate"), a specific individual, or a composite? The more specific, the better the analysis.
2. **Stimulus or decision point**: What is the specific event, situation, or trigger the adversary is responding to? (e.g., "a public attribution report naming their group," "a law enforcement takedown of their payment infrastructure," "a defender deploying new EDR across the target environment")
3. **Cultural/operational expertise available**: What does the analyst already know about this actor's culture, incentives, TTP, and past decision patterns? Is there any supporting intelligence or open-source reporting on their behavior?
4. **Output format**: Inline in chat (fast, conversational), Word (.docx, formal product), or HTML (structured deliverable)?
5. **Depth**: Quick Red Hat (focus on the single most likely course of action + rationale) or full analysis (multiple courses of action ranked, with indicators)?

If the context makes answers obvious, proceed and state your assumptions.

---

## Step 3: Build the adversary profile

Before the analyst can step into the adversary's shoes, those shoes must be accurately characterized. Gather and synthesize everything known about:

### Identity and organizational context
- **Who are they?** Named group, nation-state nexus, criminal ecosystem role (operator, affiliate, broker, developer), hacktivist collective, insider, etc.
- **Organizational structure**: Hierarchical vs. flat; centralized command-and-control vs. independent cell structure; permanent vs. project-based
- **Known leadership or key decision-makers** (if relevant)

### Values, motivations, and goals
- **Primary motivation**: Financial gain, espionage, disruption, ideology, grievance, coercion, political signaling
- **Operational priorities**: Stealth vs. impact vs. speed vs. plausible deniability
- **What does "success" mean to this actor?** Define it precisely. A state APT team's definition of success may be staying undetected for five years; a ransomware operator's may be maximizing payments per campaign hour; a hacktivist's may be public embarrassment of the target
- **What do they fear?** Attribution, legal exposure, loss of tooling, betrayal by insiders, sanctions, operational failure visible to their patron/employer

### Constraints and situational pressures
- **Technical constraints**: Known capability gaps, tooling dependencies, infrastructure limitations, operational security (OPSEC) practices
- **Operational environment**: What country/jurisdiction are they operating from? What legal, political, or organizational pressure are they under?
- **Organizational pressures**: Is this actor under time pressure from a patron? Competing with other groups for the same target? Concerned about protecting their reputation in the criminal ecosystem?
- **Resource constraints**: Access to zero-days, skilled operators, infrastructure, money, time

### Historical behavioral patterns
- **Past decisions under similar stimuli**: How did this actor respond when attributed? When a C2 was sinkholed? When law enforcement disrupted their payment channel? When a target deployed strong defenses?
- **Known TTPs and preferred operational patterns**: MITRE ATT&CK framework mapping if applicable
- **Deviations from pattern**: Any prior instances where they behaved unexpectedly, and what explained those deviations?

> *Tip: Gaps in this profile are not just "unknowns" — they are collection requirements. Flag what would need to be known to make the Red Hat analysis more accurate.*

---

## Step 4: Analyst baseline — "What would I do, and why?"

This is the critical setup step that most analysts skip — and skipping it is why Mirror Imaging persists. Before simulating the adversary, the analyst must articulate their *own* response to the same stimulus and the reasoning behind it.

Ask explicitly: **"If I were facing this situation [same stimulus, same decision point], what would I do? And what values, assumptions, and constraints are driving that answer?"**

Document the baseline response and, crucially, the underlying logic:
- What outcome am I optimizing for?
- What risks am I most sensitive to?
- What resources am I assuming I have available?
- What do I assume about the other side's detection capability or response?
- What would make me abandon this course of action?

**Now compare**: Go item by item through the adversary profile (Step 3) and ask: does this adversary share these values? These constraints? These risk tolerances? These assumptions about the operational environment?

The **delta** — where the adversary's logic diverges from the analyst's — is where the Red Hat analysis does its real work. Each divergence is an opportunity to generate a more accurate forecast of adversary behavior.

> *Example: An analyst might assume that public attribution would deter future operations (because they value their professional reputation and fear legal consequence). An APT operator working under state cover may assess that attribution has zero operational consequence and view it primarily as a signal that their cover story held — and thus continue operations unchanged. That delta is the insight.*

---

## Step 5: Red Hat shift — "What would the adversary do, and why?"

Now step fully into the adversary's frame. Commit to it. Speak in first person. Think from inside their operating environment, not from outside observing it.

Ask: **"Given everything I know about this actor's values, constraints, motivations, and operating culture — and given the stimulus in front of me — what would I do if I were them? What would I NOT do? And why?"**

### Guided questions for the Red Hat perspective

**Decision framing**:
- How do I [the adversary] perceive this situation? Is this a threat, an opportunity, an ambiguous signal, or a non-event?
- What outcome am I most trying to achieve right now? What would getting that outcome require?
- What options are available to me, and which are off the table given my current resources and constraints?

**Risk calculus**:
- What risks am I most sensitive to? What risks am I willing to accept that the analyst might not expect?
- What would have to go wrong for this course of action to constitute an unacceptable loss for me?
- How do I perceive the defender's capability to detect, respond to, or attribute my actions? Is this perception accurate?

**Organizational and personal pressures**:
- Who do I answer to? What are they expecting from me right now? What happens if I fail or if I succeed too visibly?
- Do I have allies, partners, or third-party dependencies that constrain my options?
- Am I under time pressure? Resource pressure? Reputational pressure within my ecosystem?

**Adversarial reasoning**:
- What does the defender expect me to do? What would doing the opposite achieve?
- Have I done something similar before? How did that go? What would I do differently?
- What information am I acting on, and how confident am I in it? Could I be being deceived or set up?

### First-person output (optional but powerful)

Consider drafting a short first-person document as the adversary: an internal decision memo, an operator tasking order, a conversation between the threat actor and their team. This format forces the analyst off analyst-speak and into the adversary's actual decision logic. It is also highly effective for communicating Red Hat findings to decision makers.

> *Example: "We have just been publicly named in the [company X] report. My read: attribution was based on our [toolset]. Our cover story [claim Y] held. Law enforcement has no jurisdictional reach here. Three options: (1) go quiet for 90 days and retool; (2) continue current operations — they already know who we are, additional operations cost us nothing in exposure; (3) pivot to a new campaign against [target Y] to demonstrate we are undeterred. I recommend option 2 with a parallel track on option 3…"*

---

## Step 6: Generate adversary courses of action

Synthesize the Red Hat analysis into a structured set of adversary courses of action (COAs). For each COA:

- **Label**: Short descriptive name capturing the core decision logic (not "COA 1")
- **Description**: What the adversary does, in concrete operational terms
- **Rationale**: Why, from the adversary's perspective, this COA makes sense — what they are optimizing for, what risks they are accepting
- **Enabling conditions**: What must already be true for this COA to be feasible
- **Key assumptions**: The most fragile assumption in this COA's logic — if this is wrong, the COA fails or shifts
- **Likelihood**: HIGH / MEDIUM / LOW — from the adversary's perspective, how attractive is this option relative to alternatives?

### The two COAs that matter most

Intelligence and defense planning typically care most about:

1. **Most Likely COA (MLCOA)** — the action the adversary will probably take based on their historical patterns, current pressures, and rational calculus
2. **Most Dangerous COA (MDCOA)** — the action that would be most harmful to friendly interests if executed, even if not the most probable

These two COAs are not always the same. Flag explicitly when they differ — that gap is where the most consequential planning decisions live.

> *In CTI: The MLCOA for a ransomware operator facing law enforcement disruption might be "reconstitute infrastructure in a new jurisdiction and resume operations within 30 days." The MDCOA might be "pivot to a destructive wiper payload deployed against critical infrastructure to demonstrate continued capability and coerce a government response." The MDCOA is less likely but demands defensive preparation regardless.*

---

## Step 7: Validate against known evidence

Red Hat Analysis is adversary-perspective reasoning, not unconstrained speculation. After generating COAs, validate each against the actual evidence base:

For each COA, ask:
- **Is this COA consistent with what we have already observed?** (e.g., known TTPs, past behavior, current infrastructure activity)
- **Are there any observations that are *inconsistent* with this COA?** — Give these serious weight; the adversary may not have chosen this option for a reason not yet visible
- **What observable indicators would we expect to see if this COA were already underway?** (Feed these into monitoring)
- **Is there any observed evidence that an alternative, less-considered COA is actually in progress?**

> *If a COA survived the Red Hat simulation but fails against the evidence base, it requires revision or downgrade — not suppression. The evidence inconsistency is a finding in itself.*

---

## Step 8: Report the conclusions

### Required output structure

**Header**: Actor | Stimulus | Date | Analyst (if provided)

**Section 1 — Adversary Profile Summary**
Key characteristics of the actor relevant to forecasting behavior: motivation, organizational structure, risk tolerance, technical constraints, historical patterns, and any significant known information gaps.

**Section 2 — Analyst Baseline**
What the analyst concluded they would do in the same situation, and the key values/assumptions driving that response. Explicitly identify the 2–3 most important points of divergence between analyst logic and adversary logic.

**Section 3 — Red Hat Assessment**
The first-person adversary analysis: how the adversary perceives the situation, what they are optimizing for, what constraints they are operating under, and what they are most likely to do. If a first-person narrative was drafted (Step 5), include it as an annex.

**Section 4 — Adversary Courses of Action**
All viable COAs with labels, descriptions, rationale, enabling conditions, key assumptions, and likelihood ratings. Explicitly identify MLCOA and MDCOA.

**Section 5 — Collection Indicators**
Observable indicators that would signal which COA the adversary is executing — and which would provide early warning of the MDCOA. For CTI, map these to specific MITRE ATT&CK techniques, telemetry sources, or collection platforms where applicable.

**Section 6 — Analytic Confidence and Caveats**
An honest assessment of how much cultural and operational expertise was available for this analysis and how that affects confidence. Use "possibly" and "could" when cultural expertise is limited; reserve "likely" and "probably" for high-confidence assessments grounded in rich actor knowledge. Identify specific collection requirements that would increase accuracy.

---

## Step 9: Deliver in the requested format

**Inline chat**: Markdown. Use tables for the COA section. Best for rapid operational analysis and conversational review.

**Word (.docx)**: Use the `docx` skill. Formal report with proper headings, a one-paragraph executive summary, and a structured COA table. Appropriate for product distribution, briefings, and peer review.

**HTML**: Standalone file with filterable COA tables and a clear visual separation between MLCOA and MDCOA. Good for collaborative review or team exercises.

> ⚠️ **Handling sensitive Red Hat products**: First-person adversary narratives — especially those that describe specific attack vectors, target selection logic, or vulnerability exploitation reasoning — can constitute sensitive material. Flag for restricted distribution if the analysis reveals exploitable patterns or attack planning logic that an adversary could benefit from if the document were compromised.

---

## Analyst principles

**Commit to the adversary's frame — don't hedge.** The power of Red Hat Analysis depends entirely on the analyst genuinely adopting the adversary's perspective. If you are writing "the adversary would probably think..." you have already failed. Write "I [the adversary] am thinking..." The reframe is the technique.

**The baseline step is not optional.** Skipping the self-assessment (Step 4) means you will never identify where Mirror Imaging is distorting your forecast. The delta between "what I would do" and "what they would do, given their actual values and constraints" is the central product.

**Cultural ignorance degrades everything.** Red Hat Analysis is only as good as the analyst's understanding of the adversary's cultural, organizational, and operational context. When that understanding is thin, the analysis will drift toward Mirror Imaging despite best efforts. In those situations, be explicit about the limitation, bring in subject matter experts, and hedge the language accordingly.

**Evidence inconsistencies are findings.** If the most likely COA from the Red Hat simulation is inconsistent with observed adversary behavior, do not dismiss the observation. Ask: What is the adversary optimizing for that we did not account for? Is there a constraint we missed? Is the observed behavior a deliberate deception?

**Both COAs matter to planners.** Defenders and decision makers need the MLCOA to allocate resources today and the MDCOA to plan for contingencies. Providing only the most likely answer without the most dangerous one is an incomplete product.

**The technique is not attribution.** Red Hat Analysis forecasts *behavior*; it does not confirm *identity*. Do not conflate "this actor would likely do X" with "therefore the actor who did X is this group." Attribution is a separate analytic process (see ACH and Diagnostic Reasoning).

---

## Relationship to other techniques

**Circleboarding™ (§6.4)** — Use Circleboarding first to map the Who, What, How, When, Where, and Why of the actor and the situation. A completed Circleboard provides most of the adversary profile inputs for Step 3 of Red Hat Analysis.

**Key Assumptions Check (§7.1)** — Run a KAC on the adversary profile assumptions before the Red Hat shift. Fragile assumptions about the adversary's motivations or constraints can be identified and challenged before they propagate into the COA generation. KAC also reveals which assumptions are load-bearing for the MLCOA.

**Analysis of Competing Hypotheses (§7.6)** — When multiple competing hypotheses about adversary behavior exist, ACH provides a systematic framework for evaluating them against evidence. Red Hat Analysis generates the hypotheses and rationale; ACH evaluates which hypothesis the evidence best supports.

**Deception Detection (§7.8)** — Red Hat Analysis is a prerequisite for Deception Detection. To identify a deception operation, the analyst must first know what the adversary would want the defender to believe — which is precisely the Red Hat output. If the Red Hat simulation reveals that the adversary has strong motive to deceive, escalate to formal Deception Detection.

**Diagnostic Reasoning (§7.5)** — After generating the MLCOA and MDCOA, use Diagnostic Reasoning to evaluate whether newly observed indicators are consistent with one COA but not others. This gives the Red Hat outputs operational utility as an ongoing collection-tasking tool.

**Indicators Generation, Validation, and Evaluation (§9.11)** — The collection indicators from Step 8 should be validated and formalized using the IGVE framework. Red Hat Analysis is one of the most productive generators of collection-ready behavioral indicators in CTI.

**Red Cell / Red Team Analysis** — Red Hat Analysis differs from organizational Red Cell/Red Team Analysis in scope and resource: Red Hat can be conducted by any analyst with access to cultural expertise, and its goal is to *forecast* adversary behavior. Red Cell/Red Team is conducted by dedicated organizational units whose goal is to *challenge* the conventional wisdom of established analysts or an opposing planning team. Use Red Hat when you need a behavioral forecast; use Red Cell/Red Team when you need institutional challenge to an entrenched analytic consensus.
