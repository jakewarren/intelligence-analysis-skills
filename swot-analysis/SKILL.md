---
name: swot-analysis
description: |
  Performs SWOT Analysis — Decision Support SAT (Pherson & Heuer §10.4, T48). Evaluates Strengths, Weaknesses, Opportunities, and Threats, then extends the grid into a TOWS Matrix for SO/WO/ST/WT strategies. Two modes: (1) Self-assessment of your own org, SOC, or CTI program; (2) Adversary assessment — apply SWOT to a threat actor or APT to produce a capability profile. Mode 2 feeds into Red Hat Analysis.

  Trigger on: "SWOT analysis", "run a SWOT", "strengths and weaknesses", "SWOT matrix", "TOWS matrix", "strategic assessment", "competitive analysis", "capability assessment", "how does our team stack up", "what are our gaps", "assess this threat actor", "what is this APT good at", "where is the adversary weak", "evaluate our posture", "strategic planning". Also trigger when a user wants to assess their org before a key decision or profile a threat actor's operational strengths and vulnerabilities.

  Input: typed objective, pasted context, or uploaded document. Output: inline chat, .docx, or HTML.
---

# SWOT Analysis

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §10.4 — Decision Support Technique T48*

## Purpose

SWOT Analysis evaluates the **S**trengths, **W**eaknesses, **O**pportunities, and **T**hreats relevant to a defined goal or objective. Strengths and Weaknesses are *internal* to the entity being assessed; Opportunities and Threats come from the *external* environment. Completing the grid is the foundation — but the real analytic value emerges in the TOWS extension, which cross-combines the four quadrants to generate concrete strategic options.

**Cognitive traps this technique counteracts**: Confirmation Bias (seeking only information that confirms the preferred option), Anchoring Effect (locking onto an initial estimate), Groupthink (pressure toward surface consensus), Lacking Sufficient Bins (failing to distinguish internal from external factors), Overrating Behavioral Factors (attributing outcomes solely to human intent, ignoring structural conditions), and Overestimating Probability (defaulting to optimistic scenarios).

---

## Identify the mode

Before starting, determine which mode applies:

**Mode 1 — Self-assessment**: The subject being analyzed is the user's own organization, team, program, product, or capability. The objective is to improve decision-making about a plan of action or strategic choice. Produces a SWOT grid and TOWS strategic options.

**Mode 2 — Adversary assessment**: The subject is a threat actor, adversary, competitor, or external organization. The objective is to produce an intelligence assessment of their operational posture — what they are good at, where they are vulnerable, what environmental conditions favor them, and what forces threaten their ability to operate. Produces a threat actor capability profile and a set of exploitation and disruption strategies.

If mode is not clear from context, ask a single short question before proceeding.

---

## Step 1: Ingest the input

Accept any of these forms:

- **Typed objective or question in chat** — e.g., "Run a SWOT on our incident response capability against a ransomware attack" or "Do a SWOT on APT41 in the context of targeting US defense contractors"
- **Pasted analysis, brief, or strategic document** — Extract the subject and objective from the raw material
- **Uploaded document** — Read the file; identify the entity under analysis, the goal or strategic question, and any existing characterization of strengths, weaknesses, or context

If the objective is ambiguous, ask the user to state it as a single sentence before building the grid. A vague objective produces a vague SWOT.

---

## Step 2: Confirm scope briefly

Ask one short message (or skip if obvious from context) covering:

1. **Mode**: Self-assessment or adversary assessment?
2. **Subject and objective**: What exactly is being assessed, and against what goal?
3. **Output format**: Inline chat, Word .docx, or HTML with styled grid?

---

## Step 3: State the objective and subject

Begin the analysis with a crisp framing statement:

> **Subject**: [Organization / team / threat actor / program]
> **Objective**: [The goal or question driving this analysis — one declarative sentence]

> *Mode 1 example: Subject — "XYZ Corp's threat intelligence function." Objective — "Assess whether we have the organizational and technical capability to attribute a nation-state intrusion and publish a credible threat report within 72 hours."*

> *Mode 2 example: Subject — "Sandworm (GRU Unit 74455)." Objective — "Assess Sandworm's operational posture and identify conditions that could enable or degrade their targeting of European energy infrastructure."*

