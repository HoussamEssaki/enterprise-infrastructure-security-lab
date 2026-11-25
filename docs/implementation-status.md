# Implementation status

This file separates planned design from verified implementation.

## Current status

| Workstream | State | Evidence |
|---|---|---|
| Repository structure and documentation baseline | Implemented | Initial documentation committed |
| Architecture design | Planned | Design overview available |
| Network segmentation | Planned | Addressing and traffic worksheets prepared |
| Systems and core services | Planned | To be recorded after deployment |
| Security controls | Planned | Defensive control checklist prepared |
| Monitoring | Planned | Monitoring strategy prepared |
| Backup and recovery | Planned | Policy and restore procedure prepared |
| Validation | Planned | Test register prepared |

## Evidence policy

Only change a workstream to Implemented after the component has been deployed. Change it to Tested only after the relevant validation has passed and evidence is recorded.

## Next milestones

1. Choose the hypervisor and document host resource constraints.
2. Create an isolated virtual network and inventory the lab VMs.
3. Complete the addressing plan before configuring inter-zone routing.
4. Deploy one service at a time and record sanitized configuration notes.
5. Validate segmentation, monitoring and backup restoration.
6. Add screenshots and diagrams only after they represent the actual lab.

## Change log

- 2026-11-25: Initial repository documentation baseline created. No infrastructure deployment is claimed by this commit.
