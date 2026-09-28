# PROBE-001: bolt.new Specification Probe

| | |
|---|---|
| Date | 2026-09-28 |
| Accountable | Priya (Specifier) |
| Responsible | bolt.new (one prompt, no follow-ups) |
| Input | context/FEATURES.md as of commit "FEATURES.md: Kano and EARS v1", pasted in full, nothing else |
| Delegation record | docs/DDR-001.md |
| Code kept | None. The generated project was viewed on screen and discarded. |

## Prompt

"Build a web app that implements this specification exactly." followed by the full text of FEATURES.md.

## What bolt Had to Guess

Every item below is something the build did that FEATURES.md did not state. Each became an EARS row or an explicit exclusion.

| # | What bolt assumed | Why it had to guess | Change to FEATURES.md |
|---|---|---|---|
| 1 | Email and password login for every user, including crew leads | F1 said nothing about access | F1-5 (location link, no login) and exclusion X3 |
| 2 | A form to create invoices by hand | The spec never said where invoices come from | Exclusion X4 (synthetic CSV load) |
| 3 | A date picker defaulting to today, which allows past dates | F1-1 named a promised date with no range | F1-6 (confirm past or distant dates) |
| 4 | A currency dropdown with euros and pounds | F2-1 said "amount" with no unit | F2-5 (US dollars only) |
| 5 | A customer portal page listing each customer's promises | Nothing excluded a customer view | Exclusion X5 |
| 6 | A bar chart of promises by week on the home page | Nothing; this was decoration | None. Noted as something bolt adds unasked. |

## What bolt Got Right Without Guessing

The overdue sort order (F2-2), the Unmatched state (F1-3), and the single summary line for mass breakage (F3-2) all appeared as written. Rows written as EARS with an explicit IF came through intact; rows with an unstated unit or range did not.

## Reading

Five of six guesses were gaps in the spec. The sixth was the builder's taste. Five gaps in a first draft is a normal number; the useful finding is that four of them were about scope boundaries, which is why FEATURES.md now has an Exclusions section.
