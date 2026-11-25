# Validation plan

## Purpose

Provide repeatable, non-destructive checks that demonstrate whether the lab behaves as designed. Record results rather than assuming success.

## Test register

| ID | Area | Test | Expected result | Status |
|---|---|---|---|---|
| NET-01 | Addressing | Verify each VM subnet and gateway | Matches approved addressing plan | Planned |
| NET-02 | Segmentation | Verify an approved service flow | Required service is reachable | Planned |
| NET-03 | Segmentation | Verify an unapproved cross-zone flow | Traffic is blocked | Planned |
| SYS-01 | Systems | Verify time synchronization | Hosts use configured time source | Planned |
| SEC-01 | Access | Review privileged accounts | Only approved accounts retain privileges | Planned |
| MON-01 | Monitoring | Stop a test service in the isolated lab | Alert is generated and documented | Planned |
| BCP-01 | Recovery | Restore a test backup to an isolated target | Data and service checks pass | Planned |

## Evidence record

For every test, capture test ID and date, lab version and affected components, preconditions, high-level steps, expected and observed result, Pass/Fail/Blocked status, sanitized evidence reference, follow-up action and retest date.

## Completion criteria

A phase is complete only when its design is documented, the component is deployed in the isolated lab, relevant tests have recorded results, failed tests have remediation or a documented limitation, and evidence contains no secrets or confidential information.
