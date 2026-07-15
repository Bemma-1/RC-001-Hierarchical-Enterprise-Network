### RC-001: Hierarchical Enterprise Network Design and Implementation
Project Overview

This project presents the design, implementation, and evaluation of a hierarchical enterprise network for a fictional organization with a Headquarters (HQ) and three branch offices located in Accra, Kumasi, and Takoradi.

The objective is to design a scalable, secure, and manageable network architecture that supports business operations while following industry best practices in enterprise networking. The project applies the principles of hierarchical network design, VLAN segmentation, dynamic routing, secure remote administration, and structured network testing.

The project was developed as part of a broader cybersecurity and networking research portfolio aimed at exploring enterprise network architecture, security controls, and resilient infrastructure design.

### Research Objectives:
Design a scalable hierarchical enterprise network architecture.
Implement logical network segmentation using VLANs.
Deploy dynamic routing using OSPF.
Secure network administration through SSH.
Isolate management traffic using a dedicated Management VLAN.
Evaluate network functionality through structured testing and validation.
Document architectural decisions and implementation outcomes.
Network Scope
Headquarters (HQ)

#### The headquarters serves as the core of the enterprise network and hosts:

Core routing infrastructure,
Distribution layer switching,
Server infrastructure,
Network management services,
User access networks,
Branch Offices

#### The following branch offices are connected through routed WAN links:

Accra Branch
Kumasi Branch
Takoradi Branch

#### Each branch includes:

User VLANs
Local switching infrastructure
WAN connectivity to HQ
Secure management access
Technologies Implemented
Technology	Purpose
VLANs	Network segmentation
OSPF	Dynamic routing
SSH	Secure device administration
Management VLAN	Infrastructure management
Cisco IOS	Device configuration
Packet Tracer	Network simulation
IPv4 Subnetting	Address management
Network Architecture

The design follows Cisco's three-tier hierarchical model:

Core Layer
Distribution Layer
Access Layer

This architecture improves:

Scalability
Fault isolation
Security
Network manageability
Project Deliverables
Documentation
High-Level Design (HLD)
Low-Level Design (LLD)
Architecture Decision Records (ADRs)
Risk Register
Test Plan
Research Journal
Technical Artifacts
Packet Tracer topology
Device configurations
Network diagrams
Validation results
Screenshots
Key Security Controls
SSH-only remote administration
VLAN-based segmentation
Dedicated management network
Access control through Layer 3 boundaries
Routing protocol containment
Testing and Validation

#### The network is evaluated using structured test cases that verify:

End-to-end connectivity
Inter-VLAN routing
OSPF convergence
SSH access
Branch-to-HQ communication
Server accessibility
Future Enhancements

#### Potential improvements include:

HSRP gateway redundancy
ACL-based traffic filtering
Site-to-site VPN deployment
Network monitoring with SNMP
Syslog integration
IPv6 implementation
Zero Trust segmentation
Author

Emmanuel Ampong

#### Research Interests:

Enterprise Networking
Cybersecurity
Network Automation
Secure Infrastructure Design
Threat Detection and Response

#### Repository Structure
docs/
diagrams/
packet-tracer/
configs/
screenshots/
experiments/
results/
references/
presentation/
