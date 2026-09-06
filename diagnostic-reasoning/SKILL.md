---
name: diagnostic-reasoning
description: |
  Performs Diagnostic Reasoning (DR) — Pherson & Heuer §7.5, T18. Tests whether a single new piece of evidence discriminates between competing hypotheses or merely confirms existing beliefs. Central question: "If an alternative were true, would I still see this?" If yes, the evidence is non-diagnostic. Essential for CTI: a lone IOC, code string, or TTP overlap rarely confirms attribution.

  Trigger on: "is this evidence diagnostic", "does this confirm my hypothesis", "run a diagnostic reasoning", "alternative explanations for this", "does this IOC confirm attribution", "is this code string enough to attribute", "could this be a false flag", "does this TTP confirm the actor", "run a DR on this indicator", "validate this attribution", "sanity-check this new intel". Also trigger when an analyst updates an assessment on a single item — especially in CTI when an IOC match is treated as attribution.

  Input: typed description, pasted reporting, or uploaded document. Output: inline chat, .docx, or HTML.
---

# Diagnostic Reasoning (DR)

*Source: Pherson & Heuer, Structured Analytic Techniques for Intelligence Analysis, 3rd ed., §7.5*

## Purpose

Diagnostic Reasoning tests whether a new piece of information is genuinely discriminating — whether it tells you something *exclusive* about your lead hypothesis — or whether it is equally consistent with alternative explanations and therefore analytically worthless as confirmation.

The insight at the heart of the technique: most evidence that appears to *confirm* the lead hypothesis turns out, on examination, to be equally consistent with one or more alternatives. That evidence can neither confirm nor disconfirm. Only information that is *inconsistent* with an alternative actually has diagnostic value — it allows you to rule that alternative out.

This is the micro-scale counterpart to ACH. Where ACH evaluates an entire evidence set against a full hypothesis matrix, Diagnostic Reasoning evaluates a *single item* in the moment you receive it, before it can be assimilated uncritically into the prevailing mental model.

---

## When to Use

Use Diagnostic Reasoning any time you find yourself making a snap judgment about what a new development means. Specific triggers:

- A new intelligence report arrives that "confirms" an existing belief
- A new development seems to validate the current assessment
- A new source's reporting aligns suspiciously well with the lead hypothesis
- A decision maker is about to use a single data point to justify a policy position
- You are being asked to update an assessment based on a single new item

The technique is especially important when the analyst is already committed to a position, because that commitment makes Confirmation Bias most dangerous.

---

## Step 1: Ingest the input

Accept any of these:

- **Chat description** — The analyst describes the new information or development in their own words
- **Pasted reporting** — Raw intelligence text, a cable, a SIGINT snippet, a news item
- **Uploaded document** — Read the document and extract the key new facts or claims

Your goal is to identify exactly one **focal item**: the new piece of information or development whose meaning is being evaluated. If the user has presented multiple items at once, ask them to identify the one they want to start with, or run DR on each sequentially.

---

## Step 2: Clarify scope (briefly)

Ask one short message covering:

1. **The lead hypothesis**: What is the analyst's current prevailing explanation or assessment? (State it as a single declarative sentence.)
2. **Output format**: Inline chat (fast, good for operational use), Word .docx (formal product), or HTML (visual, shareable)?

If the lead hypothesis is clear from context, skip asking about it. If the request is clearly informal ("quick check"), default to inline.

---

## Step 3: State the focal setup

State clearly before proceeding:

- **Focal item**: The new information being evaluated, in one sentence
- **Lead hypothesis (H₀)**: The current prevailing explanation or assessment
- **Analyst's initial reaction**: What the analyst took this information to mean at first glance

> *Example (CTI):*
> *Focal item: "A new malware sample submitted for analysis contains a code string previously observed exclusively in APT28 tooling."*
> *Lead hypothesis (H₀): "This intrusion was conducted by APT28 (Russian GRU)."*
> *Initial reaction: The shared code string confirms APT28 attribution.*
>
> *Example (traditional HUMINT):*
> *Focal item: "A HUMINT report indicates that Country X has resumed uranium conversion activities at a previously dormant site."*
> *Lead hypothesis (H₀): "Country X is actively pursuing nuclear weapons capability."*
> *Initial reaction: This confirms H₀.*

---

## Step 4: Generate alternative hypotheses

Brainstorm the alternative explanations a skeptical or differently-positioned analyst might reasonably consider. Aim for 3–6 alternatives. Diversity matters more than volume — look for structurally different explanations, not just variations on the same theme.

