---
name: outside-in-thinking
description: |
  Performs Outside-In Thinking / STEMPLES+ Environmental Scan — Cause and Effect SAT (Pherson & Heuer §8.1.1, T23). Surveys external forces (Social, Technological, Economic, Military, Political, Legal, Environmental, Security, +) affecting an issue. Works outside-in to surface forces specialty analysis misses. Run before hypotheses, before KDG, before any foresight exercise.

  Trigger on: "outside-in thinking", "STEMPLES", "STEMPLES+", "environmental scan", "what external forces", "PEST analysis", "PESTLE", "PMESII", "scan the environment", "external factors", "broaden my analysis", "geopolitical context", "what am I missing from the bigger picture". Also trigger when scoping a new project for comprehensive coverage, before KDG/AFA, or in CTI when geopolitical/economic/legal forces explain threat actor behavior beyond TTPs.

  Input: typed topic, pasted reporting, or uploaded doc. Output: inline chat, HTML with STEMPLES+ wheel, or .docx.
---

# Outside-In Thinking / STEMPLES+

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §8.1.1 — Cause and Effect Technique T23*

## Purpose

Outside-In Thinking identifies the broad range of forces and trends in the external environment — forces over which analysts and decision-makers have little or no control — that could nonetheless profoundly affect the issue under study. The defining move is a *reversal of direction*: most analysts work from the data at hand outward (inside-out), staying within their specialty domain. Outside-In Thinking inverts this by first asking what the broader environment is doing, then asking how those dynamics bear on the specific problem.

The mnemonic **STEMPLES+** provides the framework: **S**ocial, **T**echnological, **E**conomic, **M**ilitary, **P**olitical, **L**egal, **E**nvironmental, and **S**ecurity — plus additional factors such as Demographic, Psychological, Religious, or Informational as the topic demands. Related business-intelligence frameworks you may recognize include PEST, PESTLE, STEEPLED, and the military's PMESII — all are variants of the same underlying idea.

**Cognitive traps this technique counteracts:**

- **Tunnel Vision** — focusing exclusively on factors within one's specialty area while missing external forces that are driving behavior
- **Availability Heuristic** — overweighting vivid, recent, or familiar technical factors (e.g., malware TTPs) while underweighting slow-moving structural forces (e.g., economic sanctions, legal pressure, demographic change)
- **Anchoring Effect** — locking onto the current status quo and failing to consider that external forces may be shifting the baseline
- **Premature Closure** — forming a hypothesis before the full environmental picture has been surveyed
- **Narrow Framing** — treating a geopolitical, economic, or legal dynamic as "someone else's problem" rather than a factor that shapes the issue at hand

**Why this is distinct from Key Drivers Generation (KDG):**
Both techniques use STEMPLES+ as a brainstorming scaffold, but they serve different purposes. Outside-In Thinking is an *environmental scan* — its goal is comprehensive coverage, surfacing every plausible external force that touches the issue. KDG is a *selection and prioritization exercise* — it winnows that landscape down to the 4–6 forces most uncertain and consequential enough to serve as scenario axes. Outside-In Thinking typically precedes KDG and feeds it; running OIT first produces a richer and more defensible candidate pool.

---

## Step 1: Ingest the input

Accept any of these:

- **Typed topic or question in chat** — e.g., "What external forces could affect North Korean cryptocurrency theft operations over the next two years?" or "Run an Outside-In on the ransomware threat to US critical infrastructure"
- **Pasted reporting or analytic draft** — Extract the core issue and mine the text for any forces already mentioned; use the STEMPLES+ scan to check whether anything was missed
- **Uploaded document** — Read the file; identify the issue under study and any environmental factors already discussed

The focal issue must be concrete and bounded. If the user gives something too broad (e.g., "cybersecurity"), ask for a specific actor, campaign, sector, or policy question before proceeding. A vague issue produces a vague environmental scan.

---

## Step 2: Confirm scope (briefly)

Infer the following from context; ask only if genuinely ambiguous:

1. **Depth**: Standard (1–3 key forces per STEMPLES+ category, gaps flagged) or exhaustive (full brainstorm, all sub-questions probed, explicit uncertainty ratings). Default to standard.
2. **Downstream use**: Is this a standalone scan, or will it feed KDG, AFA, or another technique? If feeding KDG, flag which findings are likely candidates for driver promotion.
3. **Output format**: HTML with wheel visualization (default if no preference stated), inline Markdown, or Word .docx.

