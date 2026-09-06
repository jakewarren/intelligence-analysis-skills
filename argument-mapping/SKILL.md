---
name: argument-mapping
description: |
  Performs structured Argument Mapping (Pherson & Heuer §7.9, T22). Builds a hierarchical map of supporting arguments (green), objections (red), and rebuttals (orange) for a single hypothesis. Key deliverable: a bare red node inventory — uncontested objections representing explicit logical flaws that require caveats or a downgraded qualifier before publication.

  Use to pressure-test any single conclusion before publication — attribution claims, intent assessments, capability assessments. Ideal follow-on to ACH.

  Trigger on: "argument map", "argument mapping", "run an argument map", "map the argument", "test this hypothesis", "validate this conclusion", "check the logic", "build the case", "stress test a single claim", "is my argument sound", "what are the counterarguments", "map the reasoning", "what's the case for X". Also trigger after ACH or KAC when the user wants to validate the surviving hypothesis.

  Input: typed claim, pasted analysis, or uploaded document. Output: inline chat, .docx, or HTML.
---

# Argument Mapping

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §7.9 — origins in Wigmore (legal argumentation, early 20th c.); Toulmin (1958); Austhink / Tim van Gelder (computational argument mapping)*

## Purpose

Argument Mapping puts a single hypothesis to a rigorous logical test by constructing a structured, hierarchical representation of every argument for and against it — along with the evidence underneath each argument — and then demanding a rebuttal for every objection. It is the difference between feeling that an assessment is right and *knowing why* it is right.

The core rule: **any objection or counterevidence without a rebuttal is a documented flaw in the argument.** If a finished intelligence product cannot rebut every red-line challenge, it should not express high confidence in its conclusion. The Argument Map makes that vulnerability visible and forces a choice: find the rebuttal, add a caveat, or lower the confidence level.

**When to use it:**

- Before writing a finished product, to ensure the argument will hold up under scrutiny
- After an ACH, to validate the favored hypothesis with full logical depth
- When two analysts disagree — the map identifies precisely *where* the disagreement is located, which is different from *why* they disagree
- In peer review, to give reviewers a structured basis for challenging the analysis
- In CTI attribution, to surface every logical gap between indicator data and the attribution claim

**Relationship to ACH:** ACH is broad (multiple hypotheses, coarse-grained evidence rating). Argument Mapping is deep (single hypothesis, full logical structure). They are sequential, not competing: run ACH first to identify the lead hypothesis, then Argument Mapping to stress-test it.

---

## Step 1: Ingest the input

Accept any of these forms:

- **Claim in chat** — e.g., "Map the argument that Lazarus Group conducted the Bybit exchange heist"
- **Pasted analysis or raw reporting** — Extract the central claim from the material and identify any arguments already made for or against it
- **Uploaded document** — Read the file, identify the key judgment, and extract any supporting or opposing arguments that are already articulated

The central claim must be a **single declarative sentence** — precise enough that it can, in principle, be false. Vague claims ("there is a cyber threat from Russia") produce vague maps. Precise claims ("GRU Unit 74455 conducted the 2022 Viasat KA-SAT attack") produce analytically useful ones.

If the claim is ambiguous or compound, ask the user to sharpen it before proceeding.

---

## Step 2: Determine scope — then proceed

The goal here is to start the map, not to collect answers. Infer as much as possible from context and proceed with stated assumptions. Only ask if something genuinely cannot be inferred.

**Infer the following — do not ask unless ambiguous:**

- **Output format**: If the user mentions a report or document → .docx. If they say "quick check" or "tell me" → inline chat. If they upload a file and want it back → match the file format. Default → inline chat.
- **Depth**: If the user says "full map" or "comprehensive" → full. Default → standard (3–5 top-level arguments, key objections, rebuttals). Lean toward full if the claim is high-stakes (attribution, finished product).
- **CTI framing**: Infer from the claim. "Chinese APT targeting defense contractor" → attribution. "Volt Typhoon pre-positioning" → intent assessment. When in doubt, treat as attribution and probe all categories in Step 4.

