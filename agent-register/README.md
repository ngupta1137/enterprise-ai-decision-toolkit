# The Agent Register

**Every agent that can act: counted, owned, scoped, and stoppable**

**Version 1.0 · October 2026 · Nitin Gupta**

[Printable scope card and register](agent-register.pdf) · [Register template (CSV)](agent-register-template.csv) · [Back to the toolkit](../README.md)

A team can now stand up an AI agent in an afternoon. Every agent that can read a system or take an action holds some authority, whether or not anyone granted it. An agent nobody inventoried has authority nobody approved, an owner nobody named, and a stop procedure nobody has tested.

The rest of this toolkit governs systems the enterprise knows about. The Agent Register makes sure that is all of them. It has three parts: a **Scope Card** completed for each agent before it goes live, the **Register** that holds every card in one place, and a quarterly **Reconciliation** that compares the register with what is actually running.

Three rules sit underneath it:

1. **Every agent needs three things before it goes live: a scope, an owner, and a stop button.** The scope says what it may touch and what it may never touch. The owner is one named person who answers for it. The stop button is the tested way to take its authority back.
2. **No entry, no credentials.** An agent that is not in the register does not receive a service identity, an API key, or a write permission. Identity and access teams enforce this rule, not the agent's builders.
3. **The register is only true if it is reconciled.** Compare it with identities, keys, and scheduled jobs at least quarterly. A register nobody reconciles describes the agents someone remembered.

---

## What counts as an agent

Register any software that can take an action in an enterprise system on the basis of a model's output: write a record, send a message, approve a transaction, change a setting, schedule a job, or call another agent that does any of these. Two tiers keep the register usable.

| Tier | What it covers | What the register needs |
|---|---|---|
| **Acting** | Can write to, send from, or change anything in an enterprise system, directly or through another agent or tool | A full Scope Card |
| **Read-only** | Reads enterprise data and answers a person, with no ability to change anything | Identity, owner, data sources, and tier. Upgrade to Acting before any write permission is granted |

If in doubt, it is Acting. An assistant that can draft an email is Read-only. One that can send it is Acting.

---

## Part One: The Scope Card

*Complete before go-live. The card becomes the agent's register entry, and its first [Authority Change Record](../authority-change-record/) refers to it.*

### Identity

| Field | Answer |
|---|---|
| Agent ID | Unique, never reused |
| Name and purpose | One sentence: what decision or task it supports |
| Tier | Acting / Read-only |
| Non-human identity | The service identity or account it runs as, distinct from any person's |
| Built or bought | Built / Bought / Assembled. If bought, the vendor and product |
| Model and version | Pinned version, and who approves a change |
| Markets and business units | Where it runs |

### Scope: what it may touch

| Field | Answer |
|---|---|
| Systems it may read | Each system, with the data classification |
| Systems it may write to | Each system, with the action types allowed in each |
| Limits | Numeric caps per action type: value, volume, records changed per hour |
| May never touch | An explicit list: systems, data, action types, and customers or counterparties that are out of bounds, even if access exists |
| Decisions it may prepare | Analysis, drafts, and recommendations a person decides on |
| Decisions it may make | Actions it takes without a person approving each one, if any. Each must match its authority state |
| Agents and tools it may call | Every delegation path. No path may grant more than this card allows |

The "may never touch" line is the one teams skip and the one that matters most. Access drifts. An explicit exclusion list is how a reviewer notices when it has.

### Owner: who answers for it

| Role | Name | Holds |
|---|---|---|
| Accountable decision owner | | The right to approve, expand, restrict, or revoke its authority |
| Business owner | | The outcome and economics it affects |
| Technical owner | | Operation, monitoring, and recovery |
| Backup for the decision owner | | The same powers when the owner is unavailable |

One name per row. A team or a committee is not an owner.

### Stop button: how its authority is taken back

| Field | Answer |
|---|---|
| How to stop it | The mechanism: a switch, a revoked credential, a disabled policy. Not a code deployment |
| Who may press it | Named people, including someone available outside business hours |
| Scope of the stop | All actions, or also by action type and market |
| Time to stop, as tested | Minutes from decision to the last state-changing action |
| Last tested | Date, and the record of the test |
| What happens to work in flight | Actions started but not finished: completed, held, or cancelled, and by whom |
| Fallback | Who does the work while it is stopped |

An untested stop button is a belief, not a control. If you cannot take an agent's authority back, you never really gave it. You lost it.

### Authority at go-live

| Action type | Authority state | Limits | Authority Change Record |
|---|---|---|---|
| | Observe / Recommend / Act with approval / Bounded autonomy / Expanded autonomy | | |

New agents start at Observe or Recommend. Anything higher at go-live needs a completed [AI Authority Review](../ai-authority-review/) and a [Scorecard](../scorecard/) band that allows it.

