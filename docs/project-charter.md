# Project charter

## Purpose
Build a small, isolated, reproducible enterprise-style infrastructure lab to demonstrate infrastructure engineering, networking, systems administration, defensive security, monitoring, and resilience.

## Scope
- Virtualization and resource planning
- Logical network segmentation and access boundaries
- Windows/Linux services, selected according to resource constraints
- Security configuration and defensive telemetry
- Monitoring and alerting
- Backup and restore exercises
- Documentation, evidence, and iterative improvement

## Out of scope
- Production deployment or production readiness claims
- Employer/client topology, data, configuration, or credentials
- Testing third-party systems
- Exposing lab services publicly by default
- Claims of implementation without evidence

## Success criteria
A success criterion is met only when it has a documented design, bounded scope, implementation evidence where applicable, a validation result, and a recorded limitation or remediation for any failure.

## Constraints and assumptions
- Isolated lab; synthetic data
- Resource-limited, single-maintainer environment
- All test systems owned or explicitly authorized
- No secrets in version control
- Changes are recorded and reversible where practical

## Deliverables
1. Architecture and decision log
2. Asset, network and service inventories
3. Security-control register
4. Monitoring and alert catalogue
5. Backup policy and restore evidence
6. Validation register and sanitized evidence
7. Lessons learned and final portfolio summary