This framing anchors the entire grid. Every item entered in a quadrant should connect directly back to this objective. If a factor doesn't affect the objective, it doesn't belong in the grid.

---

## Step 4: Populate the four quadrants

Work through each quadrant in turn using the structured elicitation prompts below. Aim for **4–8 items per quadrant** — enough to be comprehensive without drowning in noise. Each item should be a concise declarative statement, not a vague category.

---

### 4a — Strengths (Internal / Positive)

*What does the subject do well, relative to the objective? What advantages do they hold that others lack?*

**Mode 1 elicitation prompts:**
- What capabilities, tools, or processes are clearly above average or best-in-class?
- What resources (people, budget, data, relationships, technology) are genuine advantages?
- What track record or institutional knowledge exists that would be hard to replicate quickly?
- What does the organization do reliably and repeatably?
- What do peers or competitors frequently cite as this organization's differentiator?

**Mode 2 elicitation prompts (threat actor lens):**
- What TTPs has this actor demonstrated consistently across multiple campaigns?
- What technical capabilities are confirmed — zero-days, custom malware, OT expertise, supply chain access?
- What organizational resources support sustained operations — funding, infrastructure, tasking from a state sponsor?
- What OPSEC practices have successfully protected their identity and operations?
- What access or positioning has this actor already achieved in the target environment?

**Cyber-specific Strength examples (Mode 1):**
- 24/7 SOC coverage with experienced tier-2 analysts
- Mature threat intelligence platform with normalized IOC feeds
- Established relationships with CISA, FBI CyWatch, and sector ISAC
- Endpoint telemetry from 95% of endpoints via deployed EDR agent

**Cyber-specific Strength examples (Mode 2 — adversary):**
- Demonstrated use of legitimate cloud infrastructure for C2 (Living off the Land)
- Track record of successful spearphishing against defense sector targets
- State sponsor provides diplomatic cover and resourcing insulation
- Custom implant with no public signature at time of assessment

---

### 4b — Weaknesses (Internal / Negative)

*Where does the subject fall short, relative to the objective? What internal gaps or limitations create risk or constrain options?*

**Mode 1 elicitation prompts:**
- What capabilities are missing or underdeveloped for this objective?
- Where does execution routinely fail, slip, or produce substandard output?
- What resource constraints (staffing, budget, tooling, data access) limit effectiveness?
- What dependencies on others create vulnerability if those relationships fail?
- What would an objective external reviewer criticize about the current state?

**Mode 2 elicitation prompts (threat actor lens):**
- What TTPs have been exposed, disrupted, or burned in previous campaigns?
- What capability gaps force this actor to rely on third parties, public tools, or workarounds?
- What OPSEC failures have been documented — leaked infrastructure, burned personas, exposed malware?
- What internal constraints limit their operational tempo — limited operators, single sponsor dependency, jurisdiction risk?
- Where has this actor been forced to adapt or retreat under pressure?

**Cyber-specific Weakness examples (Mode 1):**
- No dedicated malware reverse engineering capability; must outsource
- Threat intel function limited to IOC ingestion — no finished intelligence production
- Playbooks not updated in 18+ months; response procedures for OT incidents do not exist
- Legal/privacy review process creates 72-hour delay on threat intelligence sharing

**Cyber-specific Weakness examples (Mode 2 — adversary):**
- Repeated use of the same C2 infrastructure across campaigns enables rapid sinkholing
- No demonstrated capability against hardened targets with mature EDR deployment
- Relies on spearphishing entry vector; no known watering hole or supply chain capability
- Operations disrupted or attributed in 3 of 5 most recent campaigns — OPSEC degrading

---

### 4c — Opportunities (External / Positive)

*What external conditions, trends, or events could benefit the subject's pursuit of the objective, if exploited?*

**Mode 1 elicitation prompts:**
- What external trends (regulatory, technological, geopolitical, organizational) favor action now?
- What gaps in the competitive landscape or threat environment create favorable openings?
- What partnerships, programs, or resources are available externally but not yet leveraged?
- What recent events (incidents, policy shifts, adversary errors) have created new openings?
- What is the window of opportunity — is this condition time-limited?

