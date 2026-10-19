# The Market Authority Passport

**Authority is earned in a market, not in a model**

**Version 1.0 · October 2026 · Nitin Gupta**

An AI system that has earned real authority in its home market carries that track record into every new country like a passport. The passport proves who the system is and what it has done. It does not grant entry. Each new market issues its own visa, with its own conditions, based on what the home evidence can and cannot prove about local conditions.

Most global rollouts skip the visa. The system that worked in one market is switched on in the next at the same authority level, as if language, regulation, data, integrations, and customer expectations were identical. They rarely are, and the failures that follow are usually quiet: a little worse, in a language nobody on the central team reads, for months.

The passport has three parts: the **evidence portability check**, the **seven-dimension visa review**, and the **visa itself**. One rule governs entry:

> **Every new market starts one step down.**

A system enters a new market at least one authority state below the state it holds at home, unless every dimension of the visa review is rated Transfers. Authority is then re-earned locally, usually faster than the first time, because the passport accelerates the review. It never eliminates it.

---

## Part One: Evidence Portability Check

Before reviewing the market, sort the home-market evidence by whether it can travel at all.

| Evidence | Portability | Why |
|---|---|---|
| Kill switch tested, approval enforcement, limits enforced outside the model | **Travels** | Control mechanisms behave the same if the same platform runs them. Confirm they are deployed in the new region. |
| Logging, tracing, identity, and access design | **Travels** | Confirm retention and storage location meet local rules. |
| Evaluation method, rubric, and thresholds | **Travels as a method** | The way quality is judged can carry over. The results cannot. |
| Evaluation results and quality scores | **Does not travel** | Measured on home-market data, language, and behavior. |
| Language and tone quality | **Does not travel** | Must be tested in the local language and dialect, by native speakers. |
| Regulatory clearance | **Does not travel** | Classification, disclosure, and oversight duties differ by jurisdiction. |
| Integration behavior | **Does not travel** | Local instances of the same enterprise system often differ in configuration, data, and failure behavior. |
| Business outcome and value evidence | **Does not travel** | Customer behavior, pricing, and competition differ. |
| Cost per completed action | **Partially travels** | Compute cost travels. Review rate, rework, and local support cost do not. |

The left-hand column is the passport. Only the rows marked Travels can be presented as evidence in the new market without re-testing.

---

## Part Two: Seven-Dimension Visa Review

Rate each dimension for the specific market and use case. Every rating needs evidence.

- **Transfers:** home evidence is sufficient for this dimension in this market.
- **Transfers with conditions:** home evidence mostly holds, with named local adjustments that must be completed before entry.
- **Re-earn:** home evidence says nothing reliable here; local evidence must be built from the start.

| Dimension | The question for this market | Rating | Evidence | Local owner |
|---|---|---|---|---|
| **Regulatory** | Does this use case face the same classification, disclosure, and oversight duties here? | | | |
| **Data** | Is local data comparably complete, lawful to use, and accessible from where the system runs? | | | |
| **Language** | Has the system been tested in the real language, dialect, and register customers and staff use here? | | | |
| **Cultural** | Are customer expectations and acceptable interventions comparable? | | | |
| **Action** | Is each action legal, reversible, and economically sensible here, and do the local target systems behave the same way? | | | |
| **Control** | Are oversight, escalation, on-call, and recovery available locally, in local hours and language? | | | |
| **Outcome** | Can results be observed and attributed as quickly and reliably as at home? | | | |

### Entry ceilings

Some ratings cap the entry state regardless of the others:

| If this dimension is rated Re-earn | The highest entry state is |
|---|---|
| Regulatory or Action | Recommend |
| Language or Control | Act with approval |
| Data, Cultural, or Outcome | One state below home (the default rule) |

Apply the lowest ceiling that any dimension triggers.

---

## Part Three: The Visa

The visa is a one-page record issued for each market, signed before the system takes any action there.

| Field | Entry |
|---|---|
| System and use case | |
| Market | |
| Home authority state (per action type) | |
| Entry authority state (per action type) | |
| Ceiling applied, and which dimension triggered it | |
| Conditions to complete before entry | From every dimension rated Transfers with conditions |
| Local evaluation set | Size, source, and who built it; must include local-language and local edge cases |
| Local scope cap | Volume, value, customer segment, or region limit during the first period |
| Local authority owner | A named person in or accountable for this market, with the power to restrict or revoke |
| Local risk acceptance | Named risk owner, signed |
| Promotion path | The evidence and thresholds that would lift the market to the next state |
| First review date | No later than 90 days after entry |
| Signatures | Global authority owner and local authority owner |

**Both signatures are required.** Architecture can be global. Permission is local.

---

## Keeping visas current

A visa is issued against a specific version of the system. Review every active visa when:

- The model, the prompts, or the authority boundary change at home.
- The local regulation, data source, or target system changes.
- A local incident or a demotion trigger fires in any market running the same system.

A material change at home does not automatically revoke local visas. It does require each local owner to confirm, in writing, that the market's evidence still holds.

## How to use it

- **Issue a visa for the home market too.** It forces the team to write down what the home authority actually rests on, which is often less than people assume.
- **Run the visa review before localization work starts,** not after. The ratings tell you which localization work matters.
- **Track a portfolio view.** A simple table of systems by markets, showing the authority state in each cell, is often the first time leadership sees that one system is running at five different levels of trust around the world.

## Lineage

Product localization and market-entry checklists are well established, and regulated industries have long required jurisdiction-by-jurisdiction approval. What this instrument adds is the treatment of AI authority itself as the thing that must be requalified: a default rule that every new market starts one state down, explicit ceilings tied to specific dimensions, and a split between evidence that travels and evidence that never does.

---

Part of the Enterprise AI Decision Toolkit, a set of open instruments for enterprise AI governance based on *The Enterprise AI Decision System: How AI Leaders Turn Capability into Authorized Enterprise Action* by Nitin Gupta. Latest version: github.com/ngupta1137/enterprise-ai-decision-toolkit. Licensed under MIT.