Use these lenses to broaden the alternative set:

- **Denial & Deception (D&D)**: Could an adversary have staged, planted, or timed this information deliberately?
- **Innocent explanation**: Is there a mundane or coincidental explanation unrelated to the lead hypothesis?
- **Measurement/source artifact**: Is the information reporting an artifact of collection methodology, source access, or framing?
- **Alternative actor**: Could a different actor, with different goals, explain the same observation?
- **Reversed causality**: Could the relationship be backwards — does the observation indicate something *other* than what the lead hypothesis requires?
- **Timing anomaly**: Why now? Does the timing itself suggest an alternative explanation?

**Additional lenses for cyber intelligence:**

- **False flag / attribution artifact**: The most important cyber-specific alternative. Adversaries routinely plant code strings, fake compilation metadata, tool signatures, and language artifacts to frame a different actor. The 2018 Olympic Destroyer malware was specifically engineered to mimic Lazarus Group (North Korea) while the actual author was Sandworm (Russia) — the false flag deceived multiple major CTI vendors on initial analysis. Whenever a piece of evidence seems to *nail* attribution, explicitly ask whether that evidence was put there to be found.
- **Commodity or leaked tooling**: Many tools and techniques once exclusive to a single actor are now commodity — leaked (e.g., Shadow Brokers release of NSA tooling), repurchased, or re-implemented. Shared tooling is not shared identity. A Cobalt Strike beacon, a Mimikatz call, or a specific LOLBin sequence tells you almost nothing about actor identity by itself.
- **Shared or resold infrastructure**: IP addresses, ASNs, bullet-proof hosting, and anonymization services are shared across actors. A C2 IP associated with a known APT cluster may be used by a different actor using the same infrastructure provider, or may be a victim acting as an unwitting relay.
- **Collection artifact / sensor change**: Did detection rates change because *activity* changed, or because a *new detection rule* was deployed, a new log source was onboarded, or a SIEM threshold was adjusted? Evidence of "increased activity" often reflects increased visibility, not increased intent.
- **Red team / researcher / scanner**: Observed behavior may originate from an authorized penetration test, a security researcher scanning for vulnerable hosts, or an automated internet scanner. These are operationally irrelevant and should be eliminated before they drive assessment updates.

Label alternatives H₁, H₂, H₃, etc.

> *Example alternatives (CTI — APT28 code string):*
> *H₁: The code string was deliberately planted by a different actor to implicate APT28 (false flag).*
> *H₂: The code is from a shared or leaked codebase now used by multiple unrelated actors (commodity tooling).*
> *H₃: The malware was developed by a financially motivated actor who purchased or copied APT28 modules.*
> *H₄: The sample is from a security researcher or red team using captured APT28 tooling in a lab environment.*
>
> *Example alternatives (traditional HUMINT):*
> *H₁: Country X is conducting a negotiating feint — resuming activities to create leverage for sanctions relief.*
> *H₂: Activity is routine maintenance or decommissioning, not weapons-program resumption.*
> *H₃: A third party (State Y) is using Country X's facility as cover for its own program.*
> *H₄: The HUMINT source is fabricating or has been manipulated.*

---

## Step 5: Apply the diagnostic test to each alternative

This is the core step. For each alternative hypothesis Hₙ, ask:

> **"If Hₙ were true, how likely would it be that I would have observed this same focal item?"**

Score each alternative on a three-point scale:

| Score | Label | Meaning |
|-------|-------|---------|
| **C** | Consistent | If Hₙ were true, observing this focal item would be expected or plausible |
| **I** | Inconsistent | If Hₙ were true, observing this focal item would be unlikely or surprising — this evidence argues against Hₙ |
| **N** | Neutral | If Hₙ were true, the focal item would be equally likely or unlikely as under any other hypothesis |

Apply the same test to H₀:

> *"If the lead hypothesis (H₀) were true, how likely would it be that I would observe this focal item?"*

Now build the diagnostic matrix:

*CTI example (APT28 code string):*

| Hypothesis | Description | Consistency with Focal Item | Notes |
|---|---|---|---|
| H₀ (Lead) | APT28 conducted this intrusion | C | APT28 would use its own code — but that's precisely what the alternatives also predict |
| H₁ | False flag — different actor planted APT28 code | C | A planted string would look identical to genuine use; this is exactly what we'd expect to see |
| H₂ | Commodity/leaked tooling — unrelated actor | C | Shared codebases mean any actor could produce this artifact |
| H₃ | Financially motivated actor using purchased modules | C | Criminal actors regularly incorporate nation-state tool fragments |
| H₄ | Red team / researcher using captured tooling | C | Lab samples using known tooling would produce this same artifact |

