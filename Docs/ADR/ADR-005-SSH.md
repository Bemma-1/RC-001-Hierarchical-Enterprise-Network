# RC001-ADR-005 — SSH Version 2 for Secure Device Administration

## Document Information

| Field       | Value                                           |
| ----------- | ----------------------------------------------- |
| Project     | RC-001 — Secure Hierarchical Enterprise Network |
| Document ID | RC001-ADR-005                                   |
| Version     | 1.0                                             |
| Status      | Accepted                                        |
| Author      | Emmanuel Ampong                                 |
| Date        | 19 July 2026                                    |

---

## 1. Context

Network administrators require remote command-line access to routers and switches.

Remote management protocols differ significantly in how they protect administrative sessions and credentials.

The network therefore requires an encrypted remote-management protocol.

---

## 2. Decision

RC-001 shall use **SSH Version 2** for remote CLI administration.

Telnet shall not be required for normal remote administration.

Infrastructure shall be configured with:

* Device hostnames
* Domain name
* RSA keys
* SSH Version 2
* Local administrative accounts
* VTY local authentication
* SSH-only VTY transport

---

## 3. Alternatives Considered

### Telnet

#### Advantages

* Simple
* Widely understood
* Easy to configure

#### Disadvantages

* Does not provide adequate encryption for administrative sessions
* Credentials and session data may be exposed on untrusted networks
* Unsuitable as the preferred secure-management protocol

**Decision:** Rejected.

---

### SSH Version 1

#### Advantages

* Encrypted remote management compared with Telnet

#### Disadvantages

* Obsolete protocol version
* Known security weaknesses
* Superseded by SSH Version 2

**Decision:** Rejected.

---

### SSH Version 2

#### Advantages

* Encrypted management sessions
* Improved confidentiality
* Widely supported
* Appropriate for Cisco infrastructure administration

**Decision:** Accepted.

---

## 4. Credential Handling

Real personal passwords shall not be published in the GitHub repository.

Public configuration examples shall use:

* Lab-only credentials
* Redacted values
* Clearly identified placeholders

No production secrets, API keys, private keys, or reusable personal credentials shall be committed.

---

## 5. Consequences

### Positive

* Administrative sessions are encrypted.
* Telnet dependency is eliminated.
* The project demonstrates secure-management fundamentals.
* SSH supports future centralized AAA integration.

### Negative

* Requires hostname/domain configuration and RSA key generation.
* Credentials must still be managed securely.
* SSH alone does not provide complete identity governance.

---

## 6. Future Enhancements

Future projects may introduce:

* AAA
* TACACS+
* RADIUS
* Role-based administrative access
* Management ACLs
* Centralized logging
* Key-based authentication where supported

---

## 7. Related Documents

* RC001-NRS-001
* RC001-HLD-001
* RC001-LLD-001
* RC001-IPP-001

---

**Decision Status: ACCEPTED**

**End of Document**
