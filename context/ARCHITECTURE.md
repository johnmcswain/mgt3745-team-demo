# ARCHITECTURE.md

## The Gate: Build, Buy, or Delegate

Where the Phase 2 system runs and who writes it. Weights were committed before any option was scored.

### Weights

| Criterion | Weight (1 to 5) | Why |
|---|---|---|
| Fits the promise job (J-Jamal, J-Tom) | 5 | A tool that tracks invoices without promises solves the old problem. |
| Team capability | 4 | Three weeks leaves no time to learn a new platform. |
| Switching cost | 4 | Scored from HW4 and HW5, where moving data and redeploying cost each of us an evening. |
| Control of customer data | 5 | Customer names and amounts, even synthetic, are the most sensitive thing in the system. |
| Cost | 3 | Free tiers exist for every option; cost matters only past the course. |

### Scores (1 to 5)

| Criterion | Weight | Build: Worker, D1, static page | Buy: reminder features in off-the-shelf invoicing software | Delegate: bolt.new-generated and hosted app |
|---|---|---|---|---|
| Fits the promise job | 5 | 5 | 2 | 4 |
| Team capability | 4 | 5 | 3 | 2 |
| Switching cost | 4 | 4 | 2 | 2 |
| Control of customer data | 5 | 4 | 2 | 2 |
| Cost | 3 | 5 | 2 | 4 |
| **Weighted total (max 105)** | | **96** | **46** | **58** |

**Notes on the scores.**
- Buy: the products we looked at send reminders about invoices. None records what a customer told someone in the field, which is the whole job. Scored on the nearest fit.
- Delegate: the probe (docs/PROBE-001.md) showed bolt can produce a plausible app from our spec in minutes, and also that it invents a login, a currency picker, and a customer portal. Team capability scores low because none of us could maintain generated code we did not write. Delegation stays available for bounded pieces in Phase 2, each with a DDR.
- Switching cost for Build is 4 because `wrangler d1 export` produced a portable SQL file in HW4, and the Worker is one file.
