# PROJECT.md

## Original Problem Statement (Priya, HW1)

GreenLine Landscaping, a family business with three locations, is paid late on roughly one invoice in five, and the owner cannot say why.

## Reframed for the Team

At GreenLine, customers promise to pay to whoever is standing in the yard, usually a crew lead, and nobody writes the promise down. The office follows up on every overdue invoice the same way, blind to what was said in the field, so follow-up is late, awkward for the crew, and inconsistent across three locations.

**What the reframe changed.** The problem now belongs to three people: the crew lead who hears the promise, the office manager who follows up, and the owner who absorbs the cost. Solved now means a promise reaches the person who acts on it the same day, which we can observe in three weeks. The owner's original measure, days sales outstanding, stays as a long-run outcome we will not move during the course.

**Why it is still wicked.** Every fix changes a relationship. A reminder that works on one customer offends another. Crew leads are paid to mow, and anything that feels like collections work will be ignored. The owners disagree among themselves about how hard to push.

## Outcome

Increase the share of overdue invoices that have a recorded customer promise, from roughly none today (owner's estimate) to a majority of those where a field conversation happened.

## Scope for Phase 2

- In: recording a promise in the field, showing overdue invoices with their promise status, reminding the office when a promise date passes.
- Out: contacting customers, taking payments, connecting to accounting software, crew-lead accounts. See the exclusions in FEATURES.md.

## Constraints

- Synthetic data only. No real GreenLine customer data enters any tool or repository during the course.
- Course stack: Cloudflare Workers, D1, static HTML, CSS, and JavaScript.
- Three weeks of build time in Phase 2.

## Stakeholders

| Stakeholder | Interest | Relationship to the work |
|---|---|---|
| Owner (Rosa) | Cash flow and customer goodwill | User; supplied the problem |
| Office manager (Tom) | A Monday list he can trust | Primary user of F2 and F3 |
| Crew leads (Jamal and five others) | Staying out of collections work | Primary user of F1 |
| Customers | Being treated fairly | Affected; never contacted by the system |
