# Vendor Authority Gates

**Rent the intelligence. Keep the control.**

**Version 1.0 · October 2026 · Nitin Gupta**

Most enterprise AI is bought, not built, and that is usually the right call. The risk is not buying. The risk is buying in a way that quietly hands the vendor the decisions the enterprise should never give away: what the system is allowed to do, how good is good enough, what happened when something went wrong, how to stop it, and how to leave.

Vendor Authority Gates is an evaluation instrument with three parts:

1. **The Five Keeps.** Five pass or fail gates that every vendor must clear before any weighted scoring begins. They test whether the enterprise keeps control of its own decision system.
2. **The Claim Ledger.** A way to grade every vendor claim by the strength of its evidence, so a confident pitch cannot outrank a tested result.
3. **The Buyer-Owned Proof.** A proof of concept designed by the enterprise, on its own tasks and thresholds, before the vendor sees it.

The principle underneath all three: **a demo is evidence about the vendor; a proof is evidence about you.**

---

## Part One: The Five Keeps

Score each gate Pass or Fail. A Fail on any gate removes the vendor from consideration for any use case where the system will hold authority above Observe. It does not matter how strong the rest of the evaluation is.

Each gate lists the evidence that counts. A vendor statement, a roadmap item, or a slide is not evidence.

### Keep 1: Keep the Policy
The enterprise's decision rules and authority limits stay in a form the enterprise owns and can move.

**Pass requires all of:**
- Action limits (which actions, which systems, numeric caps) are configured by the enterprise, not hard-coded by the vendor.
- Those limits can be exported in a documented, readable format.
- The limits are enforced outside the model, so a model output cannot override them.

**Evidence that counts:** a live configuration session in which an enterprise user changes a limit, and an export file showing it.

### Keep 2: Keep the Bar
The enterprise decides how good is good enough, and can test any vendor against the same standard.

**Pass requires all of:**
- The enterprise can run its own evaluation set against the system, without the vendor curating the cases.
- Results are returned at the case level, not only as a summary score.
- The same evaluation can be re-run after every vendor model or platform update.

**Evidence that counts:** case-level results from the enterprise's own test set, run in the evaluation period.

### Keep 3: Keep the Record
The enterprise holds a complete, usable record of what the system did.

**Pass requires all of:**
- Every state-changing action is logged with trigger, agent identity, model and version, inputs or a reference to them, tool calls, approvals, and outcome.
- Logs can be exported in a documented format to an enterprise-controlled store.
- Retention is set by the enterprise, not limited by the vendor's default.

**Evidence that counts:** an exported log sample for a real test action, reconstructed end to end by an enterprise team member.

### Keep 4: Keep the Brake
The enterprise can stop the system, and nothing changes underneath it without notice.

**Pass requires all of:**
- An enterprise user can stop all state-changing actions without contacting the vendor and without a code deployment.
- Model versions can be pinned, and the vendor commits in the contract to advance notice of model, prompt, or default-setting changes that affect behavior.
- The enterprise can hold an update until its own regression tests pass.

**Evidence that counts:** a live stop performed by an enterprise user during the evaluation, and the contract clause on change notice.

### Keep 5: Keep the Exit
The enterprise can leave and take its working system with it.

**Pass requires all of:**
- Prompts, agent definitions, tool schemas, configurations, evaluation sets, and retrieval content can be exported in documented formats.
- The contract states exit assistance, data return, and deletion terms with dates.
- No essential component exists only inside the vendor's proprietary format with no export path.

**Evidence that counts:** an export of the evaluation-period configuration, and the exit clauses in the draft contract.

### Gate summary

| Keep | Pass / Fail | Evidence reference |
|---|---|---|
| 1. Keep the Policy | | |
| 2. Keep the Bar | | |
| 3. Keep the Record | | |
| 4. Keep the Brake | | |
| 5. Keep the Exit | | |

A vendor that fails a Keep may still be acceptable for Observe-only use, such as analysis or summarization with no ability to change anything. Record that restriction in the contract.

