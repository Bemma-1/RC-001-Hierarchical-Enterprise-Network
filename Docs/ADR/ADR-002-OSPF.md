# RC001-ADR-002 — Selection of OSPF as the Interior Gateway Protocol

## Document Information

| Field       | Value                                           |
| ----------- | ----------------------------------------------- |
| Project     | RC-001 — Secure Hierarchical Enterprise Network |
| Document ID | RC001-ADR-002                                   |
| Version     | 1.0                                             |
| Status      | Accepted                                        |
| Author      | Emmanuel Ampong                                 |
| Date        | 19 July 2026                                    |

---

## 1. Context

The enterprise requires routing between:

* Kumasi Headquarters
* Accra Branch
* Takoradi Branch

The routing architecture must also support future branch expansion.

A routing strategy was required that reduces manual route administration while providing a foundation for scalable enterprise routing.

---

## 2. Decision

RC-001 shall use **Open Shortest Path First (OSPF)** as its Interior Gateway Protocol.

The baseline implementation shall use:

* OSPF Process ID 1
* Area 0
* Explicit router IDs
* Passive LAN-facing interfaces where appropriate

Router IDs:

* HQ-R1 — 1.1.1.1
* ACC-R1 — 2.2.2.2
* TAK-R1 — 3.3.3.3

---

## 3. Alternatives Considered

### Static Routing

#### Advantages

* Simple in very small networks
* Predictable
* Low protocol overhead

#### Disadvantages

* Manual maintenance
* Poor scalability
* Greater administrative burden as branches increase
* Route changes require manual intervention

**Decision:** Rejected as the primary enterprise routing strategy.

---

### RIP

#### Advantages

* Simple configuration
* Easy to understand

#### Disadvantages

* Limited scalability
* Hop-count metric
* Maximum 15-hop routing diameter
* Less appropriate for modern enterprise design

**Decision:** Rejected.

---

### EIGRP

#### Advantages

* Efficient convergence
* Straightforward Cisco implementation
* Advanced metric calculation

#### Disadvantages

* Historically associated primarily with Cisco-centric environments
* OSPF provides stronger standards-oriented relevance for this research portfolio

**Decision:** Not selected.

---

### OSPF

#### Advantages

* Open-standard link-state protocol
* Dynamic route learning
* Scalable hierarchical design capability
* Supports future multi-area architecture
* Widely used in enterprise networking
* Suitable for route convergence experiments

**Decision:** Accepted.

---

## 4. Rationale

OSPF provides an appropriate balance between:

* Enterprise relevance
* Scalability
* Dynamic routing capability
* Research value
* Packet Tracer support

The single-area Area 0 implementation is appropriate for the current topology while allowing future expansion toward multi-area OSPF.

---

## 5. Consequences

### Positive

* Routes are dynamically learned.
* New internal networks can be advertised without creating static routes on every router.
* The design supports routing convergence experiments.
* Future branch expansion is easier.

### Negative

* OSPF is more complex than static routing.
* Incorrect network statements can create routing problems.
* OSPF requires troubleshooting knowledge.

---

## 6. Future Evolution

Future research may evaluate:

* Multi-area OSPF
* Route summarization
* OSPF authentication
* Redundant paths
* OSPF convergence under link failure
* Comparison with other routing approaches

---

## 7. Related Documents

* RC001-NRS-001
* RC001-HLD-001
* RC001-LLD-001
* RC001-IPP-001

---

**Decision Status: ACCEPTED**

**End of Document**
