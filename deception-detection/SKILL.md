---
name: deception-detection
description: |
  Performs a structured Deception Detection analysis — a core Diagnostic SAT (Pherson & Heuer, §7.8). Applies four checklists — MOM, POP, MOSES, EVE — to assess adversary intent and capability to deceive, source vulnerability to manipulation, and evidence integrity.

  Trigger on: "could this be deception", "is this a deception operation", "run a deception check", "detect deception", "deception detection", "could we be getting played", "is this disinformation", "influence operation", "could this be a plant", "is this a false flag", "denial and deception", "D&D analysis", "is our source compromised", "run MOM POP MOSES EVE", "could this reporting be fabricated". Also trigger when reporting seems too convenient, when an ACH deception hypothesis needs formal escalation, or when a source's track record or access is in question.

  Accepts a typed scenario, pasted reporting, or uploaded document. Output can be inline chat, Word .docx, or HTML.
---

# Deception Detection

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §7.8 — drawing on Richards J. Heuer Jr., "Cognitive Factors in Deception and Counterdeception" (1982), and the Bennett & Waltz counterdeception framework*

## Purpose

Deception Detection uses four structured checklists — **MOM, POP, MOSES, and EVE** — to help analysts determine when to be alert for deception, whether deception is actually present, and what to do to avoid being misled.

Deception is any deliberate act by an adversary intended to influence the analyst's perceptions, decisions, or actions to the advantage of the deceiver. This includes active deception (feeding false information), denial (concealing true information), and hybrid operations that mix genuine intelligence with fabricated material to lower the analyst's guard.

### Heuer's Fundamental Paradox

This paradox must be held in mind throughout the entire analysis:

> *"The accurate perception of deception in counterintelligence analysis is extraordinarily difficult. If deception is done well, the analyst should not expect to see any evidence of it. If, on the other hand, deception is expected, the analyst often will find evidence of deception even when it is not there."*
> — Richards J. Heuer Jr.

This means the absence of evidence of deception is not evidence of its absence — and the presence of apparent deception indicators does not confirm deception. The checklists below are tools to raise or lower plausibility, not to deliver a verdict.

---

## Step 1: Ingest the input

Accept any of these forms:

- **Problem statement in chat** — e.g., "Run a deception check on the reporting we're getting from Source Alpha on the North Korean missile program"
- **Pasted reporting or analysis** — Identify the specific claim, source, and context under examination
- **Uploaded document** — Read the document and identify the reporting being scrutinized, the source chain, and the analytic judgment at stake

The object of analysis should be clearly defined: what specific reporting, source, or scenario is being assessed for possible deception?

---

## Step 2: Scope and confirm with the user

Ask one short clarifying message covering:

1. **Output format**: Inline in chat (fast, good for quick operational checks), Word document (.docx, appropriate for formal CI or counterdeception products), or HTML (structured checklist report with color-coded risk flags)?
2. **Known context**: Is there a known adversary actor, source name/type, or analytic assessment already in play? The more context provided, the richer the analysis.
3. **ACH integration**: Should the output be formatted as evidence items for inclusion in an ACH matrix? (Recommend yes if ACH is already underway or planned.)

If the request makes these obvious — "quick check" → inline, "formal report" → .docx — skip asking and proceed.

---

## Step 3: Assess the trigger conditions

Before applying the checklists, run the trigger screen. Deception Detection is warranted — and urgency increases — when any of the following apply:

| Trigger Condition | Explanation |
|---|---|
| Analysis hinges on a **single critical piece of reporting** | Single-source dependence is the deceiver's ideal leverage point |
| Information arrives at a **strategically critical time** | When either party has much to gain or lose, deception payoff is highest |
| Accepting the information would cause **significant resource diversion** | Classic strategic deception objective: tie down enemy resources |
| Accepting the information would require **revising a key assumption or judgment** | The deceiver benefits from shifting the analyst's mental model |
| The potential deceiver may have **feedback visibility** into how the deception is being processed | Feedback loop enables refinement of the operation in real time |
| The source's **bona fides are questionable** | Direct manipulation becomes possible |
| The adversary has a **documented history of deception** | Prior behavior is the best predictor of future behavior |

Note how many triggers apply. Three or more is a strong signal to apply the full checklist suite.