State your assumed scope in one line at the start of the output: *"Outside-In Thinking for: [issue] — standard depth, HTML output."* This lets the user correct without blocking the work.

---

## Step 3: Frame the issue

Write a single, bounded declarative statement of the issue. This is not a hypothesis — it is the subject around which the environmental scan will orbit.

> *"Issue: The use of cryptocurrency by DPRK-affiliated cyber actors to fund the state's weapons programs, 2024–2026."*

> *"Issue: The resilience of ransomware ecosystems following law enforcement disruption operations, 2023–2025."*

This framing disciplines the scan. For each STEMPLES+ category, the question is not "what is happening in this domain generally?" but "what is happening in this domain that could affect **this specific issue**?"

---

## Step 4: Conduct the STEMPLES+ scan

Work through each category systematically. For each one:

1. **Generate** external forces and factors in this domain that could affect the issue — cast the net broadly, do not evaluate yet
2. **Assess relevance and impact**: Does this force actually bear on the issue? If it does, is the impact HIGH / MEDIUM / LOW? Note the direction (enables, constrains, amplifies, complicates)
3. **Flag expertise gaps**: Does the analysis team have sufficient knowledge of this domain to assess it confidently? If not, this is a collection gap
4. **Note the key uncertainty**: Within this category, what is the most important thing that is genuinely unknown?

---

### S — Social

Forces: demographic shifts, social cohesion and fragmentation, public trust in institutions, media ecosystem dynamics, social norms, cultural attitudes toward privacy/authority/risk, diaspora dynamics, insider threat psychology.

**CTI-specific prompts:**
- What social dynamics within the adversary's country or organization shape operator behavior, recruitment, or motivation (e.g., youth unemployment driving cybercrime recruitment, nationalism channeling hacktivist energy)?
- What societal trends in the victim population affect the attack surface (e.g., remote work normalization, social media dependency, declining institutional trust enabling phishing)?
- What social engineering vectors does this actor exploit, and what social conditions make those vectors more or less effective?
- Is there a whistleblower, defector, or insider threat dynamic at play?

---

### T — Technological

Forces: emerging and disruptive technologies, capability maturation curves, vulnerability disclosure and patch rates, platform adoption and deprecation cycles, AI/ML developments, supply chain technology dependencies, information environment changes.

**CTI-specific prompts:**
- What technological advances is the actor likely leveraging or racing to acquire (e.g., AI-assisted exploit development, LLM-powered phishing, quantum-resistant cryptography)?
- What technology shifts are changing the victim's attack surface (e.g., cloud migration, IoT proliferation, operational technology convergence)?
- What defensive technology trends might degrade the actor's current TTPs?
- Are there emerging platforms, protocols, or services that the actor could weaponize or abuse for C2, laundering, or recruitment?
- What vulnerability class trends (e.g., memory safety issues, supply chain injections) are the actor's TTPs aligned with, and are those trends accelerating or decelerating?

---

### E — Economic

Forces: macroeconomic conditions, trade and sanctions regimes, commodity and resource prices, financial system stability, income inequality, cybercrime economics and ROI, cryptocurrency market conditions, corporate financial pressures.

**CTI-specific prompts:**
- How do economic sanctions on the actor's sponsoring state constrain or motivate their cyber operations (e.g., DPRK using cryptocurrency theft to offset sanctions revenue loss)?
- What economic pressures on victim organizations increase their vulnerability (e.g., cost-cutting on security staff, rushed cloud migration to reduce overhead)?
- What is the current ransomware economy like — how have ransom payments, insurance payouts, and enforcement actions affected criminal economics?
- Are cybercrime affiliates financially motivated or ideologically motivated? Economic conditions shift this balance.
- What financial sector trends affect money laundering channels available to the actor?

---

### M — Military

Forces: military capability development, force posture changes, doctrine evolution, readiness and morale, alliance solidarities, military-civil integration, escalation dynamics, conflict intensity and geographic scope.

**CTI-specific prompts:**
- Is the actor's cyber operation subordinated to a military command structure, and if so, what does current military doctrine tell us about how that command would task cyber assets?
- How do ongoing conventional military operations (e.g., active conflict) affect the priority, tempo, and objectives of associated cyber operations?
- Is the actor using cyber operations as a substitute for, or complement to, kinetic military action? What does escalation dynamics between the parties suggest about this choice?
- What military capability gaps might the actor be trying to close through cyber espionage?
- Are there OT/ICS targets that would support military operational objectives?

