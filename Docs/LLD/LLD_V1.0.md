### Low-Level Design (LLD) v1.0

Project Title

#### RC-001: Hierarchical Enterprise Network Design and Implementation

#### Network Devices
Headquarters

Device    	Function
HQ-R1 -- Core Router
HQ-SW1 --	Distribution Switch
HQ-SW2	--  Access Switch
SRV-1	--  Application Server

Accra Branch
Device	   Function
ACC-R1 -- 	Branch Router
ACC-SW1	--  Access Switch

Kumasi Branch
Device	   Function
KUM-R1 -- 	Branch Router
KUM-SW1 --	Access Switch

Takoradi Branch
Device  	Function
TAK-R1	--  Branch Router
TAK-SW1	--  Access Switch
#####  VLAN Design
VLAN	  Name	Subnet

10	--  Users	192.168.10.0/24
20	--  Servers	192.168.20.0/24
99	--  Management	192.168.99.0/24

Branch Addressing
Accra
192.168.30.0/24

Gateway:

192.168.30.1
Kumasi
192.168.40.0/24

Gateway:

192.168.40.1
Takoradi
192.168.50.0/24

Gateway:

192.168.50.1
WAN Addressing
Link	Subnet
HQ-Accra	10.0.0.0/30
HQ-Kumasi	10.0.0.4/30
HQ-Takoradi	10.0.0.8/30
OSPF Design

Process ID:

1

Area:

0

Participating Devices:

HQ-R1
ACC-R1
KUM-R1
TAK-R1
SSH Design

SSH Version:

2

Requirements:

Local authentication
RSA keys
Secure VTY access

Example Username:

admin
Switch Management

Management VLAN:

VLAN 99

Switch management addresses:

Device	Address
HQ-SW1	192.168.99.11
HQ-SW2	192.168.99.12
ACC-SW1	192.168.99.21
KUM-SW1	192.168.99.31
TAK-SW1	192.168.99.41
Validation Tests
Test 1

Verify OSPF neighbor establishment.

Expected Result:

FULL state
Test 2

Verify branch-to-HQ connectivity.

Expected Result:

Successful ping
Test 3

Verify inter-VLAN routing.

Expected Result:

Successful communication
Test 4

Verify SSH access.

Expected Result:

Successful remote login
Configuration Standards

Naming Convention:

SITE-ROLE-NUMBER

Examples:

HQ-R1
ACC-SW1
KUM-R1
TAK-SW1
Version History
Version	Date	Description
1.0	July 2026	Initial Design
