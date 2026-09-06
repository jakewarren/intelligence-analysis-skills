---
name: circleboarding
description: |
  Performs Circleboarding™ — Exploration SAT (Pherson & Heuer §6.4, T9). Answers Who, What, How, When, Where, Why, and So What? to build a comprehensive picture of any topic. Answers questions (vs. Starbursting, which generates them). Ideal at project start, for incident triage, threat actor profiling, or indicator generation.

  Trigger on: "circleboarding", "run a circleboard", "5 W's and H", "who what how when where why", "map out what we know", "get a handle on this incident", "what do we know about this", "triage this incident", "what happened", "piece together what happened", "kickoff analysis". Also trigger when a user pastes raw reporting or an incident brief and wants a structured breakdown before running ACH, KAC, or indicator generation.

  Supports three modes: incident/event, threat actor, and indicator generation. Input: typed topic, incident description, pasted reporting, or uploaded doc. Output: inline chat, HTML with visual circle diagram, or Word .docx.
---

# Circleboarding™

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §6.4, T9*

## Purpose

Circleboarding™ builds a comprehensive initial picture of a topic by systematically working through the six questions any good journalist asks — **Who, What, How, When, Where, and Why** — and then demanding a **So What?** The "So What?" is the insight that connects the event to the client: what does this mean for our organization, our network, or our mission?

The technique's power lies in its structure. It prevents analysts from jumping straight to conclusions by forcing explicit passes through all six dimensions before any impact assessment is attempted. It surfaces knowledge gaps — dimensions where the answers are thin or absent — which are often as analytically significant as what is known. And it mitigates three of the most common analytic traps: **Mental Shotgun** (defaulting to the first plausible answer), **Satisficing** (stopping when the answer feels "good enough"), and **Associative Memory** (over-weighting vivid or recent information at the expense of systematic coverage).

In CTI, this is the right first move when a new campaign, intrusion, or threat actor surfaces and the team needs to stop asking "what should we do?" long enough to agree on "what do we actually know?"

---

## Step 1: Ingest the input

Accept any of these:

- **Typed topic or question** — e.g., "Circleboard the APT41 Citrix campaign from last quarter"
- **Pasted reporting or notes** — Extract the core subject and mine the text for answers to each question
- **Uploaded document** — Read it, identify the subject, and build the board from its contents

The "topic" must be concrete and bounded. If the user gives something too broad (e.g., "ransomware threats"), ask for a specific incident, actor, or campaign before proceeding. A vague topic produces a vague board.

---

## Step 2: Confirm scope — then proceed

Infer the following; only ask if genuinely ambiguous:

- **Output format**: HTML (with visual circle diagram) if no preference is stated, or if the user wants something shareable. Inline chat if they ask for "quick" or "fast." .docx if they mention a report or briefing.
- **Mode**: Incident/event mode (analyzing something that happened) vs. threat actor mode (profiling an adversary) vs. indicator mode (generating observable indicators for a scenario). The mode affects the prompts under each dimension. Infer from context; default to incident/event mode for CTI.
- **Depth**: Standard (2–4 answers per dimension, key gaps flagged) or deep dive (exhaustive answers, all sub-questions probed, explicit uncertainty ratings). Default to standard.

State your assumed scope in one line at the top of the output: *"Circleboarding [topic] — incident/event mode, standard depth, HTML output."* This lets the user correct without blocking the work.

---

## Step 3: Define the subject

State the topic as a clear, bounded declarative phrase — not a conclusion, but a subject:

> *"Subject: The intrusion campaign targeting Japanese defense contractors attributed to Bronze Starlight (DEV-0401), Q4 2024."*

Write it in the center of the board alongside "So What?" — it's what the entire analysis orbits.

---

## Step 4: Work around the circle

Go through each dimension systematically. For each one: answer what is known, flag what is unknown, and note any analytic confidence level if the user has provided enough to rate it.

The order matters: the book sequences them to follow the logic of a declarative sentence — **who** did **what**, **how**, **when**, **where**, and **why**. Work through them in this order.

---

### WHO

The actors, victims, and third parties involved.

**In CTI — incident/event mode, probe:**
- Who is the threat actor (attributable or suspected)?
- What is the targeting profile — who are the victims? Is this consistent with the actor's known collection priorities?
- Who else is involved: intermediaries, access brokers, infrastructure providers, nation-state sponsors?
- Are there insider elements?

