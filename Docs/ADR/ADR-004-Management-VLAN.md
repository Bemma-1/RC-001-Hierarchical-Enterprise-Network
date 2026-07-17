# ADR-004: Implementation of a Dedicated Management VLAN

## Status

Accepted

## Date

July 2026

## Context

Network devices require administrative access for:

* Monitoring
* Configuration
* Maintenance
* Troubleshooting

Using production user networks for management traffic introduces several risks:

* Unauthorized access attempts
* Increased attack surface
* Difficulty controlling administrative traffic
* Reduced visibility of management activities

The organization requires secure and centralized network administration.

---

## Decision

A dedicated Management VLAN (VLAN 99) shall be deployed.

All manageable network devices shall receive management IP addresses from the Management VLAN.

Only authorized administrators shall use this network for device management.

---

## Rationale

### Security

Management traffic is isolated from regular user traffic.

### Reduced Exposure

Administrative interfaces are not directly exposed to production user networks.

### Simplified Monitoring

Management traffic can be identified and monitored more easily.

### Improved Troubleshooting

Administrative access remains available even when production VLAN issues occur.

### Industry Best Practice

Dedicated management networks are widely used in enterprise environments.

---

## Alternatives Considered

### Management Through User VLANs

Pros:

* Simpler deployment
* Fewer VLANs required

Cons:

* Increased security risks
* Reduced traffic separation
* Limited administrative control

Decision:

Rejected.

---

## Consequences

Positive:

* Improved security
* Better traffic separation
* Enhanced manageability

Negative:

* Additional VLAN administration
* Additional IP address allocation

---

## Future Considerations

Future versions may implement:

* Out-of-band management
* AAA services
* TACACS+
* Centralized management systems

---

## References

Cisco Enterprise Management Design Guide
NIST SP 800-115