---

### P — Political

Forces: government stability, leadership succession, regime type and decision-making style, electoral dynamics, inter-agency politics, geopolitical alignments and rivalries, sanctions politics, cyber diplomacy.

**CTI-specific prompts:**
- What political objectives is the sponsoring state pursuing, and how do those objectives translate into collection priorities that would shape cyber targeting?
- How do domestic political dynamics in the actor's country affect operational risk tolerance (e.g., a leadership under domestic pressure may be more aggressive, or may restrain operations that could trigger retaliation at a bad time)?
- What bilateral or multilateral political developments (summits, agreements, disputes, escalations) have preceded shifts in the actor's cyber operational tempo?
- How does the political environment in the victim country shape the actor's targeting calculus (election season, leadership transition, policy shift)?
- What international cyber norms negotiations or agreements could constrain the actor or create attribution risk they care about?

---

### L — Legal

Forces: treaty frameworks, domestic criminal law, international cooperation agreements, mutual legal assistance treaties (MLATs), sanctions architectures, cybercrime legislation, rule of law, enforcement capacity.

**CTI-specific prompts:**
- In which jurisdictions does the actor operate, and what is the practical likelihood of criminal prosecution? Actors in jurisdictions with no extradition treaties or weak rule of law face near-zero legal risk — this shapes how much operational security they invest in.
- How do recent law enforcement actions (indictments, sanctions designations, infrastructure seizures) affect the actor's behavior and risk calculus?
- What legal constraints operate on defenders and responders — can they hack back, share threat intelligence, or take network defense actions beyond their own perimeter?
- Do new or proposed regulations (NIS2, GDPR, SEC cyber disclosure rules) change the victim organization's posture or reporting behavior in ways the actor could exploit or that would accelerate threat intelligence sharing?
- What legal exposure does the actor's money laundering or financial operations face, independent of their hacking activity?

---

### E — Environmental

Forces: climate and extreme weather, resource scarcity (water, food, energy), natural disaster risk, physical infrastructure dependencies, geographic and ecological constraints, energy grid dynamics.

**CTI-specific prompts:**
- Is the actor's infrastructure or population vulnerable to climate-driven instability in ways that could affect operational continuity or motivate resource-seeking behavior (e.g., energy-starved states more aggressively targeting energy sector intelligence)?
- For OT/ICS or critical infrastructure analysis: what physical environmental factors (weather events, grid stress, water stress) create windows of increased vulnerability for the target?
- Are there physical-cyber nexus risks — cyber attacks timed to amplify the impact of environmental stressors on critical infrastructure?
- Does the actor's geographic location create physical constraints (power availability, internet routing chokepoints, climate effects on data center operations)?

---

### S — Security (second S in STEMPLES+)

Forces: law enforcement and intelligence service capability and activity, alliance information-sharing, threat intelligence ecosystem maturity, defensive posture of the target sector, private sector security industry dynamics, cyber insurance markets.

**CTI-specific prompts:**
- What is the current law enforcement operational tempo against this actor type — active disruption operations, indictment campaigns, infrastructure seizures? How has this changed the actor's behavior?
- How mature is the defensive posture of the target sector? Are organizations patching faster, adopting EDR, deploying MFA at scale? This directly degrades the actor's TTPs.
- What intelligence-sharing mechanisms exist in the target sector (ISACs, government programs), and how effectively are they operating? What does the actor know about these mechanisms?
- How is the threat intelligence industry's public reporting on this actor affecting their operational security choices?
- What cyber insurance trends affect victim willingness to pay ransoms, invest in controls, or share breach information?

---

### + — Additional Factors

For any topic, ask whether additional domains deserve explicit treatment:

| Factor | When to include |
|--------|----------------|
| **Demographic** | When age, education, or population dynamics are shaping actor or victim behavior (e.g., aging workforce with lower cyber awareness, young cybercriminal recruitment pool) |
| **Psychological** | When operator motivation, morale, organizational culture, or individual decision-making styles are analytically significant (e.g., patriotic hacker vs. mercenary, burned-out operator vs. ideologically committed one) |
| **Religious/Ideological** | When belief systems or ideological commitments drive targeting or constrain actor behavior (e.g., hacktivist groups motivated by specific causes, state actors constrained by ideological posture) |
| **Informational** | When information environment dynamics — propaganda, disinformation, narrative control — are a factor in the operation or shape the strategic context |
| **Supply Chain** | When the attack surface or actor capability depends on specific supply chain dynamics not captured elsewhere |

