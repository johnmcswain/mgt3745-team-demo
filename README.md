# GreenLine Promises: MGT 3745 Demo Team

A fictional four-person team's Phase 1 repository for MGT 3745 O, Fall 2026. It shows what a finished Specification Sprint looks like: governance, specification, architecture decision, and evaluation plan, with no product code yet.

> **About this repository.** The team, the business, and the users are invented for teaching. The commit history was scripted to show the order of work that Phase 1 requires (weights before scores, stakes before code, every change through a reviewed branch). The pull requests demonstrated in class on October 1 are real. Read the files as models of altitude and traceability; copying their wording into your own repository is a coherence problem.

## What

GreenLine Landscaping's customers promise to pay to whoever is standing in the yard, and nobody writes the promise down. Phase 2 builds a tool that captures those promises in the field and puts them in front of the person who follows up.

## Team

| Member | Phase 1 role | Phase 2 role |
|---|---|---|
| Priya | Specifier | Reviewer |
| Marcus | Architect | Implementer |
| Dana | Implementer | Specifier |
| Leo | Reviewer | Architect |

Working agreement, RACI matrix, and rotation plan: [TEAM.md](TEAM.md).

## Status

Phase 1 decided four things: which problem to build ([DACI-001](docs/DACI-001.md)), what to build ([FEATURES.md](context/FEATURES.md)), where it runs ([ADR-001](context/ARCHITECTURE.md)), and what would prove it works ([EVALS.md](context/EVALS.md)). Phase 2 builds F1 (log a promise) and F2 (overdue list with promise status) first, because the riskiest assumption lives in F1.

## Links, in Reading Order

1. [TEAM.md](TEAM.md): who owns what
2. [docs/DACI-001.md](docs/DACI-001.md): why this problem
3. [context/PROJECT.md](context/PROJECT.md): the problem, reframed
4. [context/USERS.md](context/USERS.md): three users and their jobs
5. [context/FEATURES.md](context/FEATURES.md): Kano and EARS
6. [docs/PROBE-001.md](docs/PROBE-001.md): what bolt.new had to guess
7. [context/ARCHITECTURE.md](context/ARCHITECTURE.md): the Gate, ADR-001, the diagram
8. [context/EVALS.md](context/EVALS.md): the tree, the RAT, four stakes
9. [context/CLAUDE.md](context/CLAUDE.md), [context/STANDARDS.md](context/STANDARDS.md), [context/TOOLS.md](context/TOOLS.md): how we work
10. [docs/DDR-001.md](docs/DDR-001.md): the one delegation in Phase 1
11. Previews for Phase 2: [STYLE.md](context/STYLE.md), [SKILLS.md](context/SKILLS.md), [AGENTS.md](context/AGENTS.md)

## AI Use

In Phase 1, AI tools were Responsible for one task (the bolt.new specification probe, [DDR-001](docs/DDR-001.md)) and Consulted on two (a critique of the draft Kano table and a first pass at merging four STANDARDS.md files, both noted in the pull request descriptions). No AI output was committed without a named reviewer. Nothing bolt.new generated is in this repository.