**In threat actor mode, probe:**
- Who runs the group? What is the command structure?
- Who are their known or suspected targets? What sectors, geographies, or personas?
- Who are their sponsors or clients?

**In indicator mode, probe:**
- Who could potentially emit this indicator? What actor types?
- Who is the intended target of this indicator campaign?

Flag: who do we *not* know about? Unknown actors are often as significant as known ones.

---

### WHAT

The actions taken, systems compromised, data affected, or capabilities used.

**In CTI — incident/event mode, probe:**
- What malware, tools, or TTPs were used? Known families or novel?
- What systems, data, or infrastructure were targeted or compromised?
- What was the objective — espionage, disruption, financial theft, pre-positioning?
- What was the impact: data exfiltrated, systems destroyed, operations disrupted?

**In threat actor mode, probe:**
- What is the actor's primary collection interest or operational objective?
- What capability set do they demonstrate? Novel vs. commodity tooling?
- What makes this actor distinctive?

**In indicator mode, probe:**
- What indicator would the actor emit? Network, endpoint, behavioral?
- What does the artifact look like at technical level?

Flag: what is unconfirmed, suspected, or deliberately obscured?

---

### HOW

The methods, techniques, and tradecraft — the *how* the operation was executed.

**In CTI — incident/event mode, probe:**
- How was initial access obtained? (Phishing, exploit, supply chain, insider, etc.)
- How was persistence established?
- How did the actor move laterally?
- How did they maintain operational security — proxy chains, TOR, living-off-the-land?
- How was the objective achieved — data staged, exfil method, destructive payload delivery?

**In threat actor mode, probe:**
- What is the actor's standard kill chain? Where does it differ from the norm?
- How do they typically acquire and manage infrastructure?
- How do they handle attribution risk (OPSEC tradecraft)?

**In indicator mode, probe:**
- How would this indicator manifest in logs, telemetry, or traffic?
- How might we miss it — what detection gaps exist?
- How reliable is this indicator as a signal (false positive rate)?

Flag: which steps of the attack chain are undocumented or uncertain? These are collection gaps.

---

### WHEN

The timing — both absolute (dates, durations) and relative (sequencing, opportunity windows).

**In CTI — incident/event mode, probe:**
- When did the intrusion begin? When was it discovered? What is the dwell time?
- When was each stage of the attack executed — initial access, lateral movement, objective achievement?
- Is the timing correlated with geopolitical events, vulnerability disclosures, or organizational milestones (e.g., mergers, elections, contract awards)?
- When were indicators first seen in other environments?

**In threat actor mode, probe:**
- What is the actor's operational tempo? Continuous vs. episodic?
- Do they operate on a particular shift, timezone, or national calendar?

**In indicator mode, probe:**
- When would we be most likely to see this indicator?
- Is the indicator time-limited (e.g., appears only during a specific phase)?

Flag: is there a gap between when the activity began and when it was detected? Every hour of undetected dwell time is a data point.

---

### WHERE

The geography, network topology, and organizational location.

**In CTI — incident/event mode, probe:**
- Where in the network did the intrusion begin? Where did it propagate?
- Where is the C2 infrastructure located? What jurisdictions?
- Where are the victims — sectors, geographies, specific organizations?
- Where is the data now? Exfiltrated to what infrastructure, country, or actor?

**In threat actor mode, probe:**
- Where does the actor operate from? Suspected location and infrastructure base?
- Where have they struck before? Geographic and sector patterns?

**In indicator mode, probe:**
- Where in the environment would this indicator appear — network perimeter, endpoint, cloud?
- Where is collection coverage weakest?

Flag: infrastructure located in jurisdictions where law enforcement cooperation is unavailable. These limit response options.

---

### WHY

The intent, motivation, and strategic rationale.

This is the hardest dimension — and often the most analytically important. **Who** and **What** can often be established from technical evidence. **Why** requires inference about adversary intent, which is always uncertain.

**In CTI — incident/event mode, probe:**
- Why this target? What does the victim have that the actor wants?
- Why now? Is this opportunistic, or is the timing significant?
- Why this method? Does the chosen tradecraft reveal anything about operational constraints, risk tolerance, or objectives?
- Is the motive espionage, financial, disruptive, or coercive?

**In threat actor mode, probe:**
- What are the actor's strategic objectives? National collection priority alignment?
- Is the actor state-directed, state-sponsored, or independent?
- What would constitute mission success for this actor?

