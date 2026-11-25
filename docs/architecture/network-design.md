# Network design

## Design approach

Use logical segmentation to reduce unnecessary communication between workloads. Exact VLAN IDs, subnets and interfaces are left undecided until the virtual topology is deployed.

## Suggested segmentation

| Network | Example role | Policy intent |
|---|---|---|
| WAN / NAT | Controlled external connectivity | No direct inbound exposure |
| DMZ | Test service reachable from a controlled test client | Explicitly allow required service ports only |
| User | Client VMs | Access approved services, not management planes |
| Server | Infrastructure and application VMs | Restrict east-west traffic |
| Management | Hypervisor and network administration | Administrator devices only |
| Monitoring | Metrics and log collection | Collect only required telemetry |
| Backup | Backup targets | Restrict write and restore privileges |

## Addressing plan template

| Zone | VLAN ID | Subnet/CIDR | Gateway | DHCP | Notes |
|---|---|---|---|---|---|
| DMZ | TBD | TBD | TBD | TBD | Planned |
| User | TBD | TBD | TBD | TBD | Planned |
| Server | TBD | TBD | TBD | TBD | Planned |
| Management | TBD | TBD | TBD | TBD | Planned |
| Monitoring | TBD | TBD | TBD | TBD | Planned |
| Backup | TBD | TBD | TBD | TBD | Planned |

Do not reuse a subnet that conflicts with the host, VPN or home network.

## Traffic-policy worksheet

For every required flow, document source and destination zones, hosts or services, protocol and destination port, reason, direction, logging requirement and validation method.

Default to deny between zones, then add narrowly scoped rules for documented needs. Avoid broad any-to-any rules.

## Validation checklist

- Confirm each VM receives an address from the intended network.
- Confirm gateways and DNS settings are correct.
- Confirm allowed service flows work.
- Confirm unrelated cross-zone traffic is blocked.
- Confirm management services are not reachable from the user zone.
- Confirm logs identify the relevant rule or event.
- Save sanitized evidence and record the date and lab version.

All tests must remain inside the isolated lab or other explicitly authorized systems.
