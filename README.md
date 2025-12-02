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


### 🪛 What I Configured

**✔️ L-3 Switch**

* VLAN creation
* Access ports
* Trunk ports(fa0/24)
* SVI interfaces with helper-address
* ACL for HR & Guest isolation
* ip routing enabled

(L-3 Sswitch config photo)


**✔️ Router**

* DHCP pools for each VLAN
* Static routes towards switch
* Point-to-point link 10.10.10.0/30

 (router config photo )



## 🔐 Access Control List
### ACL 101 (Guest VLAN restrictions)
* Guest ➡️ Admin ❌
* Guest ➡️ HR ❌
* Guest ➡️ IT ❌
* Guest ➡️ Internet/Somewhere✔️

### ACL 102 (HR ➡️ IT restriction)
* HR cannot access IT VLAN ❌
* Everything else allowed ✔️


## 🎯 Final Output Highlights
* Full inter-VLAN routing
* Department-wise segementation
* DHCP Automation
* Complete ACL-based access control
* Corporate-style topology and documentation
  
