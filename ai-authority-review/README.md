# The AI Authority Review

**Deciding whether an AI initiative has earned the authority it holds, or the authority it is asking for**

**Version 1.0 · October 2026 · Nitin Gupta**

[Printable form, one page](ai-authority-review-form.pdf) · [Full instrument as PDF](ai-authority-review.pdf) · [Back to the toolkit](../README.md)

Most governance forums are built to approve things. A team brings a request for more authority, the meeting discusses the technology, someone asks about risk, and the request goes through because nobody can point to a specific reason to refuse it. Requests to reduce authority rarely arrive at all.

The AI Authority Review is the decision meeting the rest of the toolkit feeds. The [Readiness Scorecard](../scorecard/) measures the controls. The [True Cost of an Action](../true-cost-of-an-action/) measures the economics. The [Market Authority Passport](../market-authority-passport/) measures what travels. This review puts that evidence in front of one accountable person, asks twelve questions that each catch a different way an AI system ends up with more authority than it has earned, and records a decision. The [Authority Change Record](../authority-change-record/) then makes the decision real.

It works in both directions. The same twelve questions decide whether to expand authority, keep it, or take it back.

Three principles sit underneath it:

1. **A blank field is a finding.** An unanswered question is a governance gap, not a formatting problem. Do not fill a field with an assumption to make the form look complete.
2. **Review for demotion as deliberately as for promotion.** An initiative that is only ever checked for expansion is not being governed. It is being watched.
3. **Expand by evidence, one state at a time.** The evidence decides how far authority moves. A request for two steps up usually earns one, and the review should say exactly which evidence would earn the next.

---

## The form

*Complete before any change in authority, at every scheduled review, and whenever the evidence changes. The blank form fits on one page: [ai-authority-review-form.pdf](ai-authority-review-form.pdf).*

| Field | Answer |
|---|---|
| Initiative | |
| Business owner | |
| Review date | |
| Current authority | Observe / Recommend / Act with approval / Bounded autonomy / Expanded autonomy |
| Requested authority | State, action types, and limits |

### A. Decision and authority

| # | Question | Answer and evidence |
|-|----------------------------|--------------------|
| 1 | **Business decision.** What recurring decision or state change does this system participate in? Name the decision, not the technology. | |
| 2 | **Authority sought.** What is the current state and the requested state, for each action type separately? | |
| 3 | **Accountable decision owner.** Who has the D: the right to approve, expand, restrict, or revoke this system's authority? One name. | |

### B. Ownership and control

| # | Question | Answer and evidence |
|-|----------------------------|--------------------|
| 4 | **Business owner.** Who owns the outcome and the economics this system moves? | |
| 5 | **Technical owner.** Who operates the system and owns its recovery path? | |
| 6 | **Risk owner and control functions.** Who accepts the residual risk of this authority? Which privacy, security, legal, or risk functions hold a mandatory approval or veto, and what did each decide, on what date? | |

The authority owner cannot grant what a control function has blocked. Record each control function's decision and date here before the review reaches a decision.

### C. Evidence

**7. Evidence supporting this request.** Rate each dimension of the Evidence Chain on what can be shown, not on what is assumed.

| Dimension | The question | Evidence | Strength (Strong / Partial / Weak / None) | Gap |
|--------|------------|------------|------|--------|
| Capability | Can the system do the task, on the enterprise's own cases? | | | |
| Decision quality | Are the decisions it supports better than the current way? | | | |
| Workflow adoption | Do people use it in the real workflow, as designed? | | | |
| Human trust | Do reviewers trust it the right amount: still checking, not rubber-stamping? | | | |
| Outcome | Has the business result it was funded to move moved? | | | |
| Economic value | Is the true cost per accepted action below the value it creates? | | | |
| Risk | Have the ways it could cause harm been tested, not only listed? | | | |
| Operational readiness | Can it be monitored, stopped, recovered, and rolled back today? | | | |

A strong case on seven dimensions does not cover a real gap in the eighth. Risk and operational readiness are the two a pilot is least likely to have tested, so look there first.

### D. Boundaries and reversibility

| # | Question | Answer and evidence |
|-|----------------------------|--------------------|
| 8 | **Demotion trigger.** What specific evidence would justify reducing this system's authority, and who acts on it? | |
| 9 | **Cost boundary.** What is the fully loaded cost per accepted, completed action at production volume, not pilot scale, against what baseline? | |
| 10 | **Market boundary.** Where has this authority been earned, and where would it need requalification? | |
| 11 | **Control-plane ownership.** If the vendor or model changed tomorrow, could the enterprise keep its policy, its authority boundaries, and its evaluation criteria? If not, what does it own? | |
| 12 | **Exit condition.** What evidence would trigger redesign, pause, or exit, as the system working as intended rather than as a failure? | |

### Authority decision

| Field | Entry |
|---|---|
| Current authority | |
| Decided authority | State, action types, and limits |
| Decision | Expand / Maintain / Constrain / Pause / Redesign / Exit |
| Rationale | Which evidence decided it, in two or three sentences |
| Conditions for the next authority level | The specific evidence that would earn the next state |
| Accountable decision owner | |
| Effective date | Not before the Authority Change Record confirms the controls |
| Next review date | |

---

## Running the review (45 to 60 minutes)

**Before the session**

- Circulate the latest Scorecard result, the True Cost figures, the Stop Line, and any Market Authority Passports at least three business days ahead.
- The team requesting the change completes sections A to D in writing. A field the team cannot answer is left blank and marked, not filled in during the meeting.
- Ask each control function in question 6 for its decision in writing before the session, not during it.