**Mode 2 elicitation prompts (threat actor lens):**
- What unpatched vulnerabilities, exposed services, or architectural weaknesses in the target environment enable exploitation?
- What geopolitical or organizational moments create cover, distraction, or reduced defender attention?
- What supply chain or third-party relationships in the target create access vectors?
- What collection gaps or blind spots in the target's detection posture reduce the actor's risk?
- What criminal or state partnerships could enhance this actor's capabilities?

**Cyber-specific Opportunity examples (Mode 1):**
- Executive leadership has just approved a security transformation budget following a near-miss incident
- New CISA partnership program provides access to classified threat indicators
- Legacy system modernization program creates opportunity to bake security in from the start
- Peer organization's recent breach has created internal political will for capability investment

**Cyber-specific Opportunity examples (Mode 2 — adversary):**
- Target organization's recent merger created a period of elevated IT complexity and reduced security staffing
- High concentration of target employees on LinkedIn enables social engineering and spearphishing
- Internet-exposed VPN appliance running unpatched firmware — CVE with public PoC available
- Target relies on a single managed security provider; compromising that provider compromises all clients

---

### 4d — Threats (External / Negative)

*What external conditions, actors, or trends could harm the subject's ability to achieve the objective?*

**Mode 1 elicitation prompts:**
- What adversary capabilities, TTPs, or activities specifically threaten this objective?
- What external regulatory, legal, or political constraints could limit options or impose costs?
- What trends in the threat landscape are moving faster than our ability to respond?
- What dependencies on external parties (vendors, cloud providers, partners) create exposure?
- What would most disrupt this plan if it changed suddenly?

**Mode 2 elicitation prompts (threat actor lens):**
- What law enforcement actions, government programs, or disruption campaigns specifically target this actor or their TTPs?
- What defensive improvements in target organizations would neutralize this actor's core capabilities?
- What public attribution, sanctions, or diplomatic pressure would constrain their operational freedom?
- What rival groups or internal factional tensions could degrade cohesion?
- What technical developments (improved endpoint detection, zero-trust adoption, honeypot maturation) close the actor's attack surface?

**Cyber-specific Threat examples (Mode 1):**
- Sophisticated APT group has demonstrated persistent targeting of our sector with TTPs our current controls cannot reliably detect
- Vendor dependency: single cloud provider failure would take down security monitoring for 4–8 hours
- Regulatory timeline (DORA, SEC Rule 240.1a) imposes incident disclosure requirements we are not currently equipped to meet
- Staffing: 3 of 7 senior analysts are currently in exit conversations

**Cyber-specific Threat examples (Mode 2 — adversary):**
- Active DOJ and FBI cyber division investigation with grand jury empaneled
- CISA and sector ISACs actively sharing actor-specific IOCs and TTPs — detection improving across targets
- Zero-trust adoption program at primary target narrows lateral movement options significantly
- Competing criminal group recently arrested and may cooperate with authorities, exposing shared infrastructure

---

## Step 5: Quality-check the grid

Before proceeding to strategy generation, apply these four checks:

1. **Objective relevance**: Every item should matter for the stated objective. Remove items that are true but irrelevant.
2. **Internal vs. external discipline**: Strengths/Weaknesses describe the subject's *own* state. Opportunities/Threats describe the *external environment*. If an item describes something the subject did, or is, it is internal. If it describes a condition outside the subject's control, it is external. Misclassification is one of the most common SWOT errors.
3. **Specificity**: Vague items ("good communication") are not actionable. Push each item to be specific enough that someone could act on it.
4. **Balance**: If any quadrant has fewer than 3 items or more than 10, reconsider. A quadrant with one item is almost always a failure of elicitation. A quadrant with 12 items needs pruning.

---

## Step 6: TOWS Matrix — Strategy Generation

This is the step that separates a structured SWOT from a simple list. The TOWS Matrix cross-combines the quadrants to generate four classes of strategic options. Work through each combination:

