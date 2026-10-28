# The Stop Memo

**Ending an enterprise AI initiative on evidence, not exhaustion**

**Version 1.0 · October 2026 · Nitin Gupta**

Most enterprises know how to start an AI initiative. Very few know how to end one. Initiatives that should stop instead drift: the budget shrinks, the team thins out, the system keeps running at a fraction of its original scope, and nobody signs anything because nobody wants their name on a cancellation. Meanwhile the system often still holds authority to act.

The Stop Memo is a two-part instrument. Part one, the **Stop Line**, is written and signed when the initiative is funded, before anyone is invested in the outcome. Part two, the **Stop Decision**, is completed at each scheduled review and records one of four outcomes against that line.

Three principles sit underneath it:

1. **Write the stop line before the start date.** The conditions for ending an initiative are easiest to set honestly before anyone has spent money on it.
2. **A clear no is a result.** An initiative that proves, with evidence, that a use case should not scale has done its job.
3. **An AI system that has been stopped but not unwound is still acting.** Stopping the budget is not the same as removing the system's authority. Both have to happen.

---

## Part One: The Stop Line

*Complete at funding. Sign before work begins. Do not edit after launch; amendments are recorded as new dated versions.*

| Field | Answer |
|---|---|
| Initiative | |
| Decision the system supports | The specific recurring business decision, not the technology |
| Authority state requested | Observe / Recommend / Act with approval / Bounded autonomy / Expanded autonomy |
| Funding approved and period | |
| Review dates | At least every quarter, and at every request for more authority or funding |

### The four lines

Each line is a measurable condition. Crossing any one of them at a review triggers a Stop Decision. It does not automatically stop the initiative.

| Line | Question it answers | Written condition (number and date) |
|---|---|---|
| **Value line** | What business result must be visible, and by when, for this to be worth continuing? | |
| **Cost line** | What is the highest acceptable cost per accepted, completed action at production volume? | |
| **Risk line** | What level of incidents, policy breaches, or reversals is unacceptable? | |
| **Adoption line** | What share of eligible decisions must actually use the system, by when? | |

Write each line as a number with a date. "Meaningful improvement in forecast quality" is not a line. "Forecast error below the current manual process by the end of the second quarter, measured on the agreed holdout set" is a line.

### Signatures at funding

