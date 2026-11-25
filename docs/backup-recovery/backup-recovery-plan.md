# Backup and recovery plan

## Objectives

Protect lab configuration and data against accidental deletion, corruption and failed changes. A backup is not considered reliable until a restore has been tested.

## Scope

Identify which items need protection: infrastructure configuration exports, virtual machine data and templates, application configuration and test datasets, documentation and automation scripts, monitoring configuration and selected logs.

Do not include secrets in Git. Store sensitive backup material separately and protect it with appropriate access controls.

## Policy worksheet

| Item | Method | Frequency | Retention | Owner | Restore test |
|---|---|---|---|---|---|
| Lab documentation | Git history | Every meaningful change | Repository history | Maintainer | Clone and review |
| VM configuration | Hypervisor export / documented method | Before major changes | TBD | Maintainer | Import to isolated test |
| Application data | Application-consistent backup | TBD | TBD | Maintainer | Restore to test instance |
| Network configuration | Sanitized configuration export | After approved changes | TBD | Maintainer | Compare and validate |

Set actual frequency and retention after measuring the lab's data-change rate and storage capacity.

## Recovery procedure

1. Identify the affected component and stop changes that could worsen the issue.
2. Select a known-good backup and verify its date and integrity.
3. Restore to an isolated test location first when feasible.
4. Validate system boot, network configuration, service health and data consistency.
5. Record recovery time, issues and any data gap.
6. Return the component to service only after validation.
7. Update the runbook with lessons learned.

## Recovery objectives

Define a realistic Recovery Time Objective (RTO) and Recovery Point Objective (RPO) per service after measuring backup and restoration performance. Do not invent targets before testing.