**Result: 🔴 Non-diagnostic.** The code string is consistent with all five hypotheses. It cannot confirm APT28 attribution.

*Traditional HUMINT example (uranium conversion):*

| Hypothesis | Description | Consistency with Focal Item | Notes |
|---|---|---|---|
| H₀ (Lead) | Country X pursuing nuclear weapons | C | Expected — but this alone proves nothing |
| H₁ | Negotiating feint | C | Uranium conversion is equally useful as a bargaining chip |
| H₂ | Routine maintenance | I | Maintenance doesn't typically involve restarting conversion lines |
| H₃ | Third-party cover | C | Plausible — same observable behavior |
| H₄ | Fabricated/manipulated source | C | A plant would look exactly like this |

---

## Step 6: Assess diagnostic value

After completing the matrix, apply the diagnostic value rule:

**The focal item is non-diagnostic with respect to any alternative it is *consistent* with.** It cannot be used as evidence for H₀ against those alternatives.

**The focal item has diagnostic value only against hypotheses it is *inconsistent* with** — those alternatives can be reduced in credibility or ruled out.

Assign an overall diagnostic value rating:

| Rating | Condition |
|---|---|
| 🔴 **Non-diagnostic** | The focal item is consistent with all or most alternatives — it tells you almost nothing beyond what you already believed |
| 🟡 **Partially diagnostic** | The focal item rules out one or more alternatives while remaining consistent with others |
| 🟢 **Highly diagnostic** | The focal item is inconsistent with most alternatives — it significantly narrows the hypothesis space |

> *In the HUMINT example above: The focal item is **Partially diagnostic** — it is consistent with H₀, H₁, H₃, and H₄, but H₂ (routine maintenance) is inconsistent. The analyst should NOT treat this report as confirmation of the nuclear weapons hypothesis, but can reduce confidence in the maintenance explanation.*

---

## Step 7: Deception flag (always check)

Before finalizing, apply the Deception Check: ask whether the focal item could have been *designed* to reach the analyst and be interpreted in a way that favors the lead hypothesis.

Indicators that raise the deception flag:
- The information is unusually timely — it arrives precisely when the analyst most needs it
- The source is new or unvalidated
- The information is surprisingly clear or unambiguous — real intelligence rarely is
- Multiple corroborating reports all trace back to a single original source
- The information is not just consistent with the lead hypothesis — it is *perfectly* consistent in a way that seems almost constructed

**Cyber-specific deception indicators:**
- The attribution artifact (code string, mutex, PDB path, language setting) is unusually prominent and easy to find — genuine operational tradecraft tends to be cleaner
- The artifact matches a well-known, heavily-documented actor signature that defenders would recognize immediately — sophisticated actors avoid fingerprints that are published in open-source threat intelligence
- Compilation timestamps, timezone metadata, or language pack indicators seem curated rather than incidental
- The malware contains *only* one strong attribution signal rather than the consistent cluster of overlapping TTPs that genuine actor re-use produces
- The canonical case: **Olympic Destroyer (2018)** — malware deployed against the Pyeongchang Winter Olympics was deliberately engineered to mimic Lazarus Group (DPRK) through code similarity and false flags. Kaspersky, Crowdstrike, and others initially attributed it to North Korea; the actual author was Sandworm (Russia). The lesson: a single high-salience attribution artifact should increase suspicion, not confidence.

If the deception flag is raised, recommend escalating to a full **Deception Detection** analysis (T21/§7.8) before using this item in any finished product.

---

## Step 8: Determine collection priorities

Based on the surviving alternatives (those consistent with the focal item), identify what additional evidence would be genuinely discriminating:

For each surviving alternative Hₙ, ask:
- What would I expect to see **if Hₙ were true but H₀ were false**?
- What would I expect to *not* see if Hₙ is the correct explanation?

This generates collection requirements: information that would actually discriminate between H₀ and the remaining alternatives.

---

## Step 9: Produce the output

### Required structure

**Header**: Focal Item | Date | Lead Hypothesis

**Section 1 — Focal Setup**
One-sentence statement of the focal item, lead hypothesis, and analyst's initial reaction.