---

## Part Two: The Claim Ledger

Every material claim a vendor makes goes into the ledger, graded by the strongest evidence behind it.

| Grade | Meaning | Example |
|---|---|---|
| **Asserted** | Said in a pitch, a deck, or a document. | "Our agent resolves 80 percent of tickets without escalation." |
| **Demonstrated** | Shown working, but in the vendor's environment, on the vendor's data, with tasks the vendor chose. | A live demo on a sample help desk. |
| **Proven** | Shown working on the enterprise's own tasks, data, and thresholds, in the Buyer-Owned Proof. | Resolution rate measured on 400 of the enterprise's real tickets. |
| **Contracted** | Written into the contract with a measurement method and a remedy if it is not met. | A service level on resolution accuracy with a fee credit. |

**Two rules:**
- **In selection, only Proven claims count toward the score.** Asserted and Demonstrated claims can justify including a vendor in the proof, nothing more.
- **At renewal, only Contracted claims count.** Anything the enterprise relied on that was never contracted should be contracted at renewal or treated as unsupported.

### Ledger template

| # | Claim | Source | Grade | Evidence reference | Matters for which decision? |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

The ledger does something a scoring matrix cannot: it makes visible how much of a vendor's case rests on words. A shortlist where most of the leading vendor's strengths are Asserted is a shortlist that has not been evaluated yet.

---

## Part Three: The Buyer-Owned Proof

The enterprise writes the proof specification before any vendor sees it, and gives every shortlisted vendor the same one. Vendors may ask clarifying questions. They may not change the tasks, the data, or the thresholds.

### Specification

| Element | What the enterprise defines |
|---|---|
| Decision | The specific recurring business decision the system will support |
| Authority sought | The authority state the system would hold in production, by action type |
| Task set | The enterprise's own cases, including edge cases and known hard cases, held back from the vendor until the proof begins |
| Pass thresholds | Written quality thresholds for each action type, set before results are seen, stricter for irreversible actions |
| Failure behavior | What the system must do when it is uncertain, out of scope, or receives a hostile input |
| Human review burden | How the share of outputs needing human review will be measured, and the maximum acceptable share |
| Cost envelope | Expected volume and the maximum acceptable cost per accepted, completed action |
| Integration test | At least one real write action to a non-production copy of an enterprise system |
| Exit test | The configuration exported and re-run against a second model or provider, to show the work is portable |

### Proof report

For each vendor, report against the specification only: thresholds met or missed, review share, cost per action, failure behavior observed, integration result, exit result. Do not report features the specification did not ask about. They belong in a separate note, not in the score.

---

## Advisers have incentives too

If an adviser, integrator, or consultant is helping run the evaluation, ask them to disclose in writing any commercial relationship with a shortlisted vendor: resale, referral, co-selling, certification programs, or implementation revenue tied to the recommendation. Incentives do not make advice wrong. Undisclosed incentives make it impossible to weigh.

## How to use it

- **Run the Five Keeps first, in week one.** It is the cheapest way to shorten a shortlist, and it surfaces lock-in before anyone is attached to a product.
- **Start the Claim Ledger at the first vendor meeting.** Keep it running through contract signature.
- **Write the Buyer-Owned Proof before the RFP goes out,** so the proof design is not shaped by what vendors pitch.
- **Re-run Keeps 2, 4, and 5 at every renewal.** Control can erode as products change.

## Lineage

Pass or fail knockout criteria are common in enterprise procurement, and evidence grading has long roots in auditing and clinical research. What this instrument adds for AI is the specific set of five controls an enterprise must keep regardless of who supplies the model, and a grading scale that separates what a vendor demonstrated on its own terms from what the enterprise proved on its own.

---

Part of the Enterprise AI Decision Toolkit, a set of open instruments for enterprise AI governance based on *Enterprise AI Decision System: Turning Capability into Authorized Enterprise Action* by Nitin Gupta. Latest version: github.com/ngupta1137/enterprise-ai-decision-toolkit. Licensed under MIT.