### Signatures

| Role | Name | Date |
|---|---|---|
| Accountable decision owner | | |
| Technical owner (confirms identity, limits, and stop button are configured as written) | | |
| Identity and access (confirms credentials match this card) | | |

---

## Part Two: The Register

One row per agent, in one place, for the whole enterprise. A [CSV template](agent-register-template.csv) with these columns is included, with one fictional example row to show the format.

| Column | What it holds |
|---|---|
| Agent ID | From the Scope Card |
| Name | Short name |
| Purpose | One sentence |
| Tier | Acting / Read-only |
| Non-human identity | Service identity or account |
| Built or bought | And vendor, if bought |
| Model and version | Pinned version |
| Markets | Where it runs |
| Systems written to | From the Scope Card |
| Highest authority state | The highest state held for any action type |
| Accountable decision owner | One name |
| Business owner | One name |
| Technical owner | One name |
| Stop button last tested | Date |
| Latest Authority Change Record | Record number |
| Authority sunset | Date the current grant expires, if any |
| Scorecard band and date | From the most recent Readiness Scorecard |
| Next review | Date |
| Reconciliation status | Matched / Drifted / Unregistered / Retired, from the last sweep |

Three columns earn their place more than the rest. **Stop button last tested** shows how many agents could be stopped today. **Authority sunset** shows how many grants are quietly lapsing without review. **Highest authority state**, read against **Scorecard band**, shows how many agents hold more authority than their evidence allows.

---

## Part Three: The Reconciliation

*At least quarterly, and after any reorganization, platform migration, or acquisition. Owned by the identity and access team with the AI governance lead.*

**Step 1: Pull what is actually running.** From the identity provider, every non-human identity with write access to an enterprise system. From each AI and automation platform, every agent, API key, and scheduled job. From procurement, every product bought since the last sweep that includes agent features.

**Step 2: Match it to the register.** Each running agent lands in one of four outcomes.

| Outcome | What it means | Required response | Deadline |
|---|---|---|---|
| **Matched** | Registered, and its real permissions match its Scope Card | None | |
| **Drifted** | Registered, but its real permissions exceed its Scope Card, or its owner has left | Restrict permissions to the card, or raise an Authority Change Record to change the card. Replace any departed owner | 10 business days |
| **Unregistered** | Running, with credentials, and not in the register | Suspend its write permissions now. Complete a Scope Card, or retire it | Suspend at once. Card or retire within 10 business days |
| **Retired** | In the register, but no longer running or needed | Revoke every credential and close the entry with a dated note | 10 business days |

**Step 3: Report four numbers to the AI governance forum.**

1. Unregistered agents found this sweep, and how many were acting agents.
2. Share of acting agents whose stop button was tested in the last 90 days.
3. Share of acting agents holding more authority than their latest Scorecard band allows.
4. Authority grants that passed their sunset without renewal.

The first number is the one to watch over time. It should fall with every sweep. If it does not, the "no entry, no credentials" rule is not being enforced.

---

## How to use it

- **Make the register the gate for credentials.** The single rule that does the most work is that identity and access will not issue an agent credential without a register entry. Everything else follows from it.
- **Start with the agents you have.** Run the first reconciliation before writing any new cards. Most enterprises find agents they did not know about, and those are the ones to card first.
- **Keep it boring.** A spreadsheet or an existing configuration management database is enough. The register fails when it is incomplete, not when it is simple.
- **Bring it to the scheduled authority review.** The register shows which agents are due for review. The [AI Authority Review](../ai-authority-review/) decides. The [Authority Change Record](../authority-change-record/) records it.

## Relationship to the Scorecard

The Register is how a team earns Scorecard criteria 7.4 (agent identity and inventory), 2.1 and 2.2 (data sources and least-privilege access), 5.1 (tested kill switch), and 5.5 (delegation controls). A Scorecard applies to one system. The Register applies to all of them.

## Lineage

Asset inventories and configuration management databases are standard IT practice, and access recertification is a standard identity governance control. Banking supervisors have long expected firms to keep an inventory of their models, as in the US Federal Reserve and OCC guidance on model risk management (SR 11-7, 2011). What the Agent Register adds for AI is a required scope with an explicit "may never touch" list, the authority state and a tested stop button as required fields for every entry, the rule that no entry means no credentials, and a reconciliation designed to find agents that were never registered at all.

---

Part of the Enterprise AI Decision Toolkit, a set of open instruments for enterprise AI governance based on *The Enterprise AI Decision System: How AI Leaders Turn Capability into Authorized Enterprise Action* by Nitin Gupta. Latest version: github.com/ngupta1137/enterprise-ai-decision-toolkit. Licensed under MIT.