**In the room**

The accountable decision owner, the business owner, the technical owner, the risk owner, and a facilitator who did not build the system. Others attend only to present evidence.

| Time | Step |
|---|---|
| 0 to 5 min | The facilitator states the request in one sentence: this system, this action type, from this state to that state, with these limits. Anything outside that sentence is out of scope. |
| 5 to 10 min | **The ten-times question.** Before any evidence is shown, ask: what happens if this system is wrong ten times in a row, not once? If the answer is an afternoon of cleanup, wide authority is plausible. If the answer is ten payments sent, ten customers contacted, or ten orders placed before anyone looks, the request needs a limit, an alert, or a person in front of it, whatever the evidence says. |
| 10 to 30 min | Walk the Evidence Chain, weakest dimension first. Rate each one on what is shown in the room. Strength is the evidence, not the confidence of the presenter. |
| 30 to 40 min | Walk the boundaries. Questions 8 and 12 together tell you whether the enterprise can take this authority back. If either is blank, the request is not ready. |
| 40 to 50 min | The accountable decision owner decides, out loud, and states which evidence decided it. If the decision is less than the request, name the evidence that would earn the rest. |
| 50 to 60 min | Record conditions, the next review date, and who raises the Authority Change Record. |

**After the session**

- Raise the [Authority Change Record](../authority-change-record/) within two business days. The decision takes effect when the record confirms the controls, not when the meeting ends.
- If the decision is Pause, Redesign, or Exit, complete the [Stop Memo](../stop-memo/) Stop Decision at the same time.
- File the completed review with the change record. Together they are the audit trail: the review shows why, the record shows what changed.

## Reading the result

| Pattern in the review | What it usually means |
|---|---|
| Strong capability, weak risk and operational readiness | A successful pilot that has not yet been tested for the ways it could fail. Expand one state at most. |
| Strong evidence, blank question 3 | Nobody holds the authority. Fix ownership before deciding anything else. |
| Human trust rated strong because approval rates are near 100 percent | Possibly the opposite. Check whether reviewers are still reviewing (Scorecard 4.4). |
| Cost boundary measured at pilot volume only | Recalculate at production volume. Pilot economics almost always flatter the system. |
| Question 11 answered "the vendor handles it" | The enterprise does not own its control plane. See [Vendor Authority Gates](../vendor-authority-gates/). |
| Every review in the log ends in Expand | The forum approves. It does not govern. |

## A completed example

The review below is for a fictional system, described generically so the reasoning is visible. The figures are illustrative, not benchmarks. The same system is followed through every instrument in [examples/](../examples/).

| Field | Entry |
|---|---|
| Initiative | Invoice-matching agent in an accounts payable team |
| Business decision | Whether a supplier invoice matches its purchase order and goods receipt closely enough to be approved for payment |
| Current authority | Recommend. The agent flags matches and a clerk approves each one. |
| Requested authority | Bounded autonomy for invoices under $5,000 with an exact three-way match |
| Accountable decision owner | The accounts payable controller |
| Evidence Chain | Strong: capability (agreed with clerks on 99 percent of 4,200 invoices over 90 days), decision quality, workflow adoption, economic value. Partial: outcome (payment cycle shorter, early-payment discount capture not yet measured), human trust. Weak: risk (duplicate-payment scenario never tested), operational readiness (kill switch never tested). |
| Demotion trigger | Any duplicate payment, or agreement with weekly clerk sampling below 98 percent |
| Cost boundary | True cost of $0.40 per accepted match against a measured manual baseline of $2.10 |
| Market boundary | One country and one finance system instance only |
| Control-plane ownership | Matching rules and limits held in the enterprise's own configuration. The model can be replaced. |
| Exit condition | Stop if agreement stays below 97 percent after two rounds of retuning |
| Decision | Expand by one state only: Act with approval for invoices under $5,000, reviewed at 60 days. Bounded autonomy is refused until the kill switch and the duplicate-payment scenario have both been tested. |

The team asked for two steps up. The evidence supported one. The gaps sat in risk and operational readiness, the dimensions a pilot rarely tests, and the review caught them before the system was allowed to pay a supplier on its own.

## How to use it

- **No change in authority without a completed review.** Upward changes always. Downward changes may be decided first, as a suspension, with the review completed within five business days.
- **Use the same form for every system.** The value of the review compounds when twenty systems answer the same twelve questions, because the gaps start to repeat and point at what the enterprise as a whole is missing.
- **Count the outcomes once a year.** A portfolio where every review ended in Expand is a portfolio nobody is reviewing.

## Lineage

The review borrows its shape from investment committee papers and credit approval memos, where a request is written against a fixed set of questions and decided by a named authority, and from stage-gate product reviews. The decision-rights question draws on the RAPID framework's insistence that one role holds the D. What the review adds for AI is the eight-dimension Evidence Chain, the rule that authority moves one state at a time on evidence, the requirement to name a demotion trigger and an exit condition before any expansion, and the ten-times question as a plain test of how much damage an unwatched error could do.

---

Part of the Enterprise AI Decision Toolkit, a set of open instruments for enterprise AI governance based on *The Enterprise AI Decision System: How AI Leaders Turn Capability into Authorized Enterprise Action* by Nitin Gupta, where it appears as Appendix A. Latest version: github.com/ngupta1137/enterprise-ai-decision-toolkit. Licensed under MIT.
