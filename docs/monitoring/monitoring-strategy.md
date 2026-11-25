# Monitoring strategy

## Objectives

Provide visibility into service availability, resource health and relevant security events without collecting unnecessary personal data.

## Monitoring layers

| Layer | Examples of signals | Intended use |
|---|---|---|
| Host | CPU, memory, disk, uptime | Capacity and availability |
| Network | Interface state, latency, packet loss | Connectivity troubleshooting |
| Services | DNS, DHCP and application health checks | Service availability |
| Security | Authentication events, firewall decisions, endpoint alerts | Defensive investigation |
| Backup | Job status, age of last successful copy, restore-test result | Recoverability |

## Alert design

Each alert should have a clear condition and threshold, severity and expected impact, a named response owner, a short triage checklist, and a resolution record.

Avoid alerting on every transient event. Tune thresholds after observing normal lab behavior.

## Log handling

- Synchronize clocks across systems.
- Collect only logs needed for troubleshooting and defensive monitoring.
- Restrict access to log storage.
- Define retention based on lab needs and available storage.
- Avoid placing passwords, tokens or unnecessary personal information in logs.
- Record gaps in collection and time synchronization.

## Operational review

A weekly review can check monitored assets, alert quality, disk capacity, time synchronization, failed backup jobs and unresolved findings. Record the outcome in lab-notes.
