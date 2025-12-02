# 🚀 Enterprise-multi-VLAN-network
### 🌆Enterprise-grade multi-VLAN network (Router-on-L3 Switch Architecture)
------------------------------------------------------------------------------------------------------------

# 📄 Overview
### This project implements a full enterprise-level network using:
* **Multi-VLAN Segmentation**
* **Layer-3 Inter-VLAN Routing**
* **DHCP for all VLANs**
* **Access Control List (ACLs) for security**
* **Trunking between L3 Switch ⬅️➡️ Router**
* **Subnetting for department-wise segmentation**

**Network built in ***Cisco Packet Tracer*** .**

## 🧩VLAN Structure

|  VLAN   |    Department   |      Network      |    Gateway     |
|---------|-----------------|-------------------|----------------|
| 10      |    Admin        |  192.168.10.0/24  |  192.168.10.1  |
| 20      |    HR           |  192.168.20.0/24  |  192.168.20.1  |
| 30      |    IT           |  192.168.30.0/24  |  192.168.30.1  |
| 40      |    Guest        |  192.168.40.0/24  |  192.168.40.1  |

## 🏗️ Network Diagram
**Output**
* https://github.com/rXchauhan/Enterprise-multi-VLAN-network/blob/2ce66c0358c6b4a4dc4653517b3f7a5a9149d393/Images/topology.png

### 🪛 What I Configured

**✔️ L-3 Switch**

* VLAN creation
* Access ports
* Trunk ports(fa0/24)
* SVI interfaces with helper-address
* ACL for HR & Guest isolation
* ip routing enabled

**Switch Configuration here ⬇️**

https://github.com/rXchauhan/Enterprise-multi-VLAN-network/blob/64265abd155c1df8d36c0c499e65af8c7cc57952/Configs/L-3%20Switch.txt.txt


**✔️ Router**

* DHCP pools for each VLAN
* Static routes towards switch
* Point-to-point link 10.10.10.0/30

**Router Configuration here ⬇️**

https://github.com/rXchauhan/Enterprise-multi-VLAN-network/blob/b58e2c14e4c793fe1fba51992b59f106887fc24e/Configs/R1%20Router.txt.txt


## 🔐 Access Control List
### ACL 101 (Guest VLAN restrictions)
* Guest ➡️ Admin ❌
* Guest ➡️ HR ❌
* Guest ➡️ IT ❌
* Guest ➡️ Internet/Somewhere✔️

### ACL 102 (HR ➡️ IT restriction)
* HR cannot access IT VLAN ❌
* Everything else allowed ✔️

## Here are output of *before* and *after* ACL :-
**before ACL in VLAN-40 to VLAN-10, 20 & 30**
* *🎞️here⬇️*
* 

**After ACL in VLAN-40 to Vlan-10, 20 & 30**
* *🎞️ here⬇️*
* 

**ACL in VLAN-20 to VLAN-30**
* *🎞️ here ⬇️*
* 

## 🎯 Final Output Highlights
* Full inter-VLAN routing
* Department-wise segementation
* DHCP Automation
* Complete ACL-based access control
* Corporate-style topology and documentation
  