| Strategy type | Logic | Question to ask |
|---|---|---|
| **SO — Maxi-Maxi** | Use Strengths to exploit Opportunities | *How can we deploy our best capabilities to take advantage of the most favorable external conditions?* |
| **WO — Mini-Maxi** | Use Opportunities to overcome Weaknesses | *How can we use favorable external conditions to address or compensate for our internal gaps?* |
| **ST — Maxi-Mini** | Use Strengths to counter Threats | *How can we use our best capabilities to neutralize the most dangerous external threats?* |
| **WT — Mini-Mini** | Reduce Weaknesses to avoid Threats | *How can we minimize our internal vulnerabilities to reduce exposure to the worst external threats?* |

For each quadrant combination, generate **2–4 concrete strategic options**. Each option should name the specific Strength/Weakness and the specific Opportunity/Threat it draws from. Vague strategies ("improve capabilities") are not acceptable outputs.

> *Mode 1 SO example: "Leverage our established FBI CyWatch relationship [S] and the current executive security investment window [O] to rapidly deploy the deception technology capability we've been unable to fund previously."*

> *Mode 2 ST example (adversary assessment): "The actor's Living off the Land capability [S] is partially neutralized by the target's recent Sentinel deployment [T] — but Sentinel is only on corporate endpoints, not OT. Their most viable path forward uses existing OT access [S] against the still-unmonitored control system network."*

---

## Step 7: Prioritization

Not all strategic options are equally actionable. Assess each TOWS option on two dimensions:

| Dimension | Question |
|---|---|
| **Feasibility** | Can this be acted on with available resources and authority? High / Medium / Low |
| **Impact on objective** | If executed, how much does this advance the objective? High / Medium / Low |

Rank or bucket the options. The highest-priority options are **High Feasibility + High Impact** (act now). Options that are High Impact but Low Feasibility are candidates for investment to change feasibility. Low Impact options should be deferred or dropped.

---

## Step 8: Produce the output

### Required structure

**Header**: Subject | Objective | Date | Mode | Analyst (if provided)

**Section 1 — Framing**
Subject and objective as stated in Step 3.

**Section 2 — SWOT Grid**
Present all four quadrants in a 2×2 grid or as four clearly labeled lists. Items should be numbered within each quadrant for ease of reference in the TOWS section.

| | **Helpful** | **Harmful** |
|---|---|---|
| **Internal** | **Strengths** (S1, S2…) | **Weaknesses** (W1, W2…) |
| **External** | **Opportunities** (O1, O2…) | **Threats** (T1, T2…) |

**Section 3 — TOWS Matrix**
Four strategic option sets (SO, WO, ST, WT), each with 2–4 options that reference specific grid items by number.

**Section 4 — Priority Strategic Options**
Top 3–5 options ranked by Feasibility × Impact, with brief rationale for each.

**Section 5 — Key Risks and Watchlist** (especially for Mode 2 / adversary assessments)
What developments would materially change this assessment? What should be monitored to know if the situation is shifting?

---

## Output format guidance

**Inline chat**: Markdown tables and lists. Good for working sessions, quick strategic scans, and collaborative iteration.

**Word (.docx)**: Use the `docx` skill. Formatted report with styled 2×2 SWOT grid (color-coded quadrants), TOWS table, priority options table, and executive summary. Appropriate for formal products, leadership briefings, or strategic planning documents.

**HTML**: Standalone file with color-coded SWOT grid (green for S/O, red/amber for W/T), styled TOWS table with strategy types clearly differentiated. Good for embedding in project briefs or sharing with a cross-functional team.

---

## Potential pitfalls and how to avoid them

**Mistaking the SWOT for the strategy**: The grid is a tool for organizing information, not the end product. Always produce TOWS strategic options. A SWOT that ends with the 2×2 grid has delivered half its value.

**Internal/external confusion**: Analysts routinely miscategorize factors. A common error: "lack of budget" is listed as a Threat when it is a Weakness (it is internal). Another: "strong threat actor" is listed as a Weakness when it is a Threat. When in doubt — if the subject controls it or owns it, it is internal (S or W). If it exists in the environment regardless of what the subject does, it is external (O or T).

**Single-goal blinders**: SWOT focuses on one objective at a time. This means it is blind to the costs of the chosen option relative to alternatives. If multiple paths to the objective exist, consider running a separate SWOT for each, or use a Decision Matrix (T51) to weigh options comparatively.

