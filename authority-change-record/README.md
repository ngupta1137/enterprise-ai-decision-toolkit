# The Authority Change Record

**Every change in what an AI system may do, written down, in either direction**

**Version 1.0 · October 2026 · Nitin Gupta**

Enterprises tend to record the moment an AI system is given more authority, because that moment comes with a launch, an approval, and a celebration. They rarely record the moments it should lose authority, because those come with an incident, a quiet drift in quality, or nothing at all.

The Authority Change Record is a single one-page form used for every change in an AI system's authority, whether that change grants more or takes it away. Using the same form in both directions is the point. When promotion and demotion follow the same process, demotion stops being an admission of failure and becomes ordinary governance.

Three rules give the record its force:

1. **Same form, both directions.** Promote, constrain, suspend, revoke, and restore all use this record, with the same evidence standard.
2. **Every grant expires.** Any authority above Recommend carries a sunset date. If the authority is not renewed by fresh evidence before that date, it reverts one state automatically. Authority without an expiry date is authority nobody is reviewing.
3. **Restoring needs new evidence.** After a demotion, authority is restored only on evidence gathered after the fix, never on the record that existed before the problem.

---

## The five change types

| Type | Direction | Typical trigger |
|---|---|---|
| **Promote** | Up | Pre-set promotion thresholds met with sufficient evidence |
| **Constrain** | Narrower, same state | Limits reduced: lower caps, fewer action types, smaller scope |
| **Suspend** | Down, temporary | A demotion trigger fires, or an incident is under investigation |
| **Revoke** | Down, lasting | The system no longer deserves the authority, or the use case ends |
| **Restore** | Up, after a demotion | Root cause fixed and fresh evidence gathered after the fix |

Renewal at a sunset date is recorded as a Promote to the same state, with fresh evidence.

---

## The record

### Section A: Identity

| Field | Entry |
|---|---|
| Record number | Sequential, never reused |
| System and agent identity | The unique identity in the agent inventory |
| Change type | Promote / Constrain / Suspend / Revoke / Restore |
| Requested by, date | |
| Prior record for this system | Record number of the last change |

### Section B: What changes

Record the change for each action type separately. A system can be promoted for one action type and constrained for another in the same record.

| Action type | Authority state before | Authority state after | Limits before | Limits after | Markets affected |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |

Authority states are: Observe, Recommend, Act with approval, Bounded autonomy, Expanded autonomy.

### Section C: Evidence

For Promote and Restore, list each threshold and the evidence against it. The date each threshold was set must be earlier than this record. A threshold written after the results came in does not count.

| Threshold | Date set | Required | Observed | Evidence period and volume | Met? |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |

For Constrain, Suspend, and Revoke, record the trigger instead:

| Trigger | Threshold | Observed | When detected | How detected |
|---|---|---|---|---|
| | | | | |

For Restore, add: **Root cause** (one paragraph), **Fix deployed** (date and reference), and **Evidence period after the fix** (start date, volume). Evidence from before the fix date is not accepted.

### Section D: Controls confirmed

The technical owner confirms each control is in place for the authority state after the change, before it takes effect.

| Control | Confirmed (Y/N) | Reference |
|---|---|---|
| New limits enforced outside the model | | |
| Approval requirements configured for the new state | | |
| Demotion triggers updated for the new state | | |
| Monitoring thresholds updated | | |
| Kill switch tested within the last 90 days | | |
| Agent inventory updated with new state | | |

A change does not take effect until every applicable control is confirmed.

### Section E: Sunset

| Field | Entry |
|---|---|
| Sunset date | Required for any state above Recommend. Default: 90 days for Bounded autonomy, 60 days for Expanded autonomy |
| State if not renewed | One state below the state granted here |
| Evidence required to renew | The thresholds that renewal must meet |

### Section F: Decision and acceptance

| Role | Name | Decision | Date |
|---|---|---|---|
| Accountable decision owner (holds the right to grant and revoke) | | Approve / Reject | |
| Risk owner (accepts residual risk of the new state) | | Accept / Decline | |
| Technical owner (confirms Section D) | | Confirmed | |
| Business owner (informed and agrees) | | Agree / Object | |

For Suspend, the accountable decision owner or a named delegate may act alone and immediately. The rest of the record is completed within five business days. Speed is allowed in the downward direction. It is never allowed in the upward direction.

---

## The log

Keep every record for every system in one place, in order. Over time the log becomes the most honest account an enterprise has of how its AI systems are actually governed:

- How often authority moves up versus down.
- How long each system holds each state before it is reviewed.
- How many sunsets lapsed without renewal, which shows whether reviews are really happening.
- How quickly suspensions happen after a trigger fires.

A log that shows only promotions describes a portfolio nobody is watching.

## How to use it

- **Create the first record at launch,** recording the initial authority state as a Promote from nothing. Every later change chains from it.
- **Put the sunset dates in the calendar of the accountable decision owner,** not only in a governance tool.
- **Bring the log to the scheduled authority review.** The review decides; the record proves the decision was made.

## Lineage

Change records are standard practice in IT service management, and sunset clauses are well established in legislation and regulation. What this instrument adds for AI is the application of both to authority itself: one symmetric record for raising and lowering what a system may do, an automatic reversion when authority is not renewed by evidence, and a rule that restoring authority after a problem requires evidence gathered after the fix.

---

Part of the Enterprise AI Decision Toolkit, a set of open instruments for enterprise AI governance based on *The Enterprise AI Decision System: How AI Leaders Turn Capability into Authorized Enterprise Action* by Nitin Gupta. Latest version: github.com/ngupta1137/enterprise-ai-decision-toolkit. Licensed under MIT.
