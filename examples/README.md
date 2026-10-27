# Worked Example: One System Through the Toolkit

**A fictional invoice-matching agent, followed from funding to its third authority decision**

[Back to the toolkit](../README.md) · [Example scorecard workbook](invoice-matching-agent-scorecard.xlsx)

Templates are easy to start and hard to finish. This example shows what finished looks like. It follows one system through every instrument in the toolkit, in the order a real enterprise would use them, so you can see how the evidence from one instrument becomes the input to the next.

**Everything here is fictional.** The company, the people, the dates, and every figure are invented to show the reasoning. None of it is a benchmark, and none of it describes a real deployment.

---

## The system

An accounts payable team in a mid-sized company matches about 6,000 supplier invoices a month against purchase orders and goods receipts. A clerk checks each three-way match and approves it for payment. The manual cost, measured over a quarter, is $2.10 per invoice.

The team builds an agent that reads each invoice, finds the purchase order and goods receipt, and decides whether the three agree closely enough to approve. It runs in one country, called Market A here, on one instance of the finance system.

| | |
|---|---|
| Decision supported | Whether a supplier invoice matches its purchase order and goods receipt closely enough to be approved for payment |
| Accountable decision owner | The accounts payable controller |
| Business owner | The finance operations director |
| Technical owner | The accounts payable platform lead |
| Risk owner | The head of financial controls |

## The timeline at a glance

| When | Instrument | What was decided |
|---|---|---|
| January | [Stop Memo](../stop-memo/), part one | Four stop lines written and signed before work began |
| January | [Agent Register](../agent-register/), [Authority Change Record](../authority-change-record/) AP-001 | Registered and launched at Recommend |
| March | [Readiness Scorecard](../scorecard/), [True Cost of an Action](../true-cost-of-an-action/) | Pilot-ready, 68 of 111. True cost $0.40 per accepted match |
| April | [AI Authority Review](../ai-authority-review/), change record AP-002 | Asked for Bounded autonomy. Granted Act with approval, one state up |
| June | Scorecard and True Cost, again | Production-ready, 84 of 111. True cost at production volume $0.55 |
| July | Authority Review, change record AP-003 | Bounded autonomy for exact matches under $5,000, with a 90-day sunset |
| August | Change record AP-004 | Suspended to Act with approval the same day a demotion trigger fired |
| September | Change record AP-005, Stop Memo part two | Restored on evidence gathered after the fix. Continue |
| October | [Market Authority Passport](../market-authority-passport/) | Market B visa issued at Act with approval |

---

## 1. Funding: the Stop Line (January)

The stop conditions were written and signed before any money was spent, while nobody had anything to defend.

| Line | Written condition |
|---|---|
| Value | Average time from invoice receipt to approval below 3 days, from a baseline of 6, by 30 June, on all invoices in scope |
| Cost | True cost per accepted match no higher than $1.00 at production volume |
| Risk | Zero duplicate payments. Reversed approvals below 0.5 percent a month. Agreement with weekly clerk sampling not below 97 percent after two rounds of retuning |
| Adoption | At least 80 percent of eligible invoices routed through the agent by 31 May |

Signed by the accountable decision owner, the business owner, a finance partner, and the risk owner. Reviews set for the end of each quarter.

## 2. Go-live: the Scope Card, the register entry, and the first change record (January)

**Scope Card, abbreviated.**

| Field | Entry |
|---|---|
| Agent ID | AP-01 |
| Tier | Acting |
| Non-human identity | A dedicated service account, read and write separated |
| Systems it may read | Invoices, purchase orders, goods receipts, the supplier master |
| Systems it may write to | The approval flag on invoices in the accounts payable module, nothing else |
| Limits | Invoices under $5,000. No more than 300 flags an hour or $250,000 a day |
| May never touch | Supplier bank details, the supplier master itself, payment runs, credit notes, and any invoice from a supplier added in the last 30 days |
| Decisions it may prepare | A match decision with the reason, for a clerk |
| Decisions it may make | None at launch |
| Agents and tools it may call | None. Technically prevented from calling other agents |
| Stop button | Disable the service account's write permission from the identity console. Three named people may do it, one outside business hours |

**Change record AP-001.** Type Promote, from nothing to Recommend, for one action type: flag a match for clerk approval. The thresholds for the next step were written into the record on day one: agreement with clerks of at least 98 percent on at least 1,000 invoices, and no duplicate-payment risk found in testing. Writing the bar before the results are in is what makes the later decision honest.

## 3. First evidence: the Scorecard and the true cost (March)

**Scorecard.** Scored in a 90-minute workshop led by an internal audit lead who had not built the system. The full scored sheet, with the evidence and actions for every criterion, is in [invoice-matching-agent-scorecard.xlsx](invoice-matching-agent-scorecard.xlsx).

