# Defensive security controls

## Control objectives

The lab explores foundational defensive controls. This document is a checklist, not evidence that controls are already deployed.

### Identity and access

- Use named administrator accounts rather than shared daily-use accounts.
- Apply least privilege and separate administration from ordinary browsing.
- Enable multi-factor authentication where supported.
- Review local administrator and privileged-group membership.
- Remove or disable unused accounts and services.

### Systems hardening

- Maintain an inventory of operating systems, versions and owners.
- Apply security updates through a documented maintenance process.
- Enable host firewalls and restrict listening services.
- Use secure remote administration settings.
- Synchronize system time for reliable event correlation.
- Back up configuration before significant changes.

### Network protection

- Segment user, server, management, DMZ and backup workloads.
- Deny unsolicited inbound traffic by default.
- Document firewall exceptions with an owner and review date.
- Restrict administrative interfaces to the management zone.
- Use secure management protocols and protect administrative credentials.

### Endpoint and data protection

- Enable supported endpoint protection in the lab.
- Use synthetic data and avoid storing personal or employer-confidential information.
- Encrypt sensitive backup media where supported.
- Define retention and secure disposal for test data.

### Vulnerability and configuration management

- Maintain a software and asset inventory.
- Review vendor security advisories and apply updates.
- Record findings with severity, affected asset, remediation and retest result.
- Do not run intrusive testing against systems outside the isolated lab or without explicit authorization.

## Evidence format

For each control, record control ID, objective, implementation state, scope, sanitized configuration reference, validation date, result, evidence path, owner and remediation.

Use the labels Planned, Implemented, Tested and Not applicable consistently.
