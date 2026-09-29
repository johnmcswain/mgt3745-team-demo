# TEAM.md

## Working Agreement

- **Meetings.** Sundays 7:00 PM ET and Wednesdays 8:30 PM ET on Teams, 45 minutes, agenda in the team chat by noon the same day. Leo keeps time.
- **Channel.** Team chat for coordination. Anything that changes an artifact goes in a pull request comment, so the record lives with the file.
- **Response time.** Within 24 hours on weekdays, 36 hours on weekends. A pull request waiting for review more than 24 hours can be reviewed by any other member.
- **Quiet member clause.** If a member has not responded for 48 hours, the Driver of the nearest open decision messages them directly and copies the team. At 72 hours, the team reassigns that member's open Responsible rows and records the change in this file with the date. At 96 hours, or on October 6 if sooner, the team emails the instructor with this clause and the dates. Returning members pick up the next open row; nobody is punished for coming back.
- **Disagreement.** If a disagreement survives one meeting, it becomes a DACI in `docs/`, and the owner of the affected file is the Driver.
- **Dates.** First meeting Sep 25. Roster and protection Sep 25 and 26. DACI-001 closed Sep 26. Role PRs open by Sep 28. Reviews done Sep 29.

## Roster

| Name | Role | GitHub | Contact hours (ET) |
|---|---|---|---|
| Priya | Specifier | @priya-demo | Weekdays after 6 PM |
| Marcus | Architect | @marcus-demo | Mornings before 10 AM |
| Dana | Implementer | @dana-demo | Evenings and weekends |
| Leo | Reviewer | @leo-demo | Weekdays 12 to 2 PM, evenings |

The handles are placeholders for fictional members. In class, two real accounts stand in for all four.

## RACI Matrix (Phase 1)

R = Responsible (does the work), A = Accountable (answers for it; exactly one person), C = Consulted (asked before), I = Informed (told after). AI tools may be R or C and are never A.

| Artifact | Priya | Marcus | Dana | Leo | AI tools |
|---|---|---|---|---|---|
| TEAM.md | R | R | R | A | |
| docs/DACI-001.md (problem choice) | R | C | C | C | |
| context/PROJECT.md | A | C | I | C | |
| context/USERS.md | A | I | C | C | |
| context/FEATURES.md | A | C | I | C | C: Claude critiqued the Kano table; Priya is A |
| context/ARCHITECTURE.md (Gate, ADR-001, diagram) | C | A | C | I | |
| context/STANDARDS.md | I | C | A | C | C: Copilot drafted the merge; Dana is A |
| context/TOOLS.md | I | C | A | C | |
| context/CLAUDE.md | C | C | A | C | |
| .github/CODEOWNERS and branch protection | I | I | A | C | |
| docs/PROBE-001.md (bolt.new probe) | A | I | C | C | R: bolt.new ran the probe; Priya is A |
| docs/DDR-001.md | C | I | A | I | |
| context/EVALS.md (OST, RAT) | C | C | I | A | |
| context/EVALS.md (Prediction Stakes) | R | R | R | A | |
| Pull request reviews | R | R | R | A | |
| README.md | C | C | R | A | |

Where a row has no R, the A also did the work.

## Rotation Plan

| Member | Phase 1 | Phase 2 | Final |
|---|---|---|---|
| Priya | Specifier | Reviewer | Architect |
| Marcus | Architect | Implementer | Specifier |
| Dana | Implementer | Specifier | Reviewer |
| Leo | Reviewer | Architect | Implementer |

Nobody holds the same role twice, and every role is filled in every phase.

## Meeting Log

| Date | Decision or note | Recorded by |
|---|---|---|
| Sep 25 | Roles assigned; Leo drawn as DACI-001 Approver | Leo |
| Sep 26 | DACI-001 closed: late invoices | Priya |