| Role | Name | Date |
|---|---|---|
| Accountable decision owner (holds the right to grant or revoke the system's authority) | | |
| Business owner (owns the outcome and economics) | | |
| Finance partner | | |
| Risk owner | | |

---

## Part Two: The Stop Decision

*Complete at every scheduled review. Takes 20 to 40 minutes when the evidence is prepared in advance.*

### Step 1: Evidence against the lines

| Line | Written condition | Evidence today | Crossed? |
|---|---|---|---|
| Value | | | Yes / No |
| Cost | | | Yes / No |
| Risk | | | Yes / No |
| Adoption | | | Yes / No |

If no line is crossed, record Continue and set the next review date. If any line is crossed, continue to Step 2.

### Step 2: The fresh money test

Answer one question, in writing, before discussing anything else:

> **If this initiative arrived today as a new proposal, with the evidence we have now and only the remaining cost ahead of it, would we fund it?**

Money already spent is not part of the answer. Neither is the effort the team has put in, or the fact that the work was announced. Only the remaining cost and the evidence now available count.

Record the answer: **Yes / No / Only with changes (list them).**

### Step 3: Choose one of four outcomes

| Outcome | Use it when | What happens next |
|---|---|---|
| **Continue** | No line is crossed, or a line was crossed for a cause that is already fixed and evidenced. | Set the next review date. |
| **Redesign** | The decision is still worth supporting, but this approach is not. A different pattern, scope, or authority level could pass the lines. | Write a new Stop Line for the redesigned initiative. The old one does not carry over. |
| **Park** | The use case is valid, but a condition outside the team's control blocks it (data access, a regulation, a dependency, budget timing). | Stop spending. Keep the assets in the Harvest Register. Write the specific revival condition and an expiry date. A parked initiative not revived by its expiry becomes a Stop. |
| **Stop** | The fresh money test answer is No, and no redesign would plausibly change it. | Complete the Authority Unwind and the Harvest Register. Close the initiative. |

**Parking is not a hiding place.** An initiative may be parked once. A second park requires the accountable decision owner to document why it is not a Stop.

### Step 4: Authority unwind

*Required for Stop, and for Park when the system holds any authority above Observe.*

Stopping a model is easy. Stopping what it was doing is harder, because an AI system that held authority has usually made commitments, absorbed work, and been woven into a process. Each row needs an owner and a date.

| Unwind item | What to record | Owner | Date |
|---|---|---|---|
| Decisions returned to people | Which decisions revert to human hands, which team takes them, and whether that team has the capacity | | |
| Open commitments | Actions the system started or promised that are still in flight: offers sent, tickets opened, orders placed, messages scheduled. Who honors, completes, or cancels each one. | | |
| Customer and partner impact | Anyone who will notice the change, and what they will be told | | |
| Credentials and access | Every system identity, API key, and permission the agent held, revoked and confirmed | | |
| Scheduled and triggered actions | Jobs, triggers, and integrations that would still fire, disabled and confirmed | | |
| Data | What is retained, what is deleted, on what schedule, under which policy | | |
| Contracts | Vendor notice periods, minimum commitments, and termination dates | | |
| Records | Action logs and audit trails preserved for the required retention period | | |

The unwind is complete only when the technical owner confirms in writing that the system can no longer change anything in any connected system.

### Step 5: Harvest register

Every stopped initiative returns something to the enterprise. Record it, give each item an owner, and say where it now lives.

| Asset | Examples | Where it now lives | Owner |
|---|---|---|---|
| Evaluation assets | Test sets, labeled cases, edge-case libraries, thresholds | | |
| Data and integrations | Cleaned data, pipelines, connectors to core systems | | |
| Governance artifacts | Authority boundaries, approval flows, monitoring designs | | |
| Decision insight | What the enterprise learned about the decision itself, independent of the technology | | |
| People | Skills built, and where those people go next | | |

The evaluation assets are usually worth the most. A test set built from real enterprise tasks shortens the next attempt at the same decision, whatever technology that attempt uses.

### Step 6: Record and recognition

Write three sentences, in plain language, for the portfolio record:

1. What the initiative set out to learn or prove.
2. What the evidence showed.
3. What the enterprise will do differently because of it.

Credit the team for the quality of the evidence, not for the outcome. A team that produced a clear, early, well-evidenced Stop has saved the enterprise more money than most teams that ship.

### Signatures at decision

| Role | Name | Decision | Date |
|---|---|---|---|
| Accountable decision owner | | Continue / Redesign / Park / Stop | |
| Business owner | | | |
| Finance partner | | | |
| Technical owner (confirms unwind complete, if Stop) | | | |

---

## How to use it

- **Attach the Stop Line to the funding request.** No Stop Line, no funding. This single rule does most of the work.
- **Bring the Stop Decision to every scheduled authority review.** The same meeting that asks whether a system has earned more authority should ask whether it has earned the right to continue.
- **Review the portfolio, not just the initiative.** Once a year, count how many initiatives reached each outcome. A portfolio with no Redesigns, Parks, or Stops is not a portfolio of winners. It is a portfolio nobody is reviewing.

## Lineage

The fresh money test draws on long-standing ideas in finance about sunk costs and zero-based budgeting, and stage-gate product development has used kill decisions for decades. What this instrument adds for AI specifically is the authority unwind, the recognition that a stopped AI system may still be holding permission to act and commitments in flight, and the requirement that the stop conditions be written before funding rather than argued after it.

---

Part of the Enterprise AI Decision Toolkit, a set of open instruments for enterprise AI governance based on *Enterprise AI Decision System: Turning Capability into Authorized Enterprise Action* by Nitin Gupta. Latest version: github.com/ngupta1137/enterprise-ai-decision-toolkit. Licensed under MIT.
