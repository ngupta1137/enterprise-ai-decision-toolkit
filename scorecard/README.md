# Agentic AI Production Readiness Scorecard

A self-assessment for enterprise teams deciding whether an agentic AI system is ready to act in production, and how much authority it has actually earned.

[Read the scorecard](SCORECARD.md) · [Download the printable PDF](agentic-ai-production-readiness-scorecard.pdf) · [Back to the toolkit](../README.md)

---

## Why this exists

Most agentic AI systems that stall in production do not stall because the model is weak. They stall because nobody wrote down what the system is allowed to do, nobody can prove what it did, and nobody can take its authority back quickly when the evidence turns.

This scorecard turns that problem into 37 criteria that a team can score in one workshop. Every criterion asks for evidence, not intentions. Every anchor is written so that two reasonable people scoring the same team should land on the same number.

The organizing idea is simple: **capability is not authority.** An agent can pass every demo and still not be ready to change anything that matters.

## Who it is for

- VPs and Directors of AI deciding which agentic AI systems move from pilot to production
- Chief Data Officers and Chief AI Officers who own enterprise AI governance
- AI product leaders who need a shared language with risk, legal, security, and the business
- Risk, audit, and architecture teams reviewing an agentic AI system before launch or expansion

It works for agents you build, agents you buy, and agents assembled from both. If a vendor runs part of the system, score what your enterprise can show, not what the vendor says.

## What it covers

| # | Category | What it tests |
|---|---|---|
| 1 | Authorization and Decision Rights | What the agent may do, who decided, and how that changes |
| 2 | Data Governance | What it can read and write, and on what terms |
| 3 | Evaluation and Testing | How you know it is good enough, before and after launch |
| 4 | Observability and Audit | Whether you can prove what it did and why |
| 5 | Safety and Guardrails | Whether limits hold when the model surprises you |
| 6 | Reliability and Operations | Whether it can be run, recovered, and changed safely |
| 7 | Ownership and Accountability | Who answers for it, and how that stays current |

## How scoring works

- Each of the 37 criteria scores **0 to 3**, mapped to four maturity levels: **1 Ad hoc, 2 Developing, 3 Defined, 4 Managed**.
- Award the highest anchor where every condition is true. Anchors are cumulative.
- **No evidence, no points.** A claim nobody can show in the room scores 0.
- **Six criteria are gates** (written authority boundary, named authority owner, demotion triggers, complete action trace, tested kill switch, limits enforced outside the model). Gates cap the readiness band no matter how high the total is.
- Totals map to three bands: **Not ready (0 to 55), Pilot-ready (56 to 83), Production-ready (84 to 111)**, each with a maximum authority state and next steps.

Full rules are at the top of [SCORECARD.md](SCORECARD.md).

## Running it as a team workshop (60 to 90 minutes)

**Before the session (one week ahead)**

1. Pick one agentic AI system. One system per session; scoring a portfolio in one sitting produces averages nobody can act on.
2. Invite five to eight people: the authority owner if one exists, the business owner, the technical owner, someone from risk or compliance, someone from security, and one person who did not build the system.
3. Name a facilitator who is not on the build team, and a scribe.
4. Send the scorecard in advance and ask each owner to bring evidence for their areas: the authority document, log samples, test results, the kill switch test record.

**During the session**

| Time | Step |
|---|---|
| 0 to 10 min | Facilitator states the rules: score today's system, evidence or zero, lowest true anchor, disagreements go to the lower score and an action item. Confirm the system's scope and every action type it can take. |
| 10 to 20 min | Score the six gate criteria first. If any gate scores 0, say so out loud: the band is already capped at Not ready. Keep going anyway, because the rest of the score shows what to fix next. |
| 20 to 65 min | Work through the categories in order, about six minutes each. For each criterion, the relevant owner shows the evidence, the group agrees a score, the scribe records the score and the evidence location. Silent independent scoring followed by comparison works well for contested criteria. |
| 65 to 75 min | Total the score, apply the gate rules, and name the band and the maximum authority state it allows. Compare that to the authority the system actually holds today. A gap between the two is the most important finding of the session. |
| 75 to 90 min | Agree on the top five actions, each with an owner and a date. Prioritize gates scored 0 or 1, then any criterion blocking the next band. Set the re-score date. |

**After the session**

- Circulate the scored sheet, the evidence list, and the action list within two business days.
- If the system holds more authority than its band allows, the authority owner decides within one week whether to restrict it now or accept the gap in writing.
- Re-score at least quarterly, and every time the system's authority, model, market, or action types change.

## Tips from the field

- **Score the system, not the team.** A low score is a finding about controls, not a judgment about people.
- **Watch for "the vendor handles that."** Score what your enterprise can show. A vendor's assurance claim is not independent evidence.
- **The gap matters more than the total.** A Pilot-ready system holding bounded autonomy is a bigger problem than a Not ready system in observe mode.
- **Expect the first score to be low.** Most teams discover their first real gap at 1.2 (who actually holds the authority) or 5.1 (whether the kill switch has ever been tested).

## Cite this work

If you use or adapt this scorecard in research, internal standards, training material, or publications, please cite it:

> Gupta, N. (2026). *Agentic AI Production Readiness Scorecard* (Version 1.0) [Assessment framework]. In *Enterprise AI Decision Toolkit*. Zenodo. https://doi.org/10.5281/zenodo.23464328

BibTeX:

```bibtex
@misc{gupta2026scorecard,
  author       = {Gupta, Nitin},
  title        = {Agentic AI Production Readiness Scorecard},
  version      = {1.0},
  doi          = {10.5281/zenodo.23464328},
  year         = {2026},
  howpublished = {\url{https://github.com/ngupta1137/enterprise-ai-decision-toolkit/tree/main/scorecard}},
  note         = {Assessment framework for enterprise agentic AI governance}
}
```

The scorecard is part of the [Enterprise AI Decision Toolkit](../README.md) and is based on the authority framework in *The Enterprise AI Decision System: How AI Leaders Turn Capability into Authorized Enterprise Action* by Nitin Gupta.

## Contributing

Practitioner feedback makes this better. The most useful contributions are:

- A criterion that two people scored differently, with the reason, so the anchor can be tightened
- A failure mode you have seen in production that no criterion catches
- Evidence that an anchor threshold is wrong for a specific industry or risk level

Open an issue before proposing large changes. See [CONTRIBUTING.md](../CONTRIBUTING.md) for details.

## What this is not

This is not a certification, a legal opinion, or a compliance program. It is a structured, evidence-based conversation about whether an agentic AI system has earned the authority it holds. It draws on concepts from the NIST AI Risk Management Framework, ISO/IEC 42001, and the EU AI Act's human-oversight provisions, and is not affiliated with or endorsed by any of them.

## License

[MIT](../LICENSE). Use it, adapt it, share it. Attribution is appreciated.