Add only the factors genuinely relevant to the issue at hand. More bins are not always better — if a factor has nothing to say about this particular issue, note it briefly and move on.

---

## Step 5: Synthesize the landscape

After completing all STEMPLES+ categories, step back and produce three synthesis outputs:

### 5a — Impact matrix

Create a summary table rating each category by two dimensions:

| Category | Relevance to Issue | Impact Direction | Confidence | Key Finding |
|----------|--------------------|-----------------|------------|-------------|
| Social   | HIGH / MED / LOW   | Enables / Constrains / Complicates / Amplifies | HIGH / MED / LOW | One-sentence summary |
| ... | | | | |

### 5b — Dominant forces

Identify the 3–5 external forces with the highest relevance AND highest confidence. These are the forces the analysis should not proceed without accounting for. State each as a declarative finding:

> *"Economic — DPRK's cryptocurrency theft operations are economically rational given the scale of sanctions-induced revenue gaps; the actor has strong incentive to sustain and expand operations regardless of diplomatic signals."*

> *"Legal — The actor's operators face near-zero prosecution risk given jurisdictional safe harbor; law enforcement pressure operates primarily through infrastructure disruption rather than individual deterrence."*

### 5c — Key uncertainties

Identify the 3–5 forces where relevance is high but confidence is LOW. These are the environmental gaps most likely to invalidate current analysis if they resolve unexpectedly:

> *"Political — It is unclear whether recent high-level bilateral engagement is constraining the actor's cyber operations as a diplomatic signal, or whether operations are continuing unaffected. This matters because the current analytic baseline assumes continued high operational tempo."*

---

## Step 6: Generate collection priorities

For each significant expertise gap identified in the scan, generate a specific collection or research priority. Frame each as a question the analysis needs to answer before proceeding:

```
COLLECTION / RESEARCH PRIORITIES
Priority 1 [Category: Legal] — What enforcement actions are currently underway or planned against
            this actor, and has any recent legal activity caused operational pauses?
Priority 2 [Category: Economic] — What is the current state of the actor's cryptocurrency laundering
            channels following the Tornado Cash sanctions and Lazarus indictments?
Priority 3 [Category: Political] — Has the actor's tasking shifted following the most recent
            leadership transition, and is there evidence of altered collection priorities?
```

---

## Step 7: Produce the output

Always close every output — whether inline, HTML, or .docx — with a **Downstream Recommendations** section that names each suggested follow-on technique by its full SAT name: "Key Drivers Generation (KDG)", "Alternative Futures Analysis (AFA)", "Red Hat Analysis", "Key Assumptions Check (KAC)", etc. Do not substitute generic phrases like "scenario planning", "further analysis", or "scenario development" — the exact SAT name is what allows the user to invoke the next technique. Use the lookup table in the "Downstream recommendations" section to select the right techniques based on what the scan found.

### Inline chat (Markdown)

```
## Outside-In Thinking™: [Issue]
**Depth**: Standard | **Output**: Inline | **Date**: [date]

### Environmental Scan

#### S — Social
[Key forces, relevance, confidence, gaps]

#### T — Technological
[Key forces, relevance, confidence, gaps]

[...repeat for all categories...]

---
### Impact Matrix
[Summary table]

### Dominant Forces
[3–5 declarative findings]

### Key Uncertainties
[3–5 high-relevance, low-confidence gaps]

---
### Collection / Research Priorities
[Prioritized list]

---
### Downstream Recommendations
[Select from the table in the "Downstream recommendations" section below. Reference each technique by its proper SAT name — e.g., "Key Drivers Generation (KDG)", "Alternative Futures Analysis (AFA)", "Red Hat Analysis" — not generic phrases like "scenario development" or "further analysis".]
```

---

### HTML (default — with STEMPLES+ wheel visualization)

