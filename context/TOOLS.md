# TOOLS.md

One row per external service. No credentials in this file, ever.

| Service | Trusted with | Credentials live | Crossing statement | Switching cost |
|---|---|---|---|---|
| GitHub and Codespaces | All files and history; each member's codespace | Each member's GitHub account | "Everything in this repository, including every draft and review comment, is stored by GitHub (Microsoft) in a public repository. The team is accountable, and Dana answers for its settings." | Low: git clone anywhere |
| GitHub Copilot | Repository contents as context for suggestions | Each member's GitHub account | "Any file open in a codespace may be sent to Copilot as context, so nothing sensitive is ever in the repository. Each member is accountable for what Copilot sees in their session." | Low: turn it off |
| Claude (chat) | Context files pasted for critique | Each member's own account | "Only files from /context and /docs are pasted into Claude, by the member doing the pasting, who is accountable for what they paste." | Low: stop using it |
| Cloudflare Workers and D1 (Phase 2, planned) | Promises and synthetic invoices; request metadata including IP addresses | Implementer's Cloudflare account; wrangler token in their codespace | "Promises typed in the field and the synthetic invoice list will be stored on D1 under Cloudflare's free-tier terms, in a region we do not choose. Dana is accountable until rotation." | Medium: export with wrangler d1 export, rewrite one Worker |
| wrangler (npm) | Deploy access to the Cloudflare account | Token inside the codespace | "An npm package maintained by Cloudflare runs with deploy rights to our account. The Implementer is accountable for its version." | Low: it is the deploy tool, replaceable by the dashboard |
