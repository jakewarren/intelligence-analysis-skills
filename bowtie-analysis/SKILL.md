---
name: bowtie-analysis
description: |
  Performs Bowtie Analysis — Decision Support SAT (Pherson & Heuer §10.2, T46). Maps causes and consequences of a central event, with barriers or controls on both sides. Supports threat/risk mode and opportunity mode. Use for threat modeling, incident causation, attack-chain analysis, adversary capability assessment, barrier mapping, and security control gap identification.

  Trigger on: "bowtie analysis", "run a bowtie", "map the causes and consequences", "threat modeling", "attack chain analysis", "map the controls", "where are my defensive gaps", "escalation factors", "what caused this incident", "control gap analysis", "what could stop this attack", or "barrier analysis". Also trigger when an analyst needs to trace causal chains, assess control adequacy, or find leverage points for preventing or mitigating an event.

  Accepts a typed problem, pasted reporting, or uploaded document. Output: inline chat, .docx, or HTML with visual bowtie diagram.
---

# Bowtie Analysis

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §10.2 (T46) — originally developed by the University of Queensland (1979); industrialized by the oil and gas sector following the Piper Alpha disaster (1988)*

## Purpose

Bowtie Analysis maps the **causes** and **consequences** of a disruptive central event, with **barriers or controls** inserted between causes and the event (left side) and between the event and consequences (right side). **Escalation factors** — conditions that cause barriers to fail or controls to be bypassed — attach to individual barriers and complete the picture.

The name comes from the diagram's shape: causes converge on the left, consequences fan out on the right, and the central event is the "knot."

The technique is explicitly bidirectional:

- **Risk/Threat mode**: The central event is a hazard or security incident. Causes are threats or attack vectors. Barriers are defensive controls. The analytical goal is to identify where barriers are missing, weak, or subject to escalation factor failure.
- **Opportunity mode**: The central event is a favorable development — an adversary OPSEC failure, a law enforcement disruption of a threat actor, a new collection capability coming online. Causes are enabling trends. Accelerators speed up the event's occurrence. Amplifiers maximize its benefit.

In the CTI context, Bowtie Analysis excels as a **structured threat modeling method** that produces decision-relevant output. Unlike informal threat modeling, it explicitly forces analysts to identify barriers, test barrier completeness, and trace escalation paths — making it directly actionable for defenders and decision makers.

Bowtie Analysis counters several cognitive failure modes: **Mental Shotgun** (jumping to the first cause without mapping others), the **Availability Heuristic** (overweighting causes that come easily to mind), **Satisficing** (accepting the first "good enough" set of barriers), **Lacking Sufficient Bins** (failing to categorize causes or consequences properly), **Overrating Behavioral Factors** (attributing incidents to human error alone without mapping structural causes), and **Assuming a Single Solution** (identifying one barrier as sufficient when several may be needed).

---

## When to use it

Bowtie Analysis is most valuable when:

