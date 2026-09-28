# FEATURES.md

Kano classification first, then EARS acceptance criteria for every Must-be and Performance feature. Every EARS row traces to a job statement in USERS.md (J-Rosa, J-Tom, J-Jamal). Rows marked PROBE-001 were added after the bolt.new specification probe (docs/PROBE-001.md).

## Kano Classification

| ID | Feature | Class | Evidence and reasoning |
|---|---|---|---|
| F1 | Log a customer's payment promise from the field | Must-be | Without it nothing else has data. J-Jamal and J-Rosa. |
| F2 | Overdue list showing promise status per invoice | Must-be | J-Tom's whole job statement. Absence makes the tool pointless to the office. |
| F3 | Reminder to the office when a promised date passes | Performance | More timely equals more useful, linearly. Tom checks weekly today. |
| F4 | Mark a promise kept or broken | Performance | Tom wants it; Rosa said she would use it only if it takes one tap. |
| F5 | Filter the overdue list by location | Performance | Three locations, one office manager. Useful in proportion to volume. |
| F6 | Weekly summary for the owner | Attractive | Rosa did not ask for it and lit up when Priya described it. |
| F7 | Automatic texts or emails to customers | Reverse | Both owners interviewed said this would damage relationships. Excluded. |

The Kano table was critiqued by Claude before review (a C row in TEAM.md). It suggested F4 was Must-be; Priya kept Performance because Rosa's condition (one tap) is a performance threshold. The disagreement is recorded in the review comment on the pull request that merged this table.

## EARS Acceptance Criteria

### F1. Log a Promise (J-Jamal, J-Rosa)

- F1-1. THE SYSTEM SHALL let a crew lead record a promise with three inputs: invoice number, promised date, and an optional note of up to 140 characters.
- F1-2. WHEN a crew lead submits a promise, THE SYSTEM SHALL store it with the submitting location and a timestamp, and confirm on screen within 2 seconds.
- F1-3. IF the invoice number does not match an open invoice, THEN THE SYSTEM SHALL keep the entry, mark it Unmatched, and say so on screen, so that nothing said in the yard is lost.
- F1-4. IF the network is unavailable when a promise is submitted, THEN THE SYSTEM SHALL hold the entry on the device and send it when the network returns, showing Pending until then.
- F1-5. THE SYSTEM SHALL require no login for crew leads in Phase 2; access is by a location link that the office can revoke. (PROBE-001 #1)
- F1-6. IF a promised date is in the past or more than 60 days out, THEN THE SYSTEM SHALL ask the crew lead to confirm the date before saving. (PROBE-001 #3)

### F2. Overdue List With Promise Status (J-Tom)

- F2-1. THE SYSTEM SHALL list every invoice more than 7 days past due, with customer name, amount, days overdue, location, and promise status (None, Promised, Broken, Kept).
- F2-2. THE SYSTEM SHALL sort invoices with no promise first, then by days overdue, descending.
- F2-3. WHEN a promise is recorded for an invoice, THE SYSTEM SHALL show it on the list the next time the page loads.
- F2-4. IF an invoice has more than one promise, THEN THE SYSTEM SHALL show the most recent and a count of earlier ones.
- F2-5. THE SYSTEM SHALL show amounts in US dollars only; multi-currency is out of scope. (PROBE-001 #4)

### F3. Promise-Date Reminder (J-Tom, J-Rosa)

- F3-1. WHEN a promised date passes without the invoice being marked paid or kept, THE SYSTEM SHALL mark the promise Broken and show it at the top of the office list the next morning.
- F3-2. IF more than 20 promises break on the same day, THEN THE SYSTEM SHALL show a single summary line instead of 20 rows, so a data error does not bury the list.

### F4. Kept or Broken (J-Tom)

- F4-1. WHEN the office marks a promise Kept or Broken, THE SYSTEM SHALL record who marked it and when, in one tap from the list.
- F4-2. IF a promise is marked Kept and the invoice is still open a week later, THEN THE SYSTEM SHALL flag the mismatch.

### F5. Location Filter (J-Tom)

- F5-1. THE SYSTEM SHALL filter the overdue list by any combination of the three locations.
- F5-2. IF no invoices match the filter, THEN THE SYSTEM SHALL say so, naming the filter, instead of showing an empty table.

## Exclusions

These are decisions, recorded so nobody builds them by accident.

- **X1. No customer contact of any kind (F7).** The system never sends a message to a customer.
- **X2. No payment processing.** The system records promises and statuses; money moves elsewhere.
- **X3. No crew-lead accounts in Phase 2.** Revisit if a location link is shared outside the company. (PROBE-001 #1)
- **X4. No accounting-software integration in Phase 2.** Invoices are loaded from a synthetic CSV. (PROBE-001 #2)
- **X5. No customer-facing view.** (PROBE-001 #5)