| Category | Score | Max |
|---|---|---|
| 1. Authorization and Decision Rights | 13 | 18 |
| 2. Data Governance | 9 | 15 |
| 3. Evaluation and Testing | 9 | 15 |
| 4. Observability and Audit | 9 | 15 |
| 5. Safety and Guardrails | 9 | 15 |
| 6. Reliability and Operations | 7 | 15 |
| 7. Ownership and Accountability | 12 | 18 |
| **Total** | **68** | **111** |

Gates: 1.1 at 2, 1.2 at 2, 1.5 at 2, 4.1 at 2, **5.1 at 1**, 5.2 at 2. The kill switch existed but had never been tested. Band: **Pilot-ready**, which allows Recommend, or Act with approval in a limited scope. The system held Recommend, so there was no gap.

**True cost, March (pilot).**

| Figure | Calculation | Result |
|---|---|---|
| Attempted matches | | 1,450 |
| Accepted, completed matches | Not reversed within 14 days | 1,400 |
| Six layers | Run $60, Reach $40, Review $210, Repair $50, Assure $120, Share $80 | $560 |
| True cost per accepted match | $560 ÷ 1,400 | $0.40 |
| Action yield | 1,400 ÷ 1,450 | 97% |
| Margin against the $2.10 baseline | $2.10 − $0.40 | $1.70 |

Every match was reviewed by a clerk at this stage, so Review is the largest layer. Assure and Share were low because a central team was absorbing most of the monitoring and platform cost. The team noted that both would rise at production volume.

## 4. The first authority decision (April)

The team asked to skip a state, from Recommend straight to Bounded autonomy for exact matches under $5,000. The [AI Authority Review](../ai-authority-review/) recorded the following.

| Field | Entry |
|---|---|
| The ten-times question | Ten wrong approvals under $5,000 means up to $50,000 paid to suppliers in error, recoverable but slow, and a supplier relationship to repair each time. Not catastrophic. Not an afternoon of cleanup either. |
| Evidence Chain | Strong: capability (99 percent agreement on 4,200 invoices over 90 days), decision quality, workflow adoption, economic value. Partial: outcome (cycle time down, early-payment discounts not yet measured), human trust. Weak: risk (duplicate-payment scenario never tested), operational readiness (kill switch never tested). |
| Demotion trigger | Any duplicate payment, or agreement with weekly clerk sampling below 98 percent |
| Cost boundary | $0.40 at pilot volume against $2.10. Recalculate at production volume before the next review |
| Market boundary | Market A, one finance instance |
| Control-plane ownership | Matching rules and limits held in the enterprise's own configuration. The model can be replaced |
| Exit condition | The risk line in the Stop Memo |
| Decision | **Expand by one state only:** Act with approval for invoices under $5,000, reviewed at 60 days. Bounded autonomy refused until the kill switch and the duplicate-payment scenario have both been tested |

**Change record AP-002.** Type Promote, Recommend to Act with approval. Section D, controls confirmed, could not be completed on the day: the record requires a kill switch tested within 90 days, and it had never been tested. The change took effect two weeks later, the day after the first test stopped all write actions in 11 minutes. A signed record changes nothing until the controls behind it are real.

## 5. Production evidence (June)

Over May and June the team built an adversarial test suite that included the duplicate-payment scenario, defined and tested duplicate-action handling in the finance integration, set a quality alert, mapped every data flow, wrote an AI-specific incident playbook, ran a demotion drill, and agreed latency and quality targets with the business owner.

**Scorecard re-scored: 84 of 111, Production-ready.** Every gate at 2 or higher, no criterion at 0. The criteria that moved: 1.4, 1.5, 2.5, 3.3, 3.4, 3.5, 4.1, 4.3, 4.4, 5.1, 5.3, 6.1, 6.4, 6.5, 7.4, and 7.5, each by one point.

**True cost, June (production volume).**

| Figure | Calculation | Result |
|---|---|---|
| Attempted matches | | 5,200 |
| Accepted, completed matches | | 5,000 |
| Six layers | Run $260, Reach $150, Review $750, Repair $240, Assure $600, Share $750 | $2,750 |
| True cost per accepted match | $2,750 ÷ 5,000 | $0.55 |
| Action yield | 5,000 ÷ 5,200 | 96% |
| Margin against the $2.10 baseline | $2.10 − $0.55 | $1.55 |
| Break-even review rate | ($2.10 − $0.40 non-review cost) ÷ $0.15 review cost per reviewed match | Above 100% |

The true cost rose by more than a third from pilot to production, as Assure and Share moved from a central budget onto the system. It stayed well inside the $1.00 cost line. The break-even review rate is above 100 percent, which means human review is cheap enough here that it will never be what makes this system uneconomic. For this system, quality and risk decide the authority question, not cost.

## 6. The second authority decision (July)

With the risk and operational readiness gaps closed, the Authority Review granted **Bounded autonomy for invoices under $5,000 with an exact three-way match.** Anything that is not an exact match, or is $5,000 or more, still goes to a clerk.

