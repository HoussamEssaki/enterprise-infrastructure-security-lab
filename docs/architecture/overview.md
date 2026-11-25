# Architecture overview

## Purpose and scope

This document describes the target architecture for an isolated, small enterprise-style learning environment. It is a design baseline; implementation details must be updated to match the actual lab.

### Design goals

- Separate workloads by purpose and trust level.
- Keep management interfaces away from ordinary user networks.
- Centralize essential logs and service health information.
- Make backup and restoration responsibilities explicit.
- Keep the environment small enough to reproduce and troubleshoot.

## Logical zones

| Zone | Purpose | Default stance |
|---|---|---|
| Edge | Controlled connectivity to external networks | Deny unsolicited inbound access |
| DMZ | Services intentionally exposed to a test network | Allow only documented flows |
| Users | Workstations and user-oriented services | Least privilege |
| Servers | Infrastructure and application services | Permit only required service flows |
| Management | Hypervisor and network-device administration | Restricted administrator access |
| Monitoring | Metrics, logs and alerting | Read-only collection where practical |
| Backup | Protected backup copies | Separate access and retention controls |

## Main components

Component selection is vendor-neutral. Record product, version, resource allocation and role only after deployment.

- Hypervisor and virtual machines.
- Virtual switching and an edge firewall/router.
- Linux and/or Windows server workloads.
- DNS, DHCP and time synchronization where required.
- Monitoring and centralized log collection.
- Backup storage and a separate test-restore target.

## Trust boundaries

1. External or simulated WAN to edge.
2. Edge to internal zones.
3. User zone to server zone.
4. Administrator workstation to management zone.
5. Lab workloads to backup infrastructure.

Every crossing should have an explicit purpose, source, destination, protocol and owner.

## Operational assumptions

- The lab uses non-production, synthetic data.
- All test systems are owned or explicitly authorized.
- Internet access is limited to required updates and documentation.
- Administrative access uses unique accounts and multi-factor authentication where supported.
- Backups are not considered valid until a restoration test succeeds.

## Decisions to record

Maintain an architecture decision log with date, context, options, decision, trade-offs and validation. Do not copy confidential designs from an employer or internship.
