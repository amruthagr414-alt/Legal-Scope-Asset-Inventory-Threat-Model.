# 2. Asset Inventory

## 2.1 Inventory

| Asset ID | Asset | Purpose | Owner | Data / classification | Security importance |
|---|---|---|---|---|---|
| A-01 | Student laptop | Hosts and manages the lab | Student | Internal | High |
| A-02 | Web browser | User interface for the lab | Student | Test data | Medium |
| A-03 | OWASP Juice Shop | Intentionally vulnerable training application | Lab owner | Synthetic application data | High |
| A-04 | Local data store | Stores application records | Lab owner | Synthetic / lab-only | High |
| A-05 | Application logs | Records application activity | Lab owner | Internal; may contain sensitive details | Medium |
| A-06 | Lab configuration | Defines application settings | Lab owner | Confidential configuration | High |
| A-07 | Test accounts | Supports authorized test scenarios | Lab owner | Restricted test credentials | Medium |

## 2.2 Data classification

- **Public:** Information intentionally published in this repository.
- **Internal:** Lab notes, non-sensitive logs, and configuration descriptions.
- **Confidential:** Local configuration values that could expose the lab or host.
- **Restricted:** Passwords, tokens, session identifiers, or other authentication secrets.

Only synthetic data should be used. Never commit real passwords, API keys, session tokens, personal records, or unredacted sensitive logs to GitHub.

## 2.3 Trust boundaries

1. **TB-01 — Browser to application:** Requests cross from the user-controlled browser into the application.
2. **TB-02 — Application to data store:** The application reads and writes persistent lab data.
3. **TB-03 — Application process to host:** The application runs on the student's computer and must not be granted unnecessary host access.
4. **TB-04 — Administrator to lab:** Administrative actions require an authorized lab account and should be separated from ordinary user activity.

## 2.4 Key security assumptions

- The lab is bound to the loopback interface (`127.0.0.1`).
- The host operating system and Docker environment are maintained by the student.
- Test credentials are unique to the lab and are not reused elsewhere.
- The lab is stopped when it is not being used.
