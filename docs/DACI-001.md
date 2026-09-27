# DACI-001: Which Problem Does the Team Build?

## Roles

| Role | Who |
|---|---|
| Driver | Priya |
| Approver | Leo (drawn by lot, Sep 25) |
| Contributors | Priya, Marcus, Dana, Leo |
| Informed | Instructor |

## Options

| Option | Owner | HW1 problem in one line |
|---|---|---|
| A. Late invoices | Priya | A three-location landscaping business is paid late and cannot say why. |
| B. Parking permits | Leo | Commuter students buy permits for lots that are full by 9 AM. |
| C. Club dues | Dana | Student organizations chase dues by group chat and lose track of who paid. |
| D. Tutoring matches | Marcus | A peer tutoring center matches by availability and ignores course history. |

## Weights (committed before scores)

| Criterion | Weight (1 to 5) | Why this weight |
|---|---|---|
| Still wicked at team scale | 5 | The course grades reasoning about a wicked problem. A tame problem wastes Phase 2. |
| Users the team can reach by Oct 22 | 4 | Phase 2 validation needs at least three real users. |
| Buildable on our stack in three weeks | 4 | Workers, D1, and a static page, which all four of us have shipped. |
| Data we can get legally and soon | 3 | Synthetic data is acceptable in the course, so this matters less than it would at work. |
| Meaning: at least three of us care | 4 | Google's re:Work finding. A problem only its owner cares about loses the other three by Phase 2. |

## Scores (1 to 5, median of four private scores)

| Criterion | Weight | A. Late invoices | B. Parking | C. Club dues | D. Tutoring |
|---|---|---|---|---|---|
| Wicked at team scale | 5 | 5 | 3 | 2 | 3 |
| Users reachable | 4 | 3 | 5 | 5 | 3 |
| Buildable | 4 | 4 | 4 | 5 | 2 |
| Data | 3 | 3 | 4 | 2 | 4 |
| Meaning | 4 | 4 | 2 | 2 | 3 |
| **Weighted total (max 100)** | | **78** | **71** | **64** | **59** |

Each member scored all four options privately and committed the sheet before the medians were computed. Owners scored their own problems; the medians absorb that.

## Decision

**Option A, late invoices.** Approved by Leo, 2026-09-26.

Runner-up: B, parking permits (71), kept as the fallback if the reopen trigger fires.

## Dissent

- Marcus: The users are business owners, and business owners are hard to schedule. Our users-reachable score of 3 is generous.

## What Would Reopen This

We cannot confirm three business owners or office managers for Phase 2 testing by **October 15**. If that happens, Priya drives DACI-002 between A with a narrowed user group and B.
