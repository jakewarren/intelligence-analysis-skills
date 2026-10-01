# Intelligence Analysis Skills

A collection of 18 reusable [Agent Skills](https://agentskills.io/) for structured intelligence analysis, with a particular focus on cyber threat intelligence (CTI).

The collection turns established Structured Analytic Techniques (SATs) into guided workflows that help analysts explore problems, test hypotheses, challenge assumptions, anticipate futures, and support decisions.

## Install

Install the collection interactively:

```sh
npx skills add jakewarren/intelligence-analysis-skills
```

Preview the available skills without installing them:

```sh
npx skills add jakewarren/intelligence-analysis-skills --list
```

After installation, ask your agent for a technique by name (for example, "run an ACH") or describe the analytic problem and let the skill's trigger description route the request.

## Skills

| Category | Skill | Use it to |
| --- | --- | --- |
| Planning | [Structured Analytic Techniques](structured-analytic-techniques/SKILL.md) | Select and sequence the right techniques for an analytic problem. |
| Exploration | [Circleboarding](circleboarding/SKILL.md) | Build a comprehensive Who, What, How, When, Where, Why, and So What picture. |
| Cause and effect | [Outside-In Thinking](outside-in-thinking/SKILL.md) | Scan external forces with STEMPLES+. |
| Diagnostic | [Multiple Hypothesis Generation](multiple-hypothesis-generation/SKILL.md) | Generate a broad, non-redundant set of explanations. |
| Diagnostic | [Analysis of Competing Hypotheses](analysis-of-competing-hypotheses/SKILL.md) | Compare explanations by testing evidence for inconsistency. |
| Diagnostic | [Diagnostic Reasoning](diagnostic-reasoning/SKILL.md) | Determine whether new evidence truly discriminates among hypotheses. |
| Diagnostic | [Deception Detection](deception-detection/SKILL.md) | Assess deception risk with MOM, POP, MOSES, and EVE. |
| Diagnostic | [Key Assumptions Check](key-assumptions-check/SKILL.md) | Surface and stress-test the assumptions beneath an assessment. |
| Diagnostic | [Argument Mapping](argument-mapping/SKILL.md) | Map support, objections, and rebuttals for a conclusion. |
| Reframing | [Premortem Analysis](premortem-analysis/SKILL.md) | Work backward from analytic failure and conduct a structured self-critique. |
| Reframing | [Red Hat Analysis](red-hat-analysis/SKILL.md) | Model decisions from an adversary's perspective. |
| Reframing | [What If? Analysis](what-if-analysis/SKILL.md) | Challenge a prevailing view with a surprising alternative. |
| Reframing | [High Impact/Low Probability](high-impact-low-probability/SKILL.md) | Examine a plausible pathway to a severe tail-risk outcome. |
| Foresight | [Key Drivers Generation](key-drivers-generation/SKILL.md) | Identify the forces and uncertainties that shape future outcomes. |
| Foresight | [Cone of Plausibility](cone-of-plausibility/SKILL.md) | Bound plausible futures around a baseline and fragile assumptions. |
| Foresight | [Alternative Futures Analysis](alternative-futures-analysis/SKILL.md) | Build four scenarios from two drivers, or use MSG for larger driver sets. |
| Decision support | [Bowtie Analysis](bowtie-analysis/SKILL.md) | Map causes, consequences, controls, and escalation factors around an event. |
| Decision support | [SWOT Analysis](swot-analysis/SKILL.md) | Turn a SWOT assessment into actionable TOWS strategies. |

## Source and scope

The techniques are based primarily on:

> Pherson, Randolph H., and Richards J. Heuer Jr. *Structured Analytic Techniques for Intelligence Analysis*. 3rd ed., CQ Press, 2021.

These independent skill implementations emphasize practical use in intelligence and CTI workflows. They are not a substitute for the source text, source validation, domain expertise, or analyst judgment. References to named techniques and trademarks belong to their respective owners.