**In indicator mode, probe:**
- Why is this indicator important? What hypotheses does it discriminate between?
- Why might we misinterpret this indicator?

Flag: **unstated assumptions about motive are the most common source of analytic error in attribution.** Make every motive assumption explicit here.

---

## Step 5: Reflect and prioritize

After completing all six dimensions, step back and ask: **which dimension contains the most analytically significant information? Which dimension has the most critical gaps?**

Rank the six dimensions by two criteria:
- **Significance to the analysis** (1 = most important)
- **Confidence level** (HIGH / MEDIUM / LOW / UNKNOWN)

This forces explicit prioritization and helps the client understand where to focus collection or additional analysis. The dimensions with LOW or UNKNOWN confidence and HIGH significance are your collection requirements.

---

## Step 6: So What?

This is the payoff — the synthesis that connects the six dimensions to the client's concerns.

Answer three questions:

1. **Impact assessment**: What is the significance of this event or threat? What damage has been done or could be done?
2. **Implications**: What does this tell us about the adversary's capabilities, intent, or future behavior? What does it reveal about our own vulnerabilities?
3. **Recommended action**: What should the client do? This can be: collect more on a specific gap, implement a specific defensive measure, escalate to a follow-on SAT, or issue a warning.

The So What? should be 3–5 sentences. If you cannot write a clear So What? based on the six dimensions, that tells you something important: you do not yet have enough to assess impact. Say so explicitly.

---

## Step 7: Gap inventory

Surface every dimension where the answer was absent, thin, or uncertain. Format as a simple list:

```
KNOWLEDGE GAPS
- WHO:  Attribution remains unconfirmed; actor assessed with MEDIUM confidence based on TTP overlap only
- HOW:  Initial access vector unknown; no visibility into pre-compromise phase
- WHEN: Earliest date of compromise unknown; discovery date ≠ start date
- WHY:  Motive inferred from targeting pattern; no confirmed collection requirement linked to actor
```

Gaps that are both HIGH significance and LOW confidence should automatically generate collection requirements. Note these explicitly.

---

## Step 8: Produce the output

### For inline chat (Markdown):

Use this structure:

```
## Circleboarding™: [Subject]
**Mode**: [incident/event | threat actor | indicator] | **Depth**: [standard | deep dive]

### WHO
[Answers + gaps]

### WHAT
[Answers + gaps]

### HOW
[Answers + gaps]

### WHEN
[Answers + gaps]

### WHERE
[Answers + gaps]

### WHY
[Answers + gaps]

---
### Dimension Prioritization
[Ranked table: dimension | significance rank | confidence]

---
### SO WHAT?
[3–5 sentences: impact, implications, action]

---
### Gap Inventory
[List of significant gaps with collection requirements]
```

---

### For HTML (default — with visual circle diagram):

Produce a standalone HTML file that renders a visual representation of the circleboard. The circle should show all six dimensions positioned around the perimeter (clockwise: WHO → WHAT → HOW → WHEN → WHERE → WHY) with "SO WHAT?" in the center. Each dimension should be clickable or expandable to show its answers.

Use this structure as a template. Keep all CSS and JavaScript inline in the single file.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Circleboard: [SUBJECT]</title>
  <style>
    /* Circle diagram: use SVG for the ring layout */
    /* Dimension cards: positioned around the circle */
    /* Color scheme: gaps in amber, confirmed in green, unknown in red */
    /* So What box: centered, prominent */
  </style>
</head>
<body>
  <!-- Header: subject, date, mode -->
  <!-- SVG circle diagram with 6 labeled nodes and center -->
  <!-- Expandable dimension panels below the diagram -->
  <!-- So What box -->
  <!-- Gap inventory table -->
