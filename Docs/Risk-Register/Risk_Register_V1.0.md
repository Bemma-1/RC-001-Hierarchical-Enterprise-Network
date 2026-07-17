# Risk Register v1.0

## Project

RC-001: Hierarchical Enterprise Network Design and Implementation

## Purpose

This document identifies potential risks that may affect the successful design, implementation, operation, and evaluation of the enterprise network.

---

# Risk Assessment Methodology

Risk levels are determined using:

| Probability | Description            |
| ----------- | ---------------------- |
| Low         | Unlikely to occur      |
| Medium      | May occur occasionally |
| High        | Likely to occur        |

| Impact | Description                  |
| ------ | ---------------------------- |
| Low    | Minimal effect on operations |
| Medium | Noticeable disruption        |
| High   | Significant disruption       |

---

# Risk Register

| ID   | Risk                               | Probability | Impact | Risk Level | Mitigation Strategy                                |
| ---- | ---------------------------------- | ----------- | ------ | ---------- | -------------------------------------------------- |
| R001 | Incorrect OSPF configuration       | Medium      | High   | High       | Validate routing tables and neighbor relationships |
| R002 | VLAN misconfiguration              | Medium      | High   | High       | Verify VLAN assignments and trunk ports            |
| R003 | Incorrect IP addressing            | Medium      | Medium | Medium     | Implement IP addressing plan and peer review       |
| R004 | SSH configuration failure          | Low         | Medium | Low        | Test remote access after deployment                |
| R005 | Device configuration errors        | Medium      | High   | High       | Maintain configuration backups                     |
| R006 | WAN link failure                   | Medium      | High   | High       | Implement redundant links in future versions       |
| R007 | Unauthorized administrative access | Low         | High   | Medium     | Enforce SSH and secure credentials                 |
| R008 | Documentation inconsistencies      | Medium      | Medium | Medium     | Version control all project artifacts              |
| R009 | Packet Tracer limitations          | Medium      | Medium | Medium     | Document simulation assumptions                    |
| R010 | Human error during testing         | Medium      | Medium | Medium     | Follow structured test procedures                  |

---

# Highest Priority Risks

The following risks require continuous monitoring:

* OSPF misconfiguration
* VLAN implementation errors
* Device configuration mistakes
* WAN connectivity failures

---

# Risk Ownership

| Risk Category | Owner                 |
| ------------- | --------------------- |
| Routing       | Network Engineer      |
| Security      | Network Administrator |
| Documentation | Project Author        |
| Testing       | Project Author        |

---

# Risk Review Schedule

Risks shall be reviewed:

* During design completion
* During implementation
* During validation testing
* Prior to final project submission

---

# Version History

| Version | Date      | Description     |
| ------- | --------- | --------------- |
| 1.0     | July 2026 | Initial release |
