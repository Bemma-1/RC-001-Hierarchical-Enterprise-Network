# RC001-ADR-004 — Dedicated Network Management VLAN

## Document Information

| Field       | Value                                           |
| ----------- | ----------------------------------------------- |
| Project     | RC-001 — Secure Hierarchical Enterprise Network |
| Document ID | RC001-ADR-004                                   |
| Version     | 1.0                                             |
| Status      | Accepted                                        |
| Author      | Emmanuel Ampong                                 |
| Date        | 19 July 2026                                    |

---

## 1. Context

Routers and switches require IP connectivity for administration, monitoring, troubleshooting, and configuration.

Using ordinary end-user VLANs for infrastructure management would mix administrative and user traffic and make future security policy enforcement more difficult.

---

## 2. Decision

VLAN 99 shall be reserved for network management.

Management subnets:

* HQ — 10.10.99.0/27
* Accra — 10.20.99.0/28
* Takoradi — 10.30.99.0/28

Examples:

* HQ-SW1 — 10.10.99.2
* HQ-SW2 — 10.10.99.3
* ACC-SW1 — 10.20.99.2
* TAK-SW1 — 10.30.99.2

---

## 3. Alternatives Considered

### Management Through User VLANs

#### Advantages

* Simpler initial configuration

#### Disadvantages

* Mixes management and user traffic
* Poor logical separation
* Harder to secure later
* Less professional operational model

**Decision:** Rejected.

---

### Dedicated Out-of-Band Management Network

#### Advantages

* Strong operational isolation
* Management can remain available during some production-network failures

#### Disadvantages

* Requires additional infrastructure
* Outside the scope of the Packet Tracer baseline

**Decision:** Deferred.

---

### Dedicated Management VLAN

#### Advantages

* Logical separation
* Easier infrastructure identification
* Supports centralized SSH administration
* Provides foundation for future ACL/AAA controls

**Decision:** Accepted.

---

## 4. Security Limitation

A management VLAN alone does not guarantee that only administrators can access management interfaces.

Future controls should include:

* ACLs
* AAA
* TACACS+ or RADIUS
* Management firewall policy
* Out-of-band management

RC-001 establishes the architectural foundation.

---

## 5. Consequences

### Positive

* Management addresses are organized separately.
* Troubleshooting is easier.
* Administrative traffic is logically separated.
* Future management-access policies can be applied more cleanly.

### Negative

* Requires additional VLAN and subnet configuration.
* Incorrect trunk configuration can disrupt management connectivity.
* Additional policy controls are required for strong access restriction.

---

## 6. Related Documents

* RC001-NRS-001
* RC001-HLD-001
* RC001-LLD-001
* RC001-IPP-001

---

**Decision Status: ACCEPTED**

**End of Document**