</body>
</html>
```

For the SVG circle: place the six dimensions at clock positions 12, 2, 4, 6, 8, 10 o'clock. The center shows "SO WHAT?" with the subject text. Lines connect each dimension to the center. Color-code each dimension node by confidence: 🟢 HIGH, 🟡 MEDIUM, 🔴 LOW/UNKNOWN. Label each gap.

The HTML must be fully self-contained and render correctly when opened in a browser.

---

### For .docx:

Use the `docx` skill. Structure:
- Title: *Circleboard: [Subject]*
- Subtitle: Date, Analyst, Mode
- Section for each dimension (styled heading, answers, gaps)
- Dimension Prioritization table
- So What? section
- Gap Inventory table with collection requirements

---

## Relationship to other techniques

**Before this technique:**
Circleboarding is often the first structured technique run on a new topic. It needs only a subject and whatever raw reporting is available.

**After this technique:**
- **Key Assumptions Check (KAC)** — The Why dimension almost always produces implicit assumptions about actor intent. Feed them directly into a KAC to test their soundness.
- **Analysis of Competing Hypotheses (ACH)** — Once you have the full picture from Circleboarding, ACH lets you evaluate which hypothesis (especially about Who and Why) best fits the collected evidence.
- **Indicators Generation, Validation, and Evaluation (IGVE)** — Circleboarding in indicator mode produces a first-draft indicator set. Run IGVE to validate and score them.
- **Multiple Hypothesis Generation (MHG)** — If the Who or Why dimension surfaces multiple competing explanations, feed them into MHG to build a hypothesis set before running ACH.
- **Key Drivers Generation (KDG)** — If the So What? points toward a need for foresight analysis (how will this situation develop?), extract the Why and How dimensions as candidate drivers for KDG.

---

## Analyst principles

**Treat absence as a data point.** A dimension with no good answers is not a failed analysis — it is an explicit finding. "We do not know How the actor obtained initial access" is analytically more useful than a vague placeholder.

**Separate what is observed from what is inferred.** In the WHO and WHY dimensions especially, the temptation is to state inferences as facts. Prefix inferences: *"Assessed as..."*, *"Consistent with..."*, *"Possibly..."*.

**The So What? must be earned.** Do not write the impact assessment before completing all six dimensions. The point of the technique is to prevent premature synthesis. If you find yourself tempted to write the So What? at the top, resist — the six dimensions will often change it.

**Circleboarding is a team synchronization tool, not just an analytic one.** In a group setting, the exercise surfaces divergent mental models among team members. Two analysts who answer "Why" differently have different analytic priors — the board makes that visible and productive rather than invisible and corrosive.

---

## CTI example

**Subject:** Mass exploitation of Ivanti Connect Secure (CVE-2025-0282) by suspected PRC-nexus actor, January 2025

| Dimension | Key Answers | Confidence | Key Gaps |
|-----------|-------------|------------|----------|
| **WHO** | Suspected UNC5337/UNC5221 (PRC-nexus); victims span critical infrastructure, defense industrial base, government | MEDIUM | No confirmed IC attribution; multiple actors exploiting same CVE |
| **WHAT** | Zero-day exploitation of CVE-2025-0282; SPAWN malware ecosystem deployed; credential harvesting and VPN access maintained | HIGH | Full scope of victim set unknown; not all deployed payloads recovered |
| **HOW** | Pre-auth stack overflow → RCE → SPAWNANT installer → SPAWNMOLE tunnel → SPAWNSNAIL SSH backdoor; ICT tampered to survive factory resets | HIGH | Pre-compromise reconnaissance method unknown |
| **WHEN** | Active exploitation Dec 2024; Ivanti disclosed Jan 8 2025; CISA KEV added Jan 13 2025; dwell time in some environments exceeded 30 days | HIGH | First date of actor acquisition of exploit unknown |
| **WHERE** | Victims globally; concentration in U.S., Europe, Japan; C2 infrastructure via compromised SOHO routers and VPS (obfuscated) | MEDIUM | Geographic distribution of all victims not fully mapped |
| **WHY** | Assessed as cyber-espionage (intelligence collection) targeting government and defense sector; VPN access provides persistent entry for follow-on tasking | MEDIUM | No confirmed collection requirement publicly linked; may also be pre-positioning |

**So What?** This campaign represents a systematic effort to exploit trusted remote access infrastructure at scale, likely in support of PRC national collection priorities. The SPAWN malware's resilience against factory resets signals significant investment in persistence, suggesting the actor intends long-term access rather than rapid data theft. Organizations relying on Ivanti Connect Secure for privileged remote access should treat compromise as presumed until validated otherwise, apply Ivanti's mitigation guidance and the CISA detection tooling, and review VPN access logs for indicators from the SPAWN family. This incident also demonstrates a broader pattern of PRC-nexus actors targeting network edge devices — the gap in initial access telemetry for most victims is a systemic collection weakness that warrants investment in pre-compromise visibility.