---

## Step 4: Apply the MOM checklist — Motive, Opportunity, and Means

MOM evaluates the adversary's *capability and motivation* to run a deception operation. All three elements must be present for a serious deception threat to exist.

### Motive
- What specific goals or strategic interests would the adversary advance by deceiving you?
- Would the adversary benefit from causing you to: overestimate a threat? Underestimate it? Divert resources? Delay action? Take a specific action prematurely?
- Is there a documented strategic logic for deceiving you at this particular time?
- **Probe**: If you accepted this information as genuine, what would you probably do next? Does that action benefit the adversary?

### Opportunity (Channels)
- What mechanisms does the adversary have available to feed deceptive information into your collection systems?
  - Human sources or subsources under their influence or control?
  - SIGINT channels the adversary knows you collect?
  - Open-source or media channels they can manipulate?
  - Liaison or diplomatic channels?
- Has the adversary previously exploited any of these channels?

### Means
- Does the adversary have the technical, organizational, and operational capacity to execute a sustained deception of this complexity?
- **Costs**: What genuine intelligence or sensitive information would the adversary need to sacrifice to establish the credibility of the deception channel? Is that sacrifice consistent with what they've done?
- **Risks**: What would happen if the deception were discovered? What is the adversary's risk tolerance?
- **Feedback mechanism**: Does the adversary have visibility into whether their deception is being accepted — e.g., through a turned source, liaison reporting, SIGINT, or observed behavioral change on your side? Without feedback, sustaining calibrated deception is very difficult.

**MOM Assessment**: State whether the adversary has FULL, PARTIAL, or INSUFFICIENT motive, opportunity, and means. If all three are present, the deception hypothesis warrants serious weight.

---

## Step 5: Apply the POP checklist — Past Opposition Practices

POP examines the adversary's track record to determine whether their deception history makes the current scenario more or less plausible.

- Does the adversary have a documented history of conducting denial and deception operations?
- Does the **current scenario fit the pattern** of past deceptions? Consider:
  - Target type (analysts, policymakers, military commanders?)
  - Channel used (human sources, media, diplomatic?)
  - Timing (crisis period, pre-election, prior to military action?)
  - Objective (strategic distraction, masking capability, inducing premature action?)
- If the current scenario does **not** fit historical patterns, is there a plausible explanation for why the adversary would use a novel approach now?
  - Changed strategic circumstances?
  - Lessons learned from past failures?
  - New capabilities or channels available?
- Are there other historical precedents from comparable actors or situations?

**POP Assessment**: State whether the current situation is CONSISTENT WITH, INCONSISTENT WITH, or UNKNOWN relative to historical deception patterns. An adversary with a well-documented deception history operating in a familiar pattern substantially raises the prior probability of deception.

---

## Step 6: Apply the MOSES checklist — Manipulability of Sources

MOSES evaluates the vulnerability of the source chain to adversary manipulation. A source can be genuinely reliable in general but still compromised in a specific case.

- **Control or manipulation**: Is there any possibility the source — or a subsource in the chain — is under the control, influence, or surveillance of the potential deceiver?
  - Has the source been in a position where the adversary could have recruited, coerced, or assessed them?
  - Are there any unexplained changes in the source's access, lifestyle, or behavior?
