# Data dictionary

## raw/helpdesk_tickets_raw.csv (simulated)
| Column | Description |
|---|---|
| ticket | Ticket code, e.g. `T-1000` |
| opened_raw | Opening date as text in 3 formats (`YYYY-MM-DD`, `DD/MM/YYYY`, `Mon DD, YYYY`) |
| requester | Requester e-mail (some malformed/upper-case) |
| dept_code | Department code (inconsistent case/spaces) |
| category | Issue category (inconsistent spelling) |
| priority | High / Medium / Low (inconsistent spelling, some missing) |
| resolution_hours | Hours to resolve, stored as text (some `n/a`, `unknown`, empty) |
| notes | Free text containing phone numbers and room codes |

## raw/departments.json
`dept_code`, `dept_name`, `college`, `staff_count`

## raw/sla_targets.xlsx
`priority`, `sla_hours` (High 8, Medium 24, Low 72)

## processed/helpdesk_clean.csv
Cleaned tickets + extracted fields (`phone`, `room`, `building`, `email_valid`, `email_domain`) + merged fields (`dept_name`, `college`, `staff_count`, `sla_hours`) + derived fields (`met_sla`, `hours_vs_sla`, `resolution_band`, `weekday`, `month`).
All data are simulated; no real personal data.
