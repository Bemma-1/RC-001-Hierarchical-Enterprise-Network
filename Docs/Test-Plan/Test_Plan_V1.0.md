# Test Plan v1.0

## Project

RC-001: Hierarchical Enterprise Network Design and Implementation

## Purpose

This document defines the testing procedures used to validate the functionality, security, and operational requirements of the enterprise network.

---

# Test Objectives

The testing process shall verify:

* Layer 3 connectivity
* OSPF functionality
* Inter-VLAN routing
* Branch connectivity
* SSH administration
* Server accessibility

---

# Test Environment

## Platform

Cisco Packet Tracer 8.2.2

## Devices

* HQ-R1
* HQ-SW1
* HQ-SW2
* ACC-R1
* ACC-SW1
* KUM-R1
* KUM-SW1
* TAK-R1
* TAK-SW1

---

# Test Cases

## TC-001: OSPF Neighbor Establishment

### Objective

Verify successful OSPF adjacency formation.

### Procedure

1. Access routers.
2. Execute:

```bash
show ip ospf neighbor
```

### Expected Result

All neighboring routers reach FULL state.

### Status

Pass / Fail

---

## TC-002: Routing Table Verification

### Objective

Verify OSPF route propagation.

### Procedure

Execute:

```bash
show ip route
```

### Expected Result

Remote branch networks appear in routing table.

### Status

Pass / Fail

---

## TC-003: Inter-VLAN Routing

### Objective

Verify communication between VLANs.

### Procedure

Ping between VLAN gateways and hosts.

### Expected Result

Successful connectivity.

### Status

Pass / Fail

---

## TC-004: Branch-to-HQ Connectivity

### Objective

Verify WAN connectivity.

### Procedure

Ping HQ resources from each branch.

### Expected Result

Successful replies.

### Status

Pass / Fail

---

## TC-005: SSH Access

### Objective

Verify secure remote administration.

### Procedure

Initiate SSH session.

### Expected Result

Successful authentication.

### Status

Pass / Fail

---

## TC-006: Server Reachability

### Objective

Verify access to enterprise servers.

### Procedure

Ping server from authorized networks.

### Expected Result

Server reachable.

### Status

Pass / Fail

---

# Acceptance Criteria

The network shall be accepted when:

* All OSPF neighbors reach FULL state.
* All routing tests pass.
* All VLAN tests pass.
* SSH access functions correctly.
* End-to-end communication succeeds.

---

# Test Evidence

Evidence shall include:

* Screenshots
* Routing tables
* OSPF neighbor tables
* SSH login verification
* Ping results

---

# Version History

| Version | Date      | Description     |
| ------- | --------- | --------------- |
| 1.0     | July 2026 | Initial release |
