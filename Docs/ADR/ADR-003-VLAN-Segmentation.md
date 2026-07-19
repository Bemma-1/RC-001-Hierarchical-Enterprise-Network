# RC001-ADR-003 — VLAN-Based Network Segmentation

## Document Information

| Field       | Value                                           |
| ----------- | ----------------------------------------------- |
| Project     | RC-001 — Secure Hierarchical Enterprise Network |
| Document ID | RC001-ADR-003                                   |
| Version     | 1.0                                             |
| Status      | Accepted                                        |
| Author      | Emmanuel Ampong                                 |
| Date        | 19 July 2026                                    |

---

## 1. Context

The headquarters supports multiple organizational functions:

* Human Resources
* Finance
* Operations
* Information Technology
* Executive/Management
* Servers
* Network Management

Placing all devices in a single Layer 2 broadcast domain would reduce scalability and make network administration more difficult.

---

## 2. Decision

IEEE 802.1Q VLAN segmentation shall be used.

Headquarters VLANs:

| VLAN | Function               |
| ---: | ---------------------- |
|   10 | Human Resources        |
|   20 | Finance                |
|   30 | Operations             |
|   40 | Information Technology |
|   50 | Executive/Management   |
|   60 | Servers                |
|   99 | Network Management     |

Branches shall use:

* VLAN 10 — Users
* VLAN 99 — Management

Each VLAN shall map to a unique IP subnet.

---

## 3. Alternatives Considered

### Flat Layer 2 Network

#### Advantages

* Simple initial setup

#### Disadvantages

* Large broadcast domain
* Poor logical organization
* Difficult troubleshooting
* Limited scalability
* Weak foundation for future security policies

**Decision:** Rejected.

---

### Physical Network Separation

Departments could use completely separate physical switching infrastructure.

#### Advantages

* Strong physical separation

#### Disadvantages

* Higher equipment requirements
* Inefficient port utilization
* Greater operational complexity
* Less flexible than logical segmentation

**Decision:** Rejected.

---

### VLAN Segmentation

#### Advantages

* Creates separate broadcast domains
* Supports logical departmental organization
* Efficiently uses shared switching infrastructure
* Simplifies subnet design
* Creates a foundation for future access-control policies

**Decision:** Accepted.

---

## 4. Important Security Limitation

VLAN segmentation does **not by itself guarantee access-control isolation** once inter-VLAN routing is enabled.

In RC-001, VLANs provide:

* Broadcast-domain separation
* Logical segmentation
* Structured addressing
* A foundation for future security enforcement

Comprehensive restrictions between departments require controls such as:

* ACLs
* Firewalls
* Identity-based policy

These are outside the baseline RC-001 scope.

---

## 5. Consequences

### Positive

* Smaller broadcast domains
* Better organization
* Easier troubleshooting
* Scalable departmental design
* Foundation for future policy enforcement

### Negative

* Requires trunk configuration
* Requires Layer 3 routing between VLANs
* VLAN/trunk mismatches can cause connectivity failures
* Additional security controls are required for strict inter-department authorization

---

## 6. Related Documents

* RC001-NRS-001
* RC001-HLD-001
* RC001-LLD-001
* RC001-IPP-001

---

**Decision Status: ACCEPTED**

**End of Document**
