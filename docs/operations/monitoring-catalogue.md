# Monitoring catalogue

| ID | Layer | Signal / check | Purpose | Severity guidance | Response notes | Status |
|---|---|---|---|---|---|---|
| MON-HOST-01 | Host | Resource availability | Detect capacity / availability issues | Based on impact and sustained condition | Confirm scope and trends | Proposed |
| MON-SVC-01 | Service | Service availability | Detect loss of expected service | Based on service importance | Verify health and dependency | Proposed |
| MON-BACKUP-01 | Backup | Last successful job / restore status | Assess recoverability | Escalate overdue or failed protection | Review job and recovery plan | Proposed |
| MON-SEC-01 | Security | Selected security events | Investigate defensive signals | Context and confidence dependent | Preserve evidence, follow lab procedure | Proposed |

Avoid unnecessary personal-data collection and noisy alerting. Tune and validate each alert before treating it as operational.
