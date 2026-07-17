# ADR-002: Selection of OSPF as the Dynamic Routing Protocol

## Status

Accepted

## Date

July 2026

## Context

The enterprise network requires dynamic routing between Headquarters and branch offices.

The routing solution must:

* Scale effectively
* Support future growth
* Converge quickly
* Minimize administrative overhead
* Operate using open standards

Several routing protocols were evaluated.

---

## Decision

Open Shortest Path First (OSPF) was selected as the routing protocol for the enterprise network.

Single-area OSPF (Area 0) is implemented in Version 1.0.

---

## Rationale

### Open Standard

OSPF is vendor-neutral and interoperable across networking platforms.

### Fast Convergence

Route recalculation occurs rapidly following topology changes.

### Scalability

OSPF supports large enterprise environments.

### Efficient Routing

Shortest-path calculations optimize traffic forwarding.

### Industry Adoption

OSPF is widely deployed in enterprise networks and remains a valuable skill for networking professionals.

---

## Alternatives Considered

### RIP

Pros:

* Easy configuration
* Minimal learning curve

Cons:

* Slow convergence
* Limited scalability
* Hop-count restrictions

Decision:

Rejected.

---

### EIGRP

Pros:

* Fast convergence
* Efficient route calculation

Cons:

* Historically Cisco-centric
* Less commonly adopted in heterogeneous environments

Decision:

Rejected.

---

### Static Routing

Pros:

* Simple in small environments
* Full administrator control

Cons:

* High administrative overhead
* Poor scalability
* Difficult maintenance

Decision:

Rejected.

---

## Consequences

Positive:

* Improved scalability
* Faster convergence
* Reduced administrative effort
* Enterprise-ready routing design

Negative:

* Greater configuration complexity than RIP
* Additional troubleshooting considerations

---

## Future Considerations

Future project phases may evaluate:

* Multi-area OSPF
* Route summarization
* OSPF authentication
* Redistribution strategies

---

## References

RFC 2328: OSPF Version 2
Cisco OSPF Design Guide