**Section 2 — Alternatives Considered**
List of all hypotheses (H₀ through Hₙ) with brief descriptions.

**Section 3 — Diagnostic Matrix**
Table showing consistency scores (C / I / N) for each hypothesis against the focal item, with reasoning notes.

**Section 4 — Diagnostic Value Assessment**
The overall rating (🔴/🟡/🟢) with plain-language explanation of what the evidence does and does not establish.

**Section 5 — Deception Check**
Flag raised or clear, with reasoning.

**Section 6 — Collection Requirements**
What additional evidence would discriminate among surviving alternatives.

**Section 7 — Analyst Guidance**
Direct recommendation: Can this item legitimately update the assessment? Which alternatives remain alive? What should the analyst do next?

---

## Output format guidance

**Inline chat**: Markdown tables, concise — ideal for operational tempo when the analyst needs a fast check before acting on new reporting.

**Word (.docx)**: Use the `docx` skill. Formatted report suitable for formal products, peer review, or attachment to a finished intelligence item.

**HTML**: Standalone file with color-coded diagnostic matrix (green/yellow/red rows). Good for sharing or embedding in a working file.

---

## Cognitive biases this technique targets

Diagnostic Reasoning directly counters:

- **Confirmation Bias** — Seeking only information consistent with the lead hypothesis. DR forces explicit consideration of whether the same information is also consistent with alternatives.
- **Vividness Bias** — Focusing on one compelling scenario while ignoring others. DR requires generating a structured alternative set.
- **Satisficing** — Selecting the first "good enough" answer. DR requires testing the answer against rivals before accepting it.
- **Projecting Past Experiences** — Assuming the same dynamic is in play because it looks familiar. DR prompts: *is there a structurally different explanation?*
- **Rejecting Evidence** — Continuing to hold a judgment when contradicting evidence accumulates. DR surfaces whether the confirming evidence actually discriminates at all.
- **Ignoring Inconsistent Evidence** — Dismissing contrary information without analysis. DR integrates the alternative set and treats inconsistencies as informative.

---

## Relationship to other techniques

**Analysis of Competing Hypotheses (ACH)** — DR is the micro-scale version. Use DR for a single new item; escalate to ACH when multiple items of evidence need systematic evaluation across a full hypothesis matrix.

**Multiple Hypothesis Generation (MHG)** — If the alternatives generated in Step 4 require a more rigorous brainstorm (particularly for high-stakes or complex problems), run MHG first.

**Indicators Generation, Validation & Evaluation (IGVE)** — DR's collection requirements (Step 8) can feed directly into indicator development for ongoing monitoring.

**Deception Detection** — Escalate to the full MOM/POP/MOSES/EVE checklist whenever the deception flag is raised in Step 7.

**Key Assumptions Check (KAC)** — If the diagnostic test reveals that the focal item's consistency with H₀ depends on a buried assumption, run a KAC on that assumption.

---

## Analyst principles

**Consistency ≠ confirmation.** Evidence that is consistent with your hypothesis is not evidence *for* it unless it is simultaneously *inconsistent* with the alternatives. Make this distinction explicit every time.

**The absence of diagnostic evidence is itself diagnostic.** If a body of evidence is largely non-discriminating, that is important information: the analytic judgment rests on something other than evidence — likely assumptions or precedent. That is worth surfacing.

**Speed is not an excuse.** Diagnostic Reasoning takes minutes, not hours. There is no operational justification for skipping it when a new development is being used to update a significant assessment.

**When everything confirms the lead, suspect something.** Real-world intelligence is noisy and ambiguous. If incoming reporting consistently aligns perfectly with one explanation, ask why — it may be collection bias, source fabrication, or active deception.

**In CTI, a single attribution artifact is almost never diagnostic.** A code string, a mutex, a PDB path, a C2 IP — each of these is consistent with at least three alternative explanations (genuine actor reuse, commodity/leaked tooling, false flag). Rigorous attribution requires a *convergent cluster* of independent indicators, each checked individually through Diagnostic Reasoning, not a single vivid fingerprint. The analytic community's repeated false attributions of Olympic Destroyer, APT1/Comment Crew knock-offs, and Shadow Brokers-era tools demonstrate what happens when this discipline breaks down. The CTI analyst's phrase for this is "TTPs over IOCs" — behavioral patterns observable across multiple intrusions are harder to fabricate than individual artifacts and therefore far more diagnostic.