**Change record AP-003.** Type Promote, Act with approval to Bounded autonomy, for the exact-match action type only. Sunset in 90 days. If fresh evidence does not renew it by then, authority reverts one state, to Act with approval. Section D confirmed: limits enforced in the finance integration, kill switch tested within 90 days, demotion triggers wired to an alert, inventory updated.

## 7. The demotion trigger fires (August)

A supplier master data migration changed the identifiers on about 400 suppliers. Matches against those suppliers started failing in a way the model did not recognize as a failure. Weekly clerk sampling of autonomous approvals fell to **97.6 percent**, below the 98 percent trigger. No duplicate payment occurred.

**Change record AP-004.** Type Suspend, Bounded autonomy to Act with approval, for all invoices. Signed by the accounts payable controller alone, within two hours of the alert, as the record allows for suspensions. The technical owner confirmed the change in the integration the same afternoon, and the 63 approvals made since the migration were re-checked by clerks. The rest of the record was completed within five business days. Speed is allowed in the downward direction.

The Stop Line was not crossed. Agreement never fell below 97 percent and no retuning was needed. This is the distinction the toolkit draws on purpose: a demotion trigger protects the enterprise from the system's current authority, and a stop line protects the enterprise's money. One fired. The other did not.

## 8. Restore and review (September)

**Root cause and fix.** The supplier identifier mapping was corrected on 19 August, and supplier master changes were added to the regression suite, so the next migration is tested before it reaches production.

**Change record AP-005.** Type Restore, Act with approval to Bounded autonomy, exact matches under $5,000. The evidence period started the day after the fix, never before it: four weeks, 3,900 invoices at Act with approval, weekly sampling at 99.2 percent, clerk agreement 99.3 percent. New 90-day sunset. The earlier sunset on AP-003 no longer applies.

**Stop Memo, part two, Q3 review.**

| Line | Written condition | Evidence | Crossed? |
|---|---|---|---|
| Value | Cycle time below 3 days by 30 June | 2.4 days | No |
| Cost | No higher than $1.00 per accepted match | $0.55 | No |
| Risk | Zero duplicate payments, reversals below 0.5 percent, agreement not below 97 percent after two retunings | None, 0.2 percent, lowest weekly sample 97.6 percent | No |
| Adoption | 80 percent of eligible invoices by 31 May | 86 percent | No |

No line crossed. Outcome: **Continue.** Next review at the end of the fourth quarter.

## 9. A second market (October)

The finance team in Market B asked for the same agent. The [Market Authority Passport](../market-authority-passport/) review found:

| Dimension | Rating | Why |
|---|---|---|
| Regulatory | Transfers with conditions | Electronic invoicing is mandatory in Market B. Local finance confirms the agent reads the mandated format |
| Data | Transfers with conditions | Same platform region; invoice archive retention is longer under local rules |
| Language | Re-earn | Invoices arrive in a language the evaluation set never covered |
| Cultural | Transfers | Approval practice is the same |
| Action | Transfers | Same action, same finance system |
| Control | Transfers | Same kill switch and limits, confirmed deployed for Market B |
| Outcome | Re-earn | No evidence yet on Market B suppliers or invoice quality |

Language rated Re-earn caps entry at Act with approval. Outcome rated Re-earn caps it one state below home. Both point to the same entry state. **Visa: Act with approval for invoices under $2,000,** with a local evaluation set of 300 Market B invoices, a first review no later than 90 days after entry, and a local authority owner, the Market B finance controller, who can restrict or revoke on their own.

The same agent now runs at two levels of trust: Bounded autonomy in Market A and Act with approval in Market B. That is not inconsistency. It is the evidence, market by market.

---

## The register entry today

| Field | Entry |
|---|---|
| Agent ID | AP-01 |
| Highest authority state | Bounded autonomy (Market A). Act with approval (Market B) |
| Stop button last tested | 2 October |
| Latest Authority Change Record | AP-005, plus the Market B visa |
| Authority sunset | 21 December (Market A) |
| Scorecard band and date | Production-ready, 84 of 111, June. Re-score due before the December renewal |
| Reconciliation status | Matched |

## What the example shows

- **The evidence supported one state at a time.** The team asked for two steps in April and earned one. The gap was in risk and operational readiness, the two dimensions a pilot is least likely to test.
- **Controls gate the effective date, not the meeting.** The April promotion waited two weeks for a kill switch test. The record, not the decision, made the change real.
- **Pilot economics flattered the system.** True cost rose from $0.40 to $0.55 at production volume and stayed inside the line, but only because the line was written for production volume from the start.
- **Demotion was fast and ordinary.** The suspension took two hours and needed one signature. Restoration took a month and needed new evidence. That asymmetry is the design.
- **Trust is local.** One agent, two markets, two authority states, each backed by its own evidence.

---

Part of the Enterprise AI Decision Toolkit, a set of open instruments for enterprise AI governance based on *The Enterprise AI Decision System: How AI Leaders Turn Capability into Authorized Enterprise Action* by Nitin Gupta. Latest version: github.com/ngupta1137/enterprise-ai-decision-toolkit. Licensed under MIT.