Produce a standalone HTML file. The visualization should render a circular diagram with the 9 STEMPLES+ segments arranged around a central issue label. Each segment is colored by impact level (HIGH = deep amber, MED = medium blue, LOW = light gray, UNKNOWN = white/hatched). Clicking a segment expands a detail panel below. The dominant forces and collection priorities appear as structured panels outside the wheel.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Outside-In Thinking: [ISSUE]</title>
  <style>
    /* STEMPLES+ wheel: SVG with 9 segments, color-coded by impact */
    /* Issue label centered in the wheel */
    /* Click-to-expand detail panels for each category */
    /* Dominant forces section: bordered, prominent */
    /* Collection priorities: numbered list, flagged */
    /* Clean intelligence-report aesthetic: white background, dark text */
  </style>
</head>
<body>
  <!-- Header: issue, date, depth -->
  <!-- SVG wheel: 9 segments (STEMPLES + one + segment) -->
  <!-- Detail panels (initially collapsed, expand on click) -->
  <!-- Impact matrix table -->
  <!-- Dominant forces panel -->
  <!-- Key uncertainties panel -->
  <!-- Collection priorities panel -->
  <!-- Downstream recommendations: proper SAT names (KDG, AFA, Red Hat, KAC, etc.) -->
</body>
</html>
```

The HTML must be fully self-contained (no external dependencies) and render correctly when opened in a browser.

---

### Word (.docx)

Use the `docx` skill. Structure:
- Title: *Outside-In Thinking: [Issue]*
- Subtitle: Date, Analyst, Depth
- One section per STEMPLES+ category (heading, forces, relevance rating, gaps)
- Impact Matrix table
- Dominant Forces section
- Key Uncertainties section
- Collection Priorities table
- Downstream Recommendations

---

## Downstream recommendations

After completing the scan, tell the user which techniques are natural next steps:

| Finding type | Recommended next technique |
|---|---|
| Need to rank and prioritize the forces identified | **Key Drivers Generation** (T34) — takes the OIT candidate pool and winnows to 4–6 scenario-ready drivers |
| Multiple competing explanations for *why* external forces are behaving as they are | **Analysis of Competing Hypotheses** (T19) — formalize the competing explanations and test against evidence |
| One or more external forces represents a potential surprise or tail risk | **High Impact/Low Probability Analysis** (T30) — develop the scenario in which that force tips against expectations |
| Significant uncertainty about adversary intent or decision-making | **Red Hat Analysis** (T25) — adopt the adversary's perspective to understand how they perceive the same external environment |
| Major assumptions in the analysis are exposed as fragile by the scan | **Key Assumptions Check** (T14) — surface and rate the assumptions the analysis is now resting on |
| External forces suggest the situation could evolve in multiple distinct directions | **Alternative Futures Analysis** (T39) — use the OIT forces as candidate drivers for a scenario matrix |

---

## Analyst principles

**Start from the outside.** The technique's value is precisely in forcing the analyst to begin outside their comfort zone. If you find yourself naturally gravitating toward the Technical category first because it is most familiar, resist. Start with Social or Legal or Environmental — the categories farthest from your specialty are most likely to surface genuinely non-obvious forces.

**Forces, not actors.** A force is a dynamic or trend that operates independently of any single decision-maker — "declining rule-of-law environment in Eastern Europe," not "Russia." Framing forces as actors leads to the same tunnel vision the technique is designed to break.

**Absence is a finding.** If a STEMPLES+ category has nothing to say about the issue at hand, state that explicitly and briefly. An analyst who has thought through Legal and concluded it is not a significant factor has done more rigorous work than one who simply skipped it.

**Relevance is the filter, not completeness.** The goal is not to fill every bin with findings. It is to ensure that no major external force has been overlooked. Three solid, relevant findings per category are more useful than eight superficial ones.

**This technique precedes hypotheses.** Outside-In Thinking is most valuable *before* the analyst has formed a lead hypothesis. If a lead hypothesis is already in place, the Availability Heuristic will filter the STEMPLES+ scan to find only forces that confirm it. Run OIT first; let the hypothesis emerge from the scan.

---

## CTI example

**Issue:** Disruption of ALPHV/BlackCat ransomware operations following FBI infrastructure seizure (December 2023)

| Category | Relevance | Direction | Key Force | Confidence |
|----------|-----------|-----------|-----------|------------|
| **S**ocial | HIGH | Complicates | ALPHV's affiliate model depends on continuous recruitment in cybercriminal forums; exit scam behavior (post-FBI-seizure disappearance) damages trust and impedes relaunch | HIGH |
| **T**echnological | MED | Enables | Rust-based ransomware architecture allowed rapid recompilation and rebranding; no technical barrier to resumed operations | HIGH |
| **E**conomic | HIGH | Amplifies | Affiliates who lost pending payments during the seizure have financial incentive to defect or retaliate; disruption does not eliminate the economic rationale for ransomware | HIGH |
| **M**ilitary | LOW | Neutral | No significant military factor; ALPHV operates as independent criminal enterprise | HIGH |
| **P**olitical | MED | Constrains | FBI action was part of a sustained DoJ cyber-enforcement campaign; political will for continued action appears high; however US-Russia relations limit extradition | MED |
| **L**egal | HIGH | Constrains | Decryptor release and coordination with victims demonstrates law enforcement's new operational playbook; ALPHV operators likely assessing prosecution risk more carefully; jurisdictional safe harbor in Russia remains | HIGH |
| **E**nvironmental | LOW | Neutral | No significant environmental factor | HIGH |
| **S**ecurity | HIGH | Constrains | FBI seizure of affiliate panel gives law enforcement significant visibility into victim organizations and prior operations; this intelligence value likely exceeds the short-term disruption effect | MED |
| **+** Psychological | HIGH | Amplifies | Exit scam behavior suggests ALPHV leadership prioritized personal financial gain over organizational continuity; affiliates who were burned are motivated to expose infrastructure details to competitors or LE | MED |

**Dominant forces:**
1. *Economic*: The financial model driving ransomware is unaffected by the seizure; new infrastructure can be stood up quickly, and affiliates face strong incentives to continue operations under a different brand.
2. *Legal/Security*: Law enforcement's new playbook (victim notification, decryptor release, affiliate data seizure) is more disruptive to operations than infrastructure seizures alone — the intelligence value persists after the operation ends.
3. *Psychological*: The exit scam behavior indicates organizational dysfunction; the highest short-term risk is not a reconstituted ALPHV but former affiliates taking their skills to competing groups (notably RansomHub).

**Key uncertainties:**
- *Political*: Whether the ALPHV operators are actively being sought by Russian domestic law enforcement (as a diplomatic signal) or remain fully protected is unknown and materially affects reconstitution risk.
- *Security*: The full scope of what law enforcement obtained from the seized affiliate panel has not been disclosed; this shapes how aggressively former affiliates will operate.

**Collection priorities:**
1. [Security] Monitor known ALPHV affiliates for migration to RansomHub, LockBit, or new brands — affiliate continuity is the leading indicator of capability reconstitution.
2. [Legal/Political] Track DoJ and international law enforcement announcements for indictments or sanctions targeting named ALPHV principals; pace of action signals political will.
3. [Economic] Track ransom payment trends in the 90 days post-seizure to assess whether affiliate defection has materially degraded operational capacity.

---

## Relationship to other techniques

**Key Drivers Generation (§9.1)** — The natural downstream consumer of an Outside-In Thinking scan. OIT generates the candidate pool of external forces; KDG applies the Fundamental / Uncertain / Consequential filter to select the 4–6 forces worth using as scenario axes. Run OIT first when time permits.

**Key Assumptions Check (§7.1)** — An OIT scan frequently reveals that the current analysis is built on assumptions about external forces that have not been examined. Feed those assumptions directly into a KAC. Conversely, a KAC often surfaces assumptions about the external environment that should trigger an OIT scan on those specific domains.

**SWOT Analysis (§10.4)** — The Opportunities and Threats quadrants of a SWOT are essentially the outputs of an Outside-In Thinking scan. The techniques are complementary: SWOT is better suited when the question is strategic decision-making; OIT is better suited when the question is comprehensive environmental coverage before any analysis is formed.

**Red Hat Analysis (§8.1.3)** — Understanding the external environment the adversary inhabits (via OIT) is prerequisite to a rigorous Red Hat Analysis. An OIT run focused on the adversary's environment — what political, economic, legal, and social forces shape their decision space — can populate the situational awareness section of a Red Hat product.

**Alternative Futures Analysis (§9.6)** — External forces surfaced by OIT, once prioritized via KDG, become the scenario axes for AFA. OIT → KDG → AFA is a complete forward-looking analytical chain.

**Indicators Generation (§9.11)** — The key uncertainties flagged in Step 5c of OIT are natural inputs to indicator generation: for each uncertainty, ask what observable signal would indicate which way that force is resolving.