- **Basis of reliability**: What is the actual evidentiary basis for judging this source reliable?
  - Past reporting accuracy (and how was it verified)?
  - Access assessment (have they been confirmed to have genuine access to what they're reporting on)?
  - Independent corroboration of key claims?
- **Direct vs. indirect access**: Does the source have **direct access** to the information reported, or are they relaying what a subsource told them?
  - *The subsource can be more critical than the source.* Deception operations frequently insert false information at the subsource level, relying on the trusted source to unwittingly carry it forward.
  - Has the subsource's identity and access been independently verified?
- **Track record granularity**: Is the source's track record genuinely positive, or is it good enough on peripheral matters while being unverifiable on the critical claims?
  - A classic deception technique: establish credibility with accurate, low-stakes reporting, then deliver the false payload.

**MOSES Assessment**: Rate source vulnerability as HIGH, MEDIUM, or LOW. Flag any part of the source chain where manipulability cannot be ruled out.

---

## Step 7: Apply the EVE checklist — Evaluation of Evidence

EVE interrogates the actual evidence body for internal consistency, corroboration, and anomalies that would be expected if the material were fabricated or selectively constructed.

- **Chain of evidence integrity**: Has the entire chain — from original reporting through translation, transcription, and dissemination — been checked for accuracy and fidelity?
- **Critical evidence verification**: Has the most critical single piece of evidence (the "load-bearing" claim) been independently verified, not just accepted?
- **Cross-source consistency**: Does the reporting from this source conflict with reporting from other collection disciplines (e.g., HUMINT vs. SIGINT vs. OSINT vs. imagery)?
  - Genuine intelligence tends to be multiply corroborated over time.
  - Deception operations tend to over-corroborate the key claim (the deceiver controls or influences multiple channels) while leaving anomalies in peripheral details.
- **Corroboration test**: Do independent sources provide genuine corroboration — or do they all trace back to the same original reporting, creating the illusion of multiple-source confirmation?
- **Absence of expected evidence**: What evidence *should* be present if the reported activity is real and at the scale reported?
  - Are there logistics signatures? Financial trails? Personnel movements? Physical infrastructure changes?
  - If activity of this significance is occurring, what corroborating indicators are missing, and why?
  - *The absence of expected evidence is significant evidence.*
- **"Too good" test**: Is the reporting suspiciously complete, timely, or directly responsive to your known intelligence requirements? High-quality reporting that answers exactly what you most need to know warrants extra scrutiny.

**EVE Assessment**: State whether the evidence body is ROBUST, MIXED, or FRAGILE. Flag specific gaps or anomalies that are inconsistent with genuine reporting.

---

## Step 8: Apply the Rules of the Road

These operational principles should inform both the analysis and any recommendations going forward:

1. **Avoid overreliance on a single source.** Single-source dependence is the deceiver's greatest asset.
2. **Seek and heed the opinions of those closest to the reporting.** The case officer, collection manager, or regional expert who developed or handled the source often has instinctive concerns that deserve airing.
3. **Be suspicious of human sources or subsources who have not been seen or whose access is unclear.** Unverified access is unverified access — regardless of how good the reporting sounds.
4. **Do not rely exclusively on verbal intelligence.** Look for material evidence — documents, imagery, addresses, phone numbers, physical indicators — that can be independently verified.
5. **Be suspicious of information that plays strongly to your own known biases and preferences.** The adversary knows what you want to believe. A sophisticated deception operation delivers exactly that.
6. **Watch for a pattern of initial accuracy followed by repeated failure with convenient explanations.** Establishing credibility with good early reporting and then inserting false payload later is the oldest trick in the book.
7. **Generate a full hypothesis set including a deception hypothesis from the outset.** Once an analyst is anchored on a non-deception explanation, cognitive defenses against deception collapse.
8. **Know both the limitations and the capabilities of the potential deceiver.** Overestimating the adversary's capability leads to false deception detections; underestimating it leads to missed ones.

---

## Step 9: Synthesize the deception assessment

Bring the four checklist assessments together into an integrated judgment.

### Deception plausibility matrix

| Checklist | Finding | Weight |
|---|---|---|
| **MOM** | Adversary motive, opportunity, and means? | Foundation — if MOM is absent, deception is implausible |
| **POP** | Consistent with historical deception patterns? | Historical precedent raises or lowers prior probability |
| **MOSES** | Source chain vulnerable to manipulation? | Determines *how* deception could reach the analyst |
| **EVE** | Evidence body internally consistent and corroborated? | Final evidential test |

### Overall deception plausibility rating

Apply one of these ratings based on the combined checklist findings:

| Rating | Criteria |
|---|---|
| **HIGH** | MOM fully present + POP consistent + MOSES vulnerability identified + EVE shows gaps/anomalies |
| **MEDIUM-HIGH** | MOM present + two other checklist flags |
| **MEDIUM** | MOM present + one other checklist flag, or MOM partial + broader concerns |
| **LOW-MEDIUM** | MOM partial + evidence appears robust + source chain appears sound |
| **LOW** | MOM absent or clearly insufficient |

**Critical caveat**: HIGH plausibility does not confirm deception. LOW plausibility does not rule it out. Return always to Heuer's paradox: if deception is done well, you should expect the rating to look low.

### Analytic implications

State what the deception hypothesis, if true, would imply:
- What is the deceiver trying to make you believe?
- What decision or action is the deception designed to produce?
- What would be masked or concealed if the active reporting is a cover story?
- What would the real situation look like — and how would you collect against it?

---

## Step 10: Produce the output

Structure the output as follows:

### Required output structure

**Header**: Subject | Date | Classification | Analyst (if provided)

**Section 1 — Deception Concern Summary**
The specific reporting or scenario under scrutiny and the reason deception analysis was triggered (which trigger conditions applied).

**Section 2 — MOM Analysis**
Findings on adversary motive, channels (opportunity), and means. MOM assessment rating.

**Section 3 — POP Analysis**
Historical deception pattern assessment. Consistency finding.

**Section 4 — MOSES Analysis**
Source chain vulnerability assessment. MOSES rating with specific flags.

**Section 5 — EVE Analysis**
Evidence body integrity assessment. EVE rating with specific anomalies or gaps noted.

**Section 6 — Overall Deception Plausibility**
Combined rating with reasoning. Statement of what the deception hypothesis, if true, would mean for current analysis.

**Section 7 — Recommendations**
Specific collection, source validation, or analytic steps to reduce deception uncertainty. These typically include:
- Independent corroboration requirements
- Source access verification steps
- Alternative collection disciplines to consult
- Indicators to monitor that would raise or lower deception plausibility

**Section 8 — ACH Feed (if requested)**
List of deception-related findings formatted as evidence items (with credibility ratings) ready for insertion into an ACH matrix.

---

**Inline chat**: Use markdown tables for the checklist summaries. Suitable for operational reviews and rapid checks.

**Word (.docx)**: Use the `docx` skill. Formal counterdeception report with structured sections and executive summary. Appropriate for CI reviews, source validation requests, or formal escalation products.

**HTML**: Standalone file with color-coded risk ratings per checklist (red/amber/green). Useful for team review or briefings.

---

## Analyst principles

**Cognitive bias is the deceiver's primary weapon.** The checklists exist to interrupt automatic acceptance. Confirmation Bias (seeking only confirming evidence), Satisficing (accepting "good enough" reporting without probing), Evidence Acceptance Bias (accepting data as true because it supports your case), and Availability Heuristic (over-weighting vivid or recent reporting) are all exploitable. The discipline of the checklist is what creates resistance.

**The most dangerous deception is the one that tells you what you already believe.** The adversary researches your biases. Information that validates your existing assessment, arrives when you need it most, and comes through a trusted channel deserves the highest scrutiny — not the least.

**Protect the source relationship — but not at the cost of analytical integrity.** The natural reaction to concerns about a source is to defend them, especially if the relationship was hard to build. This is precisely the psychological dynamic a sophisticated deception operation exploits. Analytical integrity requires the ability to suspend that loyalty long enough to complete the checklist.

**A negative finding is still a finding.** If the checklists produce LOW deception plausibility, document that assessment and the reasoning behind it. This creates an audit trail and forces the analyst to commit to their confidence level — which itself improves calibration over time.

**Document dissent.** In a team setting, the most valuable output is often the specific checklist cells where analysts disagree. Those disagreements reveal different assumptions about adversary capability, source reliability, or evidence interpretation — all of which deserve explicit examination.

---

## Relationship to other techniques

**Analysis of Competing Hypotheses (ACH)** — The natural partner technique. Findings from MOM, POP, MOSES, and EVE should be entered as evidence items in the ACH matrix when deception is one of the hypotheses being evaluated. If an ACH deception hypothesis remains viable after full matrix scoring, escalate to formal Deception Detection.

**Key Assumptions Check (KAC)** — Run a KAC before or in parallel with Deception Detection. The KAC will often surface the assumption "the reporting we're relying on is genuine" — which is precisely the assumption Deception Detection is designed to test.

**Premortem Analysis** — Useful if Deception Detection produces a MEDIUM or higher rating but the team remains anchored on the non-deception hypothesis. Premortem imagines the deception hypothesis is true and works backward to explain how it was missed.

**Indicators Generation (§9.11)** — The recommendations from Step 9 (Section 7) generate actionable deception indicators for ongoing collection and monitoring.
