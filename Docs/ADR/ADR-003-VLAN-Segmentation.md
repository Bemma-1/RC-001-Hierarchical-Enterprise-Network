# ADR-003: Adoption of VLAN-Based Network Segmentation

## Status

Accepted

## Date

July 2026

## Context

The enterprise network serves multiple groups of users, servers, and administrators. A flat Layer 2 network would place all devices within a single broadcast domain, leading to:

* Excessive broadcast traffic
* Reduced performance
* Increased security risks
* Limited traffic isolation
* Difficult policy enforcement

The organization requires logical separation of network resources while maintaining efficient communication.

---

## Decision

Virtual Local Area Networks (VLANs) shall be implemented to logically segment the enterprise network.

The following VLANs are deployed:

| VLAN ID | Name       | Purpose                |
| ------- | ---------- | ---------------------- |
| 10      | Users      | End-user devices       |
| 20      | Servers    | Enterprise servers     |
| 99      | Management | Network administration |

Inter-VLAN communication shall be controlled through Layer 3 routing.

---

## Rationale

### Improved Security

Sensitive resources such as servers and management interfaces are isolated from general user traffic.

### Reduced Broadcast Domains

Broadcast traffic remains within individual VLAN boundaries, improving overall network efficiency.

### Better Network Organization

Departments and services can be logically grouped regardless of physical location.

### Simplified Administration

Network policies can be applied consistently at VLAN boundaries.

### Scalability

Additional VLANs can be introduced as organizational requirements grow.

---

## Alternatives Considered

### Flat Network

Pros:

* Easy deployment
* Minimal configuration

Cons:

* Large broadcast domains
* Reduced security
* Difficult troubleshooting
* Limited scalability

Decision:

Rejected.

---

## Consequences

Positive:

* Enhanced security
* Improved performance
* Better traffic management
* Increased scalability

Negative:

* Additional configuration complexity
* Requirement for inter-VLAN routing

---

## Future Considerations

Potential future VLANs include:

* Voice VLAN
* Guest VLAN
* Wireless VLAN
* Security Operations VLAN

---

## References

IEEE 802.1Q VLAN Standard
Cisco Campus Network Design Guide