**State your assumptions at the start of the output** (one sentence is enough: "Treating this as a standard-depth attribution map, inline format"). This lets the user correct course without blocking the analysis.

The only reason to ask a clarifying question before proceeding is if the central claim itself is so vague or ambiguous that building a map is impossible. Even then, propose your best interpretation and invite correction rather than waiting for a response.

---

## Step 3: State the central claim (the "Root Node")

Write the hypothesis as a precise single-sentence claim at the top of the map. Assign it a **provisional qualifier** — this is the analyst's *starting position*, not the conclusion. The map will test whether that position is justified. After completing Steps 4–9, you will issue a *post-map qualifier* that either confirms or revises this initial one. The post-map qualifier is what goes on the finished product.

| Qualifier | Meaning |
|-----------|---------|
| **Certainly** | No reasonable doubt |
| **Almost certainly** / **Highly likely** | Very strong grounds; minor residual doubt |
| **Probably** / **Likely** | Preponderance of evidence; meaningful alternative remains |
| **Possibly** / **May** | Credible but not dominant; significant competing explanations |
| **Unlikely** | Evidence tilts against; but not ruled out |

If the user has not stated a qualifier, assume a provisional "Probably" and note it. The map's job is to determine whether that starting point holds.

> *CTI example: "Almost certainly [provisional], the intrusion set designated UNC4841 is responsible for the mass exploitation of Barracuda ESG appliances."*

**Important:** When you reach Step 9 and find bare red nodes, you must revise the qualifier downward if the evidence warrants it. The revised qualifier must appear in the final output header — not only in a recommendations paragraph. A qualifier discrepancy (e.g., writing "Almost certainly" in the header while recommending "Probably" in Section 4) is an analytic error.

---

## Step 4: Build the supporting argument layer (Green)

Identify all top-level reasons why the claim is true. These are the **arguments** (sometimes called "co-premises" or "reasons") — general assertions that, if true, lend force to the central claim. They are connected to the root node with a green line.

For each argument, ask: *"If this is true, does it give me reason to believe the root claim?"* If yes, it belongs here. If it depends on another argument being established first, it belongs as a sub-argument (see Step 5).

**Good argument statements** are concise declarative sentences, not fragments:
- ❌ "TTP overlap"
- ✅ "The intrusion TTPs are consistent with the actor's previously documented tradecraft, including use of custom implants and living-off-the-land binaries"

### CTI argument categories to probe

For attribution claims, systematically probe these categories to ensure coverage:

- **Capability**: Does the actor have the technical means to conduct this operation?
- **Intent / motivation**: Does the actor have a plausible reason to conduct this operation at this time?
- **Opportunity / access**: Did the actor have the access necessary to conduct this operation?
- **TTP alignment**: Does the tradecraft match the actor's known methods?
- **Infrastructure attribution**: Does the infrastructure link back to the actor?
- **Timing**: Is the timing of the operation consistent with the actor's operational patterns?
- **Victim targeting**: Is the victim consistent with the actor's targeting profile?
- **Indicator overlap**: Do specific technical indicators (malware families, C2 infrastructure, tooling) link to the actor?

For threat or capability assessments, probe: technical capacity, resource availability, operational history, external support, and stated intent.

---

## Step 5: Attach evidence to each argument (Green sub-nodes)

Under each top-level argument, attach the **specific evidence** that supports it. Evidence nodes are connected to their parent argument with a green line.

For each evidence item, record:

- **The evidence statement** — Specific, factual, and neutral. Not a conclusion. (e.g., "Malware sample SHA256 [hash] shares a 94% code similarity with BLINDINGCAN, attributed to Lazarus Group by CISA and FBI")
- **Source credibility**: HIGH (confirmed, multiple corroborating sources), MEDIUM (single source, partially corroborated), LOW (unverified, single source, possible fabrication)
- **Source type**: HUMINT, SIGINT, OSINT, TECHINT (malware/forensic analysis), own analysis, gap/absence

