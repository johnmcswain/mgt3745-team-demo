# STANDARDS.md

Merged from four members' HW5 versions by Dana, with Copilot drafting the first merge (a C row in TEAM.md). Where two rules conflicted, the stricter one was kept; each such choice is marked **Merged:**.

## Documents

- Markdown, one H1 per file, headings in title case.
- No em dashes. Use a colon, a comma, parentheses, or two sentences. **Merged:** Priya and Leo already required this; Marcus and Dana did not.
- Tables for anything compared across more than two items.
- Every EARS row has an ID (F1-1) and traces to a job statement.
- Dates as YYYY-MM-DD in records; plain dates in prose.

## Code (Phase 2)

- JavaScript modules, `const` by default, no `var`.
- `textContent` for any user-supplied text. Never `innerHTML` with user data.
- SQL through `prepare().bind()` only. **Merged:** Marcus's HW5 file allowed template strings for "trusted" values; the team rule allows none.
- Every `fetch` checks `res.ok` and shows the user a message on failure.
- No `console.log` in committed code. **Merged:** Dana allowed it behind a DEBUG flag; the stricter rule won, and Dana's dissent is in the merge commit.
- No secrets, tokens, or location links in the repository, ever.

## Git

- Branch names: `role/short-description`, lowercase, hyphens. Example: `spec/features-kano`.
- One artifact per pull request where possible.
- Commit messages: `FILE: what changed`. Example: `USERS.md: merge four profiles into three`.
- Pull request description has four parts: What changed, RACI row, How to check it, AI use.
