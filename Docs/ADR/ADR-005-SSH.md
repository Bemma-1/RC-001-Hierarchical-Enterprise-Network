# ADR-005: Adoption of SSH for Secure Device Administration

## Status

Accepted

## Date

July 2026

## Context

Network administrators require remote access to routers and switches for:

* Configuration
* Monitoring
* Maintenance
* Troubleshooting

Historically, Telnet has been used for remote administration. However, Telnet transmits credentials and management traffic in plaintext.

This creates significant security risks, including:

* Credential interception
* Session hijacking
* Unauthorized access
* Information disclosure

The organization requires secure remote administration capabilities.

---

## Decision

Secure Shell (SSH) Version 2 shall be implemented on all routers and switches.

Telnet access shall be disabled.

Remote administration shall occur exclusively through SSH.

---

## Rationale

### Encryption

SSH encrypts management traffic, protecting credentials and session data.

### Authentication

SSH supports secure user authentication.

### Confidentiality

Administrative commands cannot be easily intercepted during transmission.

### Integrity

SSH helps ensure management sessions are not modified in transit.

### Industry Best Practice

SSH is the standard protocol for secure network administration.

---

## Alternatives Considered

### Telnet

Pros:

* Easy configuration
* Minimal resource requirements

Cons:

* Plaintext credentials
* No encryption
* Significant security risks

Decision:

Rejected.

---

### Console-Only Administration

Pros:

* No remote attack surface

Cons:

* Operationally inefficient
* Not practical for distributed branch environments

Decision:

Rejected.

---

## Consequences

Positive:

* Secure administrative access
* Reduced credential exposure
* Compliance with security best practices

Negative:

* Additional configuration requirements
* SSH key management considerations

---

## Future Considerations

Future versions may implement:

* TACACS+ authentication
* Multi-factor authentication
* Public key authentication
* Centralized identity management

---

## References

RFC 4251: Secure Shell Protocol Architecture
Cisco Secure Management Best Practices
NIST SP 800-53
