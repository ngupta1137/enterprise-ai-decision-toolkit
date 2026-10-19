# Contributing

Thanks for helping improve the Enterprise AI Decision Toolkit. The goal is instruments that any two reasonable people would fill in the same way, given the same evidence. Contributions that move toward that goal are the most welcome.

## What to contribute

**Reading disagreements.** If two people scored a criterion, graded a vendor claim, or rated a market dimension differently, open an issue naming the instrument, the item, both answers, and what each person was looking at. These are the most valuable reports, because they show exactly where the wording is ambiguous.

**Missing failure modes.** If you have seen an enterprise AI system fail in a way no instrument would have caught, describe the failure (without confidential details) and suggest which instrument it belongs in.

**Threshold feedback.** If a number is wrong for your industry or risk level (20 test cases per action type, a 15-minute kill switch, a 90-day sunset on bounded autonomy), explain why and what you would use instead.

**Field reports.** If you used an instrument in a real decision, a short note on what worked and what did not helps more than a proposed rewrite.

**Clarity fixes.** Typos, unclear wording, or language that is vague enough to be argued either way.

## How to contribute

1. **Open an issue first** for anything beyond a typo. Describe the problem before proposing a fix.
2. **Fork and branch** once the change is agreed.
3. **Keep the style.** Plain practitioner language. No hype, no em dashes, no criteria such as "ensure appropriate governance." Every item must name something a team can show as evidence.
4. **Keep scales cumulative.** Where an instrument uses graded anchors, a higher grade must require everything in the one below it.
5. **Keep the shared vocabulary.** The five authority states (Observe, Recommend, Act with approval, Bounded autonomy, Expanded autonomy) are used across every instrument. Changes to them affect all six.
6. **Open a pull request** that references the issue and explains what changed and why.

## What will not be accepted

- Code, tooling, or automation. This repository holds the instruments and their documentation only.
- Vendor or product references. The instruments are tool-neutral.
- Items that cannot be answered from evidence.
- Additions that add length without catching a distinct failure.

## Versioning

Changes to criteria, gates, thresholds, bands, or decision rules increase that instrument's version number and are listed in the top-level README. Wording-only fixes do not.

## Conduct

Be direct, be specific, and assume good intent. Critique the instrument, not the person.