- **Pre-incident threat modeling**: An organization needs to understand whether its defensive controls are adequate against a known threat vector — e.g., before deploying a new internet-facing system, before a high-risk geopolitical period, or as part of a red team engagement debrief.
- **Post-incident causation analysis**: An incident has occurred and the organization needs to understand not just *what* happened but *why controls failed* — escalation factors that bypassed barriers are often the most actionable finding.
- **Adversary capability assessment**: A threat actor has a known capability (e.g., a ransomware group's established TTPs). Map their attack chain as the left side, your controls as barriers, and potential outcomes as consequences to identify where you are most exposed.
- **Opportunity exploitation**: A threat actor's infrastructure has been disrupted, a key operative arrested, or a vulnerability in the adversary's supply chain identified. Map the enabling trends, barriers to exploitation, and amplifiers to maximize benefit.
- **Lessons-learned / after-action review**: Map what should have stopped the event, what did stop it, what failed, and why.

Bowtie Analysis is NOT the right tool when:
- You need to evaluate **which of several competing explanations** best fits available evidence — use ACH (§7.6).
- You need to **generate and stress-test hypotheses** — use MHG (§7.4) or What If? (§8.2.4).
- You need to **evaluate individual pieces of evidence** for diagnostic value — use Diagnostic Reasoning (§7.5).

---

## Step 1: Ingest the input

Accept any of the following:

- **Problem statement in chat** — e.g., "Run a bowtie on a ransomware attack against our OT environment" or "Map the causes and consequences of a supply chain compromise"
- **Pasted reporting or incident brief** — Extract the central event from the reporting; identify named causes and consequences already mentioned; note any controls or barriers already described
- **Uploaded document** — Read the file; identify the focal event, any described attack chain, and any mentioned defensive measures or outcomes
- **Output from another SAT** — A Hi-Lo Analysis, ACH, or Red Hat session may have identified a focal event that now warrants full bowtie mapping

---

## Step 2: Ask one clarifying question set

Before beginning, send a single short message covering:

1. **Mode**: Is this a **risk/threat** event (mapping how a bad thing happens) or an **opportunity** event (mapping how a favorable development can be accelerated)? If unclear, state your assumption.
2. **The central event**: State precisely what the analyst believes the central event is (or should be). Confirm before proceeding.
3. **Depth**: Quick operational mapping (causes + barriers + consequences) or full analysis (includes escalation factors, control assessment, recommendations)?
4. **Output format**: Inline chat (markdown), Word .docx (formal product), or HTML (visual bowtie diagram)?

If the request is specific enough to make these obvious — e.g., a clearly described incident, a follow-on from a Red Hat session — state your assumptions and proceed without asking.

---

## Step 3: Define the central event

The central event — also called the **Risk Event** (threat mode) or **Opportunity Event** (opportunity mode) — is the **knot** of the bowtie. Everything on the left leads to it; everything on the right flows from it.

Defining the central event precisely is the single most important step. A vague event produces a vague bowtie that is not actionable.

**Good (threat mode)**: *"Ransomware deployment across IT and OT network segments, causing loss of visibility and control of industrial control systems and simultaneous encryption of backup infrastructure."*

**Poor**: *"A cyberattack."*

**Good (opportunity mode)**: *"Law enforcement seizure of the threat actor's primary C2 infrastructure and arrest of two key operators, degrading the group's ability to conduct operations for an estimated 6–12 months."*

**Poor**: *"The threat actor getting disrupted."*

Define:
- **What** is the specific event?
- **Who** is involved (threat actor, victim organization, affected systems)?
- **What threshold** marks the event as having occurred — i.e., how do we know it happened?
- **Is the event historical** (already occurred, now mapping causation) or **prospective** (anticipated, now mapping prevention and response)?

---

## Step 4: Map the causes (left side)

List all causes of the central event. In threat mode, causes are **threats** or **attack vectors**. In opportunity mode, causes are **enabling trends** or **conditions** that make the favorable event possible.

### Threat mode — attack vector enumeration

For a security incident, causes are the entry points, conditions, or adversary actions that can lead to the event. Think across:

| Category | Example causes |
|----------|---------------|
| **Initial access vectors** | Spearphishing, drive-by compromise, valid account abuse, supply chain injection, public-facing application exploitation |
| **Enabling conditions** | Unpatched vulnerability, misconfigured cloud storage, over-privileged service accounts, absent MFA, default credentials |
| **Insider factors** | Malicious insider, negligent user, social engineering victim |
| **Third-party / supply chain** | Compromised vendor update, malicious open-source dependency, managed service provider access |
| **Physical / environmental** | Physical access to network jack, rogue device implant |

### Opportunity mode — enabling trend enumeration

For an opportunity event, causes are the conditions or developments that, if present, make the favorable outcome achievable. Examples in CTI:

- Threat actor's OPSEC failures accumulating over time
- Law enforcement partnership formalizing
- New technical collection capability operational
- Threat actor's key personnel under financial pressure (HUMINT indicator)
- Threat actor's malware using infrastructure with exposed registration data

### Guidance for both modes

- **Be specific**: "Phishing" is too vague; "credential-harvesting spearphish targeting IT helpdesk personnel impersonating Active Directory password reset" is actionable.
- **Be exhaustive**: Brainstorm across attack surface systematically. In cyber, use MITRE ATT&CK Initial Access tactics as a checklist to avoid omission.
- **Prioritize but don't prune yet**: Include lower-probability causes. The barrier mapping step will reveal which ones are inadequately controlled.
- Place each cause on the left side of the diagram, with a line connecting it to the central event.

---

## Step 5: Map the consequences (right side)

List all consequences of the central event — what flows from the event if it occurs (threat mode) or what beneficial outcomes arise (opportunity mode).

### Threat mode — consequence enumeration

Consequences in security incidents typically cascade across layers:

| Layer | Example consequences |
|-------|---------------------|
| **Operational** | System downtime, loss of visibility into OT process, degraded service delivery |
| **Data** | Exfiltration of sensitive data, destruction of records, ransomware encryption |
| **Financial** | Ransom payment, remediation cost, regulatory fine, lost revenue |
| **Strategic** | Intelligence loss, capability degradation, competitive disadvantage |
| **Reputational** | Customer trust damage, media coverage, executive accountability |
| **Regulatory/Legal** | Mandatory disclosure, breach notification, litigation |
| **Geopolitical** | Diplomatic friction, escalation pressure, alliance implications |

### Opportunity mode — benefit enumeration

For opportunity events:
- Operational gain (disruption to adversary capability, intelligence windfall)
- Strategic gain (changed adversary behavior, deterrence signal sent)
- Collection gain (new access, new sources, new technical telemetry)
- Partnership gain (demonstrated cooperation cements relationships)

### Guidance for both modes

- **Follow the cascade**: Secondary and tertiary consequences routinely exceed the immediate primary impact. A ransomware encryption event (primary) triggers: operational shutdown → supply chain disruption → customer contract penalties → regulatory notification → legislative response. Map at least two layers deep.
- **Be specific**: "Reputational damage" is too vague; "public disclosure of 2.3 million customer records triggers class-action filing and stock price decline of 15-20%" is actionable.
- Place each consequence on the right side of the diagram, with a line connecting it from the central event.

---

## Step 6: Map preventive barriers or accelerators (left side — between causes and the central event)

For each cause on the left side, identify the **barriers** (threat mode) or **accelerators** (opportunity mode) that sit between that cause and the central event.

### Threat mode — preventive barriers

A **preventive barrier** is a control that, if functioning, stops the cause from leading to the central event.

For each cause identified in Step 4, ask: *"What must fail for this cause to lead to the central event?"* The inverse — what must succeed — is the barrier.

| Cause | Preventive barrier |
|-------|-------------------|
| Spearphishing → credential theft | Email security gateway (DMARC/DKIM/SPF), phishing-resistant MFA |
| Exploitation of unpatched vulnerability | Patch management process, vulnerability scanning, network segmentation |
| Compromised vendor update | Software supply chain integrity checks (code signing, SBOM validation), vendor access controls |
| Insider credential abuse | Privileged access management, user behavior analytics, least-privilege enforcement |

**Critical**: For each barrier, explicitly assess whether the barrier is **present**, **partially present**, or **absent**. This is the primary analytic output for defenders — the map of where controls are missing.

### Opportunity mode — accelerators

An **accelerator** is an action or condition that speeds up or increases the likelihood of the opportunity event occurring. Examples:

- Sharing intelligence with law enforcement partners (accelerates prosecution/seizure)
- Publishing adversary infrastructure indicators (accelerates community-wide blocking)
- Coordinating with allied governments (accelerates synchronized response)

---

## Step 7: Map recovery barriers or amplifiers (right side — between the central event and consequences)

For each consequence on the right side, identify the **recovery barriers** (threat mode) or **amplifiers** (opportunity mode) that sit between the central event and that consequence.

### Threat mode — recovery barriers

A **recovery barrier** is a control that, if functioning, stops the central event from leading to its worst-case consequence. These are the **reactive** controls — they do not prevent the event, but they limit its impact.

| Consequence | Recovery barrier |
|-------------|-----------------|
| Loss of OT visibility | Offline backup of historian data, manual operation procedures, OT-specific incident response playbook |
| Data exfiltration | Data loss prevention controls, network egress monitoring, encryption of sensitive data at rest |
| Ransomware encryption | Offline backups tested and validated, system restore capability, crypto-resilient backup architecture |
| Regulatory disclosure requirement | Pre-drafted breach notification templates, legal counsel on retainer, regulatory liaison relationship established |

**Critical**: As with preventive barriers, assess each recovery barrier as **present**, **partially present**, or **absent**.

### Opportunity mode — amplifiers

An **amplifier** increases the magnitude or duration of the beneficial consequence. Examples:
- Publishing a detailed technical report on the disrupted actor's TTPs (amplifies the community-wide defensive benefit)
- Using disruption window to expand collection and attribution (amplifies intelligence gain)
- Briefing partner nations before public disclosure (amplifies diplomatic benefit)

---

## Step 8: Map escalation factors

An **escalation factor (EF)** is anything that causes a barrier or accelerator to fail — or enhances the positive effect of an amplifier.

This is the step most commonly skipped in informal threat modeling, and it is where Bowtie Analysis generates its highest-value findings. A barrier that looks solid on paper may be routinely defeated by a known escalation factor.

### Escalation factor — threat mode

For each barrier identified in Steps 6 and 7, ask: *"Under what conditions does this barrier fail?"*

| Barrier | Escalation factor |
|---------|------------------|
| Phishing-resistant MFA | Real-time phishing proxy (EvilProxy-type attack) bypasses push-based MFA; OTP-based MFA susceptible to SIM swap |
| Patch management | Legacy OT systems cannot accept patches without vendor recertification; patch window is monthly, leaving 30-day exposure |
| Network segmentation | IT/OT convergence project created temporary firewall bypass that was never closed |
| Offline backups | Backup system uses a shared credential with the production environment — ransomware operator already has access |
| Incident response playbook | Playbook requires key personnel who are unavailable; last test was 18 months ago |

**Escalation factor barriers (EF barriers)**: For each escalation factor, identify whether a second-order control exists that prevents the EF from defeating the primary barrier. Example: the escalation factor "OTP-based MFA susceptible to SIM swap" has an EF barrier of "phishing-resistant FIDO2 hardware keys mandated for all privileged accounts."

### Escalation factor — opportunity mode

For accelerators and amplifiers, escalation factors enhance rather than defeat:
- An accelerator of "share intelligence with law enforcement" has an escalation factor of "pre-established secure channel and cleared liaison officer" — which makes the share faster and more complete.

---

## Step 9: Assess the full bowtie — control gap analysis

After all elements are mapped, conduct a systematic gap assessment:

### Control gap inventory

For each barrier (preventive or recovery):

| Barrier | Present? | Quality | Escalation factor identified? | EF Barrier present? | Gap? |
|---------|----------|---------|-------------------------------|---------------------|------|
| [barrier name] | Yes / Partial / No | Strong / Moderate / Weak | Yes / No | Yes / No / N/A | Yes / No |

### Priority gap findings

Gaps are prioritized by:

1. **Left-side preventive gaps**: A cause with NO preventive barrier means the event occurs whenever that cause is present. Highest priority for remediation.
2. **Right-side recovery gaps with high-severity consequences**: A consequence with no recovery barrier means maximum harm when the event occurs.
3. **Unmitigated escalation factors on critical barriers**: A nominally "present" barrier with an unmitigated escalation factor is effectively absent.

### Common gap patterns in CTI

- **The IT/OT seam**: Preventive controls exist for IT but not OT; the boundary itself is the gap.
- **Third-party inheritance**: Organization has strong controls for its own systems; vendor/partner access bypasses most of them.
- **Detection without response**: Monitoring is present (the cause is detected) but no automated or procedural response barrier exists — detection without action is not a barrier.
- **Untested barriers**: A backup system, playbook, or segmentation control exists on paper but has never been tested. These should be marked "partial" not "present."
- **Single-person dependencies**: A recovery barrier depends on a named individual who could be unavailable during an incident. Flag as escalation factor.

---

## Step 10: Produce the bowtie diagram

Render the complete bowtie as a structured visual representation. In chat, use a text diagram. In HTML, generate an interactive diagram. In .docx, use a structured table layout.

### Text bowtie structure (inline chat)

```
CAUSES (left)               BARRIERS               CENTRAL EVENT          BARRIERS               CONSEQUENCES (right)
──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

[Cause 1]                   [Preventive Barrier 1]
    └──────── EF: [EF 1a] ──────────────────────┐
                                                 │
[Cause 2]                   [Preventive Barrier 2]──────► [CENTRAL EVENT] ──────[Recovery Barrier A]──────► [Consequence A]
    └──────── EF: [EF 2a]  ──────────────────────┤             │
              EF Barrier: [EFB 2a]               │         [Recovery Barrier B]──────► [Consequence B]
                                                 │             └── EF: [EF B1]
[Cause 3]                   [NO BARRIER ⚠️]──────┘             EF Barrier: [none ⚠️]
```

Adapt to actual content. Flag missing barriers clearly with ⚠️. Flag unmitigated escalation factors with ⚠️.

### HTML output — visual bowtie diagram

When HTML output is requested, generate a self-contained HTML file with:

- A **visual bowtie SVG or CSS-based diagram** with causes on the left, consequences on the right, the central event as a prominent node in the center, and barriers annotated on the connecting lines
- **Color coding**: green = barrier present and tested; amber = barrier partial or untested; red = barrier absent
- **Escalation factors** shown as callout annotations on the relevant barrier lines
- A **control gap summary table** below the diagram listing all red and amber barriers with priority ranking
- An **analyst notes** section with key findings and recommendations

Build the HTML using vanilla HTML, CSS, and JavaScript only — no external dependencies except fonts from Google Fonts if desired.

---

## Step 11: Structure the written output

### Required output structure

**Header**: Focal event | Date | Analyst (if provided) | Mode (Threat / Opportunity)

**Executive Summary** (2–3 sentences)
The central event, the most critical control gap identified, and the single highest-priority action recommendation.

**Section 1 — Central Event**
The focal event defined precisely, with the threshold for occurrence and whether it is historical or prospective.

**Section 2 — Cause Analysis (Left Side)**
All identified causes, organized by category. Flag which causes have no preventive barrier.

**Section 3 — Preventive Barriers / Accelerators**
For each cause: the barrier or accelerator, its current status (present / partial / absent), and any identified escalation factors with their EF barriers.

**Section 4 — Consequence Analysis (Right Side)**
All identified consequences, organized by layer (operational → data → financial → strategic → reputational → regulatory → geopolitical). Flag which consequences have no recovery barrier.

**Section 5 — Recovery Barriers / Amplifiers**
For each consequence: the barrier or amplifier, its current status, and any identified escalation factors.

**Section 6 — Control Gap Inventory**
Full table of all barriers with present/partial/absent status, quality assessment, and escalation factor coverage. Sorted by priority.

**Section 7 — Key Findings**
The 3–5 most significant analytic findings: critical gaps, unmitigated escalation factors, systemic patterns, and high-leverage remediation opportunities.

**Section 8 — Recommendations**
Prioritized action list. For threat mode: what to fix first and why. For opportunity mode: what to do to accelerate or amplify the favorable outcome.

**Section 9 — Analytic Confidence and Limitations**
Confidence level (HIGH / MEDIUM / LOW) in the completeness of the bowtie. Key gaps in knowledge (unknown barriers, unverified escalation factors). Flag where assumptions are doing analytic work.

---

## Analyst principles

**The bowtie is only as good as its specificity.** Vague causes produce vague barriers. "Phishing" as a cause produces "email security" as a barrier — neither is actionable. "Credential-harvesting spearphish targeting finance personnel impersonating wire transfer approvals" produces "phishing-resistant MFA with FIDO2 hardware tokens required for all finance staff access to payment systems" — that is actionable. Push for specificity at every step.

**Absence of a barrier is the most important finding.** A cause with no preventive barrier means the event is directly reachable whenever that cause is present. A consequence with no recovery barrier means maximum harm is guaranteed when the event occurs. These are not administrative findings — they are critical vulnerabilities. Lead with them.

**Untested barriers are not barriers.** A backup system that has never been restored from, a segmentation control that has never been penetration tested, an incident response playbook that has not been exercised in 18 months — these are amber at best. Mark them partial and flag them for testing priority.

**Escalation factors are where the insight lives.** Most organizations have a list of controls. The bowtie's unique contribution is tracing *why controls fail*. Every experienced security incident has a pattern: the control was present but the escalation factor defeated it. Identifying those escalation factors before the incident is the entire point of the exercise.

**Don't let the diagram create false confidence.** The book explicitly warns: a detailed Bowtie Analysis can create the impression that all options and outcomes have been considered — they have not. Unanticipated causes exist. Novel escalation factors emerge. Unknown-unknowns remain outside the diagram by definition. Flag this in the analytic confidence section. Use Premortem Analysis to stress-test the completed bowtie.

**Dual-mode thinking is not optional.** Even in threat analysis, consider whether the same event presents any opportunity elements. A major ransomware incident may simultaneously be an opportunity to push for executive approval on long-stalled security investments, to invite law enforcement into a relationship, or to capture unique threat intelligence about the adversary's TTPs. Map both.

---

## Cognitive biases countered

| Bias | How Bowtie Analysis counters it |
|------|-------------------------------|
| **Mental Shotgun** | Forces systematic enumeration of all causes and consequences rather than fixating on the first that comes to mind |
| **Availability Heuristic** | Structured enumeration across cause categories surfaces less salient but equally real attack vectors |
| **Satisficing** | Requires complete barrier coverage for every cause and consequence — not just the most obvious ones |
| **Lacking Sufficient Bins** | Consequence taxonomy (operational → data → financial → strategic → regulatory → geopolitical) prevents consequence types from being overlooked |
| **Overrating Behavioral Factors** | Structural causes (misconfigured systems, absent controls) are explicitly mapped alongside human factors |
| **Assuming a Single Solution** | Multiple barriers per cause and per consequence are required — single-point dependencies are explicitly flagged |

---

## Potential pitfalls

**Completeness illusion**: The most dangerous artifact of a detailed bowtie. A finished diagram with 20 causes, 30 barriers, and 15 consequences can create the impression that the analyst has thought of everything. Explicitly caveat that the bowtie captures *known* causes, consequences, and barriers. Unknown attack vectors, unanticipated consequences, and novel escalation factors remain outside it. Schedule a review cadence.

**Over-abstraction**: Causes and consequences stated at too high a level produce barriers that are equally abstract and therefore useless for decision makers. Enforce the specificity rule at every step.

**Conflating detection with prevention**: Monitoring and alerting are not preventive barriers unless they are connected to an automated or procedural response that stops the cause from reaching the event. Log-only detection without a response playbook is not a barrier.

**Static product problem**: A bowtie is accurate at the time it is built. Environments change, threats evolve, controls are added and removed. An unreviewed six-month-old bowtie may be dangerously misleading. Recommend a review cadence in the output.

**Missing the right side**: Analysts and defenders systematically under-invest time on consequence mapping and recovery barriers. The bias is toward prevention. Force equal rigor on the right side — recovery barriers often have the most glaring gaps.

---

## Relationship to other techniques

**Red Hat Analysis (§8.1.3, T25)** — A natural predecessor. Red Hat Analysis determines *how an adversary would approach the target* — their likely attack approach, decision calculus, and preferred TTPs. Feed the Red Hat output directly into the left side of the bowtie as the cause set. A bowtie built from Red Hat analysis is significantly more adversarially realistic than one built from generic threat library enumeration.

**High Impact/Low Probability Analysis (§8.2.5, T30)** — Hi-Lo produces a focal scenario that warrants deep examination. Bowtie Analysis is the ideal next step: map how the Hi-Lo focal scenario could be reached (left side), what would happen if it were (right side), and where controls are insufficient. The Hi-Lo indicator set also maps cleanly to bowtie escalation factors.

**Impact Matrix (§10.3, T47)** — The natural follow-on to Bowtie Analysis. Once the right-side consequences are mapped, the Impact Matrix evaluates how each consequence affects each key stakeholder or organizational unit — adding a stakeholder dimension to the consequence analysis. The two techniques are designed to be used sequentially.

**Indicators Generation, Validation, and Evaluation (§9.11, T44)** — The escalation factors identified in the bowtie are prime candidates for monitoring indicators. An escalation factor that is beginning to manifest is an early warning that a previously robust barrier is about to be defeated. Feed escalation factors into an IGVE session to generate the monitoring regime.

**Premortem Analysis (§8.2.2, T31)** — Use Premortem to stress-test the completed bowtie. The Premortem question: "Assume the central event occurred despite our bowtie — how did that happen?" This will surface assumed barriers that did not actually hold, escalation factors that were not considered, and causes that were omitted.

**Analysis of Competing Hypotheses (§7.6, T19)** — When the cause of a past event is disputed (e.g., whether an incident was opportunistic or targeted, whether it was one threat actor or multiple), run ACH to determine the most likely explanation before building the bowtie. Building a bowtie on an incorrect causal hypothesis produces incorrect barrier recommendations.

**Alternative Futures Analysis (§9.6, T39)** — AFA can produce multiple scenarios for how a threat landscape evolves. Each scenario may produce a different central event. Build a separate bowtie for each high-priority AFA scenario to understand how defensive requirements vary across futures.

**Circleboarding™ (§6.4, T9)** — Use Circleboarding at the start of an engagement when the full picture of an event is unclear. Circleboarding's Who/What/How/When/Where/Why structure produces the raw material — threat actors, targets, methods, timing — that populates the bowtie's left side more completely than ad hoc brainstorming.

**Decision Trees (§10.6, T50)** — Decision Trees and Bowtie Analysis both analyze chains of events. Decision Trees map forward-branching decision paths. Bowtie Analysis is focused specifically on a single event with bidirectional cause-consequence mapping and explicit barrier/control identification. They are complementary: use Bowtie for risk/control analysis; use Decision Trees for branching decision-option analysis.