**Generic items**: SWOT grids populated with generic statements ("good team," "complex threat landscape") produce generic strategies. Every item should be specific enough to be falsifiable. Ask: could someone familiar with this subject dispute this? If it is too vague to dispute, it is too vague to be useful.

**Unbalanced quadrants**: If the Threats quadrant has 10 items and Strengths has 2, the grid has anchored on danger. Rebalance by deliberately pushing for strengths and opportunities before moving on.

---

## Cyber intelligence applications

**SOC capability assessment**: Run a SWOT before a major investment decision or red team engagement. Map what the SOC does well (Strengths: SIEM coverage, analyst experience), where it falls short (Weaknesses: no OT visibility, no DFIR playbooks), what external conditions enable improvement (Opportunities: new EDR program, incoming threat intel sharing agreement), and what is coming for it (Threats: sophisticated phishing campaigns, regulatory deadlines). The TOWS strategies become the roadmap for the security program.

**Threat actor capability profiling (Mode 2)**: SWOT is a rigorous alternative to informal capability assessments. Apply it to an APT before writing a threat report, or as a structured input to Red Hat Analysis. Map confirmed TTPs as Strengths; exposed infrastructure or burned implants as Weaknesses; unpatched target environments as Opportunities; law enforcement activity or defensive improvements as Threats. The TOWS output tells you what this actor is likely to do next and where they are most vulnerable to disruption.

**New tool or technology adoption**: Evaluating a new SIEM, SOAR, deception platform, or threat intel service? SWOT the decision: Strengths of the current state (don't lose what you have), Weaknesses being addressed (what pain does this solve?), Opportunities in the vendor ecosystem or the threat landscape, and Threats from implementation (deployment risk, vendor lock-in, integration complexity).

**Breach disclosure strategy**: Before disclosing an incident publicly or to regulators, SWOT the disclosure options. Strengths: early notification builds trust. Weaknesses: limited forensic picture at time of disclosure may undermine credibility. Opportunities: regulatory cooperation credit, sector-wide warning value. Threats: adversary learns detection was successful and adapts; plaintiff attorneys begin collection.

**CTI function build-out**: When standing up or maturing a CTI program, SWOT the current state. Forces systematic identification of what the team does well (avoiding the trap of self-deprecating "we have nothing"), what is missing, what organizational conditions favor investment, and what risks threaten the program's sustainability.

---

## Relationship to other techniques

**Outside-In Thinking / STEMPLES+** (T23) — The Opportunities and Threats quadrants of a SWOT are operationally equivalent to the external factors produced by Outside-In Thinking. STEMPLES+ (Social, Technical, Economic, Military/Political, Legal, Environmental, Security) is an effective elicitation device to systematically populate the external quadrants before populating the internal ones.

**Impact Matrix** (T47) — The Impact Matrix maps stakeholder reactions to a decision; SWOT maps the strategic landscape before making the decision. When a decision is complex and stakeholder management matters, run SWOT first to identify the strategic options, then use Impact Matrix to assess how each option will land with key actors.

**Red Hat Analysis** (T25) — Mode 2 SWOT (adversary assessment) feeds naturally into Red Hat Analysis. The SWOT produces the capability map; Red Hat adopts the adversary's frame to simulate how they will actually think through their options given that capability map.

**Key Assumptions Check** (T14) — SWOT assessments rest on numerous assumptions: that listed Strengths actually hold up, that Opportunities won't evaporate, that Threats are real. After completing a high-stakes SWOT, run a KAC to surface the most fragile assumptions — especially any WT (Mini-Mini) strategies that assume weaknesses can be addressed before threats materialize.

**Key Drivers Generation** (T34) — If this SWOT reveals significant uncertainty about which external conditions will dominate, use KDG to identify the 2–3 key drivers that most determine whether Opportunities or Threats prevail. This bridges SWOT into scenario planning via Alternative Futures Analysis.

**Alternative Futures Analysis** (T39) — When the external environment (Opportunities and Threats) is highly uncertain and the stakes are high, convert the SWOT's external quadrants into scenario drivers. The four AFA scenarios then each represent a different configuration of external conditions — showing which TOWS strategies remain valid across scenarios (robust strategies) and which only work in favorable conditions (fragile strategies).
