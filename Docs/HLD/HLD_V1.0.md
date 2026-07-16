### High-Level Design (HLD) v1.0
#### Project Title

RC-001: Hierarchical Enterprise Network Design and Implementation

#### Purpose

This document presents the high-level design for a scalable and secure enterprise network supporting a Headquarters (HQ) and three branch offices located in Accra, Kumasi, and Takoradi.

The design applies industry-standard hierarchical networking principles to improve scalability, security, performance, and manageability while providing a foundation for future growth.

#### Business Problem

Many organizations experience challenges related to:

Poor network scalability
Flat network architectures
Limited fault isolation
Weak network segmentation
Difficult network administration
Security vulnerabilities

The organization requires a network architecture that supports multiple sites while maintaining operational efficiency and security.

#### Project Objectives

The network shall:

Support connectivity between HQ and branch offices.
Enable logical separation of departments.
Provide centralized management.
Support secure administrative access.
Facilitate dynamic routing.
Allow future expansion without major redesign.
Design Requirements
Functional Requirements
Inter-site communication.
Inter-VLAN routing.
Dynamic route advertisement.
Secure device administration.
Server access from authorized networks.
Non-Functional Requirements
Scalability.
Reliability.
Security.
Manageability.
Availability.
Network Sites
Headquarters (HQ)

#### Functions:

Core routing
Distribution switching
Server hosting
Network management
Branch Offices
Accra Branch

Supports local users and WAN connectivity.

Kumasi Branch

Supports local users and WAN connectivity.

Takoradi Branch

Supports local users and WAN connectivity.

#### Network Architecture

The design follows the Cisco Hierarchical Enterprise Model.

##### Core Layer

Responsibilities:

High-speed forwarding
Inter-site connectivity
Backbone routing

##### Distribution Layer

Responsibilities:

Policy enforcement
Inter-VLAN routing
Route summarization

##### Access Layer

Responsibilities:

End-user connectivity
VLAN assignment
Port security
Security Architecture

##### Security controls include:

SSH-only device administration
Dedicated Management VLAN
VLAN segmentation
Password protection
Encrypted credentials

##### Future controls may include:

ACLs
VPN services
IDS/IPS integration
Network Access Control
Routing Strategy

The enterprise uses OSPF as the dynamic routing protocol.

Benefits:

Fast convergence
Scalability
Open standard
Efficient route propagation

Single-area OSPF is deployed in Version 1.0.

##### VLAN Strategy

The network is segmented into:

User VLAN
Server VLAN
Management VLAN

##### Segmentation improves:

Security
Broadcast containment
Network performance
High-Level Topology

HQ serves as the central site.

Branches connect to HQ through routed WAN links.

                 HQ
                  |
     -------------------------
     |           |           |
   Accra      Kumasi     Takoradi
#### Risks

Key risks include:

Routing misconfiguration
VLAN assignment errors
Device failure
Unauthorized access
WAN outages

Risk mitigation measures are documented in the Risk Register.

#### Success Criteria

 The project is considered successful when:

All sites communicate successfully.
OSPF converges correctly.
VLAN segmentation functions as intended.
SSH management is operational.
Testing objectives are achieved.
Future Expansion

#### Future phases may introduce:

Dual WAN links
HSRP
IPv6
ACL policies
VPN services
Zero Trust segmentation