**The "because" test:** State the argument, then ask: *"Because?"* The answer should be the evidence. If you cannot complete this sentence, the argument has no evidentiary support — it is an assumption masquerading as a reason.

**Absence of evidence as evidence:** Note when expected indicators are *absent*. If the actor reliably uses a specific implant and it is not present in this intrusion, that is a red-line data point (see Step 6). The dog that did not bark is often more diagnostic than confirming evidence.

---

## Step 6: Identify objections and counterevidence (Red)

Now challenge the claim from the other direction. Identify every significant argument *against* the root claim and every piece of evidence that is inconsistent with the supporting arguments. These are connected with red lines.

### Categories of objection to probe:

**Objections to the root claim:**
- What alternative actor could plausibly have conducted this operation? (Competing attribution)
- Could this be a false flag — deliberate planting of indicators to implicate the named actor?
- Could this be a coincidence — unrelated actors using similar tools or infrastructure?
- Is there a simpler or more parsimonious explanation?

**Counterevidence to supporting arguments:**
- For each green evidence node: is there any evidence inconsistent with it?
- For each green argument: does any evidence undercut the warrant connecting it to the root claim?

**CTI-specific challenges to always raise:**
- Tool reuse by multiple actors (commodity malware, shared infrastructure)
- Infrastructure recycling or resale (C2 IPs attributed to one actor later reused by others)
- False-flag indicators (deliberate use of another actor's TTPs or malware)
- Compilation timestamp manipulation
- Source reliability issues (single-source reporting, potential fabrication, limited collection coverage)
- Technical indicator ambiguity (code similarity that falls short of unique attribution)

### Write each objection as a complete sentence

- ❌ "False flag possibility"
- ✅ "The malware code similarities could result from deliberate borrowing of Lazarus Group TTPs by a third-party actor seeking to implicate North Korea"

---

## Step 7: Generate rebuttals (Orange)

For each red-line objection or piece of counterevidence, attempt a rebuttal. Rebuttals are connected to their target objection with an orange line.

A valid rebuttal does one of three things:
1. **Explains away** the objection — the counterevidence is unreliable, misattributed, or does not actually contradict the argument
2. **Limits the scope** of the objection — the objection is partially valid but does not undermine the overall claim
3. **Shows the objection is non-diagnostic** — even if the counterevidence is true, it is equally consistent with the root claim being true (see Diagnostic Reasoning, §7.5)

**Write each rebuttal as a complete sentence that directly addresses the objection it rebuts.**

> *Example:*
> - **Objection (red):** "The APT tool used in this intrusion was leaked on hacking forums in 2020 and could have been used by any actor"
> - **Rebuttal (orange):** "The version used in this intrusion contains a custom C2 communication protocol not present in the leaked version, indicating the actor has access to the private development branch"

---

## Step 8: Identify bare red nodes — the analytical deliverable

**A bare red node is an objection or counterevidence item with no orange rebuttal.** This is the most important output of an Argument Map.

Each bare red node represents either:
- A genuine logical vulnerability in the argument (the objection has merit and cannot be answered)
- A collection gap (the rebuttal likely exists but the analyst does not have the information to make it)
- An assumption buried in the argument (the rebuttal is being assumed rather than evidenced)

**Inventory every bare red node.** For each one, determine:

| Bare Red Node Assessment | Implication |
|--------------------------|-------------|
| **Cannot be rebutted with available information** | This is a flaw. The qualifier on the root claim must be reduced, or the claim must be caveated explicitly in the product. |
| **Likely rebuttal exists but information is unavailable** | This is a collection gap. Generate a collection requirement. |
| **Rebuttal exists but is itself an assumption** | Elevate this assumption to the KAC for explicit treatment. |

The number and severity of bare red nodes determines argument soundness (Step 9).

---

## Step 9: Assess overall argument soundness

Evaluate the argument across four dimensions:

### 9a. Logical completeness
Have all significant supporting arguments been identified? Have all significant objections been raised? An argument map that has only green nodes is not thorough — it reflects confirmation bias, not rigorous analysis.

### 9b. Evidential sufficiency
For each top-level green argument: is it supported by at least one HIGH or MEDIUM credibility evidence item? An argument with no evidentiary backing is an assumption. Flag it.

### 9c. Rebuttal coverage
What percentage of red-line items have orange rebuttals? This is the "rebuttal rate." A high rebuttal rate increases confidence. A low rebuttal rate may indicate the analyst has not invested in addressing objections, or that the objections are genuinely unanswerable.

### 9d. Warrant quality
For each top-level argument, assess the **warrant** — the logical bridge connecting the argument to the root claim. Is the inferential step sound? Common warrant failures:
- **Correlation-causation** conflation (infrastructure overlap doesn't prove the same actor)
- **Base rate neglect** (the TTP appears in many intrusion sets, not just this one)
- **Temporal fallacy** (the actor used this TTP two years ago; has behavior changed?)

---

## Step 10: Produce the output

### Required structure

**Header:** Root claim | **POST-MAP QUALIFIER** (revised after Step 9) | Date | Analyst (if provided)

If the post-map qualifier differs from the analyst's initial qualifier, note it explicitly: e.g., *"Initial claim: 'Almost certainly' → Post-map assessment: 'Probably' — downgraded due to 2 unresolved bare red nodes."*

**Section 1 — The Argument Map**

Present the full argument hierarchy. In text format, use indentation and color-coded labels to show the structure:

```
[ROOT CLAIM] "[POST-MAP QUALIFIER], [claim]."
│
├── ✅ ARGUMENT 1: [Top-level supporting argument]
│   ├── 🟢 EVIDENCE: [Supporting evidence — credibility: HIGH/MED/LOW, source type]
│   ├── 🟢 EVIDENCE: [Supporting evidence]
│   └── 🔴 COUNTER-EVIDENCE: [Inconsistent item]
│       └── 🟠 REBUTTAL: [Orange-line rebuttal]
│
├── ✅ ARGUMENT 2: [Top-level supporting argument]
│   ├── 🟢 EVIDENCE: [Supporting evidence]
│   └── 🔴 OBJECTION: [Objection to this argument]
│       └── ⚠️ BARE RED NODE — No rebuttal available
│
└── 🔴 OBJECTION TO ROOT CLAIM: [Challenge to the overall claim]
    └── 🟠 REBUTTAL: [Orange-line rebuttal]
```

**Key:**
- ✅ Green argument (supports root claim)
- 🟢 Green evidence (supports parent argument)
- 🔴 Red objection or counterevidence
- 🟠 Orange rebuttal
- ⚠️ Bare red node (no rebuttal — explicit vulnerability)

**Section 2 — Bare Red Node Inventory**

List every bare red node with:
- The uncontested objection
- Assessment: genuine flaw / collection gap / buried assumption
- Recommended action: reduce qualifier / add caveat / generate collection requirement / run KAC

**Section 3 — Argument Soundness Assessment**

A direct evaluative paragraph covering logical completeness, evidential sufficiency, rebuttal coverage, and warrant quality. End with an explicit verdict:

> *"Post-map qualifier: [Probably / Almost certainly / Possibly / etc.]. Maintained / Upgraded from / Downgraded from analyst's initial '[initial qualifier]' because [one sentence rationale]."*

This verdict is not a recommendation — it is the conclusion. It must match the qualifier shown in the header above Section 1.

**Section 4 — Analytic Recommendations**

Specific, actionable guidance:
- Qualifiers that should be adjusted in the written product
- Caveats that must appear in the product to reflect bare red nodes
- Collection requirements generated by unresolvable objections
- Follow-on techniques recommended (KAC for load-bearing assumptions; Deception Detection if false-flag objections are unresolved; Diagnostic Reasoning for ambiguous evidence)

---

## Analyst principles

**Green nodes are not proof; they are reasons.** An argument map full of green nodes feels persuasive. It is not the same as being correct. The value of the map is in the red nodes.

**Objections must be taken seriously.** The goal is not to dismiss every red-line item quickly with a perfunctory rebuttal. A rebuttal is only valid if it genuinely addresses the objection. Acknowledge where the rebuttal is weak.

**A map without red nodes was not done honestly.** Every serious analytic claim about adversary intent, capability, or attribution has legitimate objections. If none appear, the analyst has not tried hard enough to find them — or has unconsciously filtered them out (Confirmation Bias).

**The qualifier must match the map.** If the map has three bare red nodes of high severity, the root claim cannot be stated as "almost certainly." The map is a forcing function for honest confidence calibration.

**Source credibility matters.** A HIGH-credibility evidence item that is inconsistent with a supporting argument is more damaging to that argument than a LOW-credibility item. Weight the analysis accordingly.

---

## Relationship to other techniques

**Analysis of Competing Hypotheses (ACH)** — Run ACH before Argument Mapping when there are multiple competing explanations. ACH identifies the favored hypothesis; Argument Mapping validates it. If no ACH has been run, consider whether there are alternative hypotheses worth examining before investing in mapping a single claim.

**Key Assumptions Check (KAC)** — Bare red nodes that reflect buried assumptions should be elevated into a KAC. The KAC's S/C/U classification and risk rating then feeds back into the Argument Map to calibrate the qualifier.

**Diagnostic Reasoning (§7.5)** — When a red-line objection rests on a piece of evidence, ask whether that evidence is actually diagnostic. If the evidence would exist whether or not the root claim is true, the objection is weaker than it appears.

**Deception Detection (§7.8)** — If multiple false-flag objections survive without rebuttal, escalate to a Deception Detection analysis. An argument map that cannot rebut plausible false-flag scenarios is a warning sign that deception may be in play.

**Adversarial Collaboration (§8.3)** — When two analysts disagree, the Argument Map pinpoints where: the disagreement will be visible as a disputed argument, disputed evidence, or disputed rebuttal. This is more productive than open-ended debate.

---

## Output format guidance

**Inline chat:** Markdown code block for the tree structure. Good for quick pre-publication checks and informal peer review.

**Word (.docx):** Use the `docx` skill. Full formatted report with tree structure in a styled table, bare red node inventory table, and analytic recommendations section. Appropriate for formal peer review and finished intelligence products.

**HTML:** Standalone file with color-coded nodes and collapsible argument branches. Good when the map needs to be shared or embedded in a briefing package.

---

## CTI example: Attribution claim

> **Root claim:** "Almost certainly, UNC2452 (Cozy Bear / APT29) conducted the SolarWinds Orion supply chain compromise discovered in December 2020."

**Supporting arguments (green):**
- The SUNBURST backdoor shares code patterns and infrastructure with TEARDROP and Cobalt Strike tooling previously attributed to APT29
- The operational security and patience exhibited (months-long dormancy period) is consistent with Russian SVR tradecraft
- The targeting profile — U.S. government agencies, defense contractors, think tanks — aligns with SVR collection priorities
- C2 domain generation algorithms used by SUNBURST overlap with known APT29 infrastructure patterns

**Objections (red):**
- No human intelligence or signals intelligence directly confirming Russian state direction has been publicly disclosed
- The sophistication of the operation is within reach of several state-level actors (China, Israel) with similar capabilities

**Rebuttals (orange):**
- The U.S. Intelligence Community, including NSA, FBI, CISA, and ODNI, issued a joint statement attributing the intrusion to "likely Russian origin" — reflecting classified reporting not publicly available
- The combination of targeting, timing (during U.S. election period), and specific TTPs narrows the field significantly; no alternative attribution has been publicly advanced by any IC element

**Bare red nodes:**
- ⚠️ The human/signals intelligence basis for attribution cannot be publicly rebutted — collection gap; qualifier maintained at "almost certainly" based on IC consensus while acknowledging this as a caveat in the product
