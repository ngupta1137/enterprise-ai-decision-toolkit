# Enterprise AI Decision Toolkit

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23464328.svg)](https://doi.org/10.5281/zenodo.23464328)

**Eight open instruments for deciding what an enterprise AI system is allowed to do, and proving it.**

Most enterprise AI does not fail because the model is weak. It fails in the space around the model: nobody wrote down what the system may do, nobody can show what it did, the vendor holds the controls, the business case counted the cheapest number, the rollout to a second country assumed the first one's evidence, and nobody was willing to sign the decision to stop.

Each instrument in this toolkit addresses one of those gaps. None of them needs software. Each one is a document a leadership team can fill in, sign, and keep.

The organizing idea behind all eight is the same: **capability is not authority.** A system can be very good at something and still not have earned the right to do it on the enterprise's behalf.

---

## Start here

Pick the row that matches the decision in front of you.

| If you need to... | Use | Time |
|---|---|---|
| Know which AI agents the enterprise is running, and who can stop each one | [Agent Register](agent-register/) | One reconciliation sweep, then quarterly |
| Fund a new AI initiative | [Stop Memo](stop-memo/) part one, and [True Cost of an Action](true-cost-of-an-action/) | 30 minutes, plus the cost model |
| Choose or renew an AI vendor | [Vendor Authority Gates](vendor-authority-gates/) | One session per vendor |
| Decide whether a system is ready to act in production | [Readiness Scorecard](scorecard/), with the [scoring workbook](scorecard/scorecard-workbook.xlsx) | 60 to 90 minutes |
| Decide whether to give a system more authority, or take some back | [AI Authority Review](ai-authority-review/) | 45 to 60 minutes |
| Record a change in what a system may do | [Authority Change Record](authority-change-record/) | 20 to 30 minutes |
| Switch a system on in a new country or regulatory regime | [Market Authority Passport](market-authority-passport/) | 60 minutes |
| Decide whether an initiative should continue | [Stop Memo](stop-memo/) part two | 20 to 40 minutes |

New to the toolkit? Read the [worked example](examples/), which follows one fictional system through every instrument, from funding to its third authority decision.

## The instruments

| Instrument | The question it answers | Use it when |
|---|---|---|
| [Agent Register](agent-register/) | Which agents can act, who owns each one, and can we stop them? | Before any agent receives credentials, and in a quarterly reconciliation |
| [Agentic AI Production Readiness Scorecard](scorecard/) | Has this system earned the authority it holds? | Before launch, before any expansion of authority, and quarterly after that |
| [AI Authority Review](ai-authority-review/) | Should this system's authority expand, stay, or contract? | Before every change in authority, and at every scheduled review |
| [Authority Change Record](authority-change-record/) | What changed in what this system may do, who decided, and on what evidence? | Every promotion, constraint, suspension, revocation, or restoration |
| [Vendor Authority Gates](vendor-authority-gates/) | Will buying this keep the enterprise in control of its own decisions? | Vendor selection, proof of concept, contract, and renewal |
| [Market Authority Passport](market-authority-passport/) | How much of the home-market evidence holds in a new market? | Before switching on an AI system in a new country, language, or regulatory regime |
| [True Cost of an Action](true-cost-of-an-action/) | What does one accepted, completed action really cost? | Business case, pilot exit, and every quarterly value review |
| [Stop Memo](stop-memo/) | When do we stop, and how do we stop cleanly? | Written at funding, used at every scheduled review |

Each folder holds the instrument as a readable page and a printable PDF. The Scorecard also comes as a [spreadsheet](scorecard/scorecard-workbook.xlsx) that applies the gate and band rules automatically, and the AI Authority Review as a [one-page form](ai-authority-review/ai-authority-review-form.pdf).

## How they fit together

The eight follow the life of an AI system in the enterprise.

1. **Funding.** Write the **Stop Memo**'s stop line before the start date, while nobody is yet invested in the outcome. Build the business case on the **True Cost of an Action**, not on the price of a model call.
2. **Buying.** If any part of the system is bought, run **Vendor Authority Gates** before weighted scoring begins.
3. **Launching.** Complete the **Agent Register** scope card: a scope, an owner, and a stop button, before any credential is issued. Score the system on the **Readiness Scorecard**. The band sets the most authority it may hold. Record the grant on an **Authority Change Record**, with an expiry date.
4. **Operating.** Re-score quarterly. Every request for more authority, and every scheduled review, goes through the **AI Authority Review**. Every change in authority, up or down, goes on the same change record. Recalculate the true cost each quarter. Reconcile the register against what is actually running.
5. **Expanding.** Before entering a new market, issue a **Market Authority Passport**. Every new market starts one step down.
6. **Reviewing.** At each scheduled review, complete the stop decision against the stop line written at funding: continue, redesign, park, or stop. If the answer is stop, unwind the system's authority as well as its budget.

The instruments share one vocabulary for authority, so a score on one carries straight into another. Every instrument uses the same five authority states:

| State | What the system may do |
|---|---|
| Observe | Watch and report. No output reaches a decision. |
| Recommend | Suggest. A person decides and acts. |
| Act with approval | Prepare the action. A person approves each one before it happens. |
| Bounded autonomy | Act alone inside written limits, with every action traced and reversible where possible. |
| Expanded autonomy | Act alone across a wider scope, earned by sustained evidence at the bounded level. |

## Running them as workshops

Every instrument is designed to be completed in a working session with the people who own the decision, not filled in by one person at a desk.

- **Agent Register:** one reconciliation sweep with identity and access, then quarterly. Each scope card takes 30 minutes with the owners.
- **Scorecard:** 60 to 90 minutes, one system per session. The full facilitator guide is in [scorecard/](scorecard/).
- **AI Authority Review:** 45 to 60 minutes with the accountable decision owner. The facilitator guide, including the ten-times question, is in [ai-authority-review/](ai-authority-review/).
- **Authority Change Record:** 20 to 30 minutes per change. Suspensions can be signed immediately and reviewed afterwards. Upward changes are never fast-tracked.
- **Vendor Authority Gates:** one session per vendor for the Five Keeps, before any weighted scoring.
- **Market Authority Passport:** 60 minutes with the global owner and the local owner in the same room.
- **True Cost of an Action:** one month of operating data and someone from finance.
- **Stop Memo:** 30 minutes at funding to write the stop line; 20 to 40 minutes at each review, with the evidence prepared in advance.

Bring evidence. In every instrument, a claim nobody can show in the room counts as no evidence.

## Where these come from

These instruments apply and extend the authority framework in *The Enterprise AI Decision System: How AI Leaders Turn Capability into Authorized Enterprise Action* by Nitin Gupta, drawn from more than fifteen years of building and delivering enterprise AI systems at global scale.

They are not invented from nothing, and they say so. Each instrument names the established ideas it builds on, such as stage-gate reviews, zero-based budgeting, change control, and total cost of ownership. What is new is the application to AI authority and the specific mechanisms each one uses.

They draw on concepts from the NIST AI Risk Management Framework, ISO/IEC 42001, and the EU AI Act, and are not affiliated with or endorsed by any of them. Nothing here is a certification, a legal opinion, or a compliance program.

## Cite this work

To cite the toolkit as a whole:

> Gupta, N. (2026). *Enterprise AI Decision Toolkit* (Version 1.1) [Governance instruments]. Zenodo. https://doi.org/10.5281/zenodo.23464328

```bibtex
@misc{gupta2026toolkit,
  author       = {Gupta, Nitin},
  title        = {Enterprise AI Decision Toolkit},
  version      = {1.1},
  doi          = {10.5281/zenodo.23464328},
  year         = {2026},
  howpublished = {\url{https://doi.org/10.5281/zenodo.23464328}},
  note         = {Open instruments for enterprise AI authority, governance, and value}
}
```

To cite a single instrument, use its name as the title and its folder URL, for example `https://github.com/ngupta1137/enterprise-ai-decision-toolkit/tree/main/stop-memo`. A [CITATION.cff](CITATION.cff) file is included so GitHub can generate the citation for you.

## Contributing

The most useful contributions come from people who have used an instrument for real: a criterion two people read differently, a failure no instrument would have caught, a threshold that is wrong for a particular industry. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Versions

| Version | Date | Change |
|---|---|---|
| 1.1 | October 2026 | Added the AI Authority Review and the Agent Register. Added the Expanded-ready band to the Scorecard (Scorecard 1.1), a scoring workbook, a one-page Authority Review form, and a worked example. See [CHANGELOG.md](CHANGELOG.md) |
| 1.0 | October 2026 | First public release of six instruments |

## License

[MIT](LICENSE). Use them, adapt them, put them in your own standards and training. Attribution is appreciated.
