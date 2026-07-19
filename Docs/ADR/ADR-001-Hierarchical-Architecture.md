# RC001-ADR-001 — Hierarchical Network Architecture

## Document Information

| Field        | Value                                           |
| ------------ | ----------------------------------------------- |
| Project      | RC-001 — Secure Hierarchical Enterprise Network |
| Organization | Ashanti Logistics Ghana Ltd.                    |
| Document ID  | RC001-ADR-001                                   |
| Version      | 1.0                                             |
| Status       | Accepted                                        |
| Author       | Emmanuel Ampong                                 |
| Date         | 19 July 2026                                    |

## Revision History

| Version | Date         | Change                                                     |
| ------- | ------------ | ---------------------------------------------------------- |
| 1.0     | 19 July 2026 | Architecture decision aligned with finalized RC-001 design |

---

## 1. Context

Ashanti Logistics Ghana Ltd. requires a network architecture connecting its Kumasi headquarters with branch offices in Accra and Takoradi.

The network must support:

* Multiple departments
* Centralized servers
* Network segmentation
* Dynamic routing
* Secure administration
* Future expansion

A flat network architecture would provide limited modularity and become increasingly difficult to manage as the organization grows.

An architectural model was therefore required that could organize network functions into logical layers while remaining practical for implementation in Cisco Packet Tracer.

---

## 2. Decision

RC-001 shall use a **hierarchical enterprise network architecture**.

At headquarters, the traditional hierarchical model is represented through a compact/collapsed implementation:

* Routing/core function — HQ-R1
* Aggregation/distribution function — HQ-SW1
* Access function — HQ-SW2

Branch offices shall use a simplified architecture consisting of:

* Branch router
* Managed access switch
* User and management VLANs

The design intentionally represents hierarchy logically without deploying unnecessary physical devices.

---

## 3. Alternatives Considered

### Alternative 1 — Flat Network

All devices could exist within a small number of broadcast domains.

#### Advantages

* Simple initial configuration
* Fewer logical components
* Lower implementation complexity

#### Disadvantages

* Larger broadcast domains
* Poor scalability
* Difficult troubleshooting
* Weak organizational structure
* Difficult future policy enforcement

**Decision:** Rejected.

---

### Alternative 2 — Full Three-Tier Campus Architecture

Separate physical core, distribution, and access layers could be implemented.

#### Advantages

* Strong modularity
* High scalability
* Closer to large-enterprise architecture
* Supports redundancy more naturally

#### Disadvantages

* Excessive complexity for the RC-001 scale
* Requires more simulated equipment
* Introduces redundancy and high-availability concerns beyond the baseline project scope

**Decision:** Deferred.

A fuller redundant architecture will be explored in RC-002.

---

### Alternative 3 — Collapsed Hierarchical Architecture

Core/routing and distribution responsibilities are consolidated while preserving logical access-layer separation.

#### Advantages

* Appropriate for small-to-medium enterprise scale
* Lower complexity
* Maintains hierarchical design principles
* Easier troubleshooting
* Provides a path for future expansion

**Decision:** Accepted.

---

## 4. Rationale

The hierarchical model was selected because it provides:

* Modularity
* Scalability
* Easier troubleshooting
* Clear separation of network functions
* Structured expansion
* Better documentation
* A foundation for future redundancy

The collapsed implementation balances professional design principles with the scope and limitations of the Packet Tracer environment.

---

## 5. Consequences

### Positive

* Network functions are clearly organized.
* New departments can be added more easily.
* Additional access switches can be introduced without redesigning the entire network.
* Troubleshooting boundaries are clearer.
* Future projects can introduce redundancy incrementally.

### Negative

* HQ-R1 remains a single point of failure.
* HQ-SW1 remains a critical aggregation device.
* The architecture does not provide full enterprise redundancy.

These limitations are accepted for RC-001.

---

## 6. Future Evolution

RC-002 may extend the architecture through:

* Redundant routers
* Redundant distribution switching
* HSRP
* EtherChannel
* Spanning Tree optimization
* Dual WAN connectivity

---

## 7. Related Documents

* RC001-NRS-001
* RC001-HLD-001
* RC001-LLD-001
* RC001-IPP-001

---

**Decision Status: ACCEPTED**

**End of Document**
