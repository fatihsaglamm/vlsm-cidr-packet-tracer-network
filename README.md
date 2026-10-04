# 🌐 VLSM & CIDR Network Design in Cisco Packet Tracer

A computer networking project focused on designing and implementing an IPv4 network using **VLSM**, **CIDR**, **RIPv2**, and Cisco Packet Tracer.

The project demonstrates efficient IP address allocation, subnet planning, router configuration, routing, and end-to-end connectivity between multiple organizational departments.

## 📌 About the Project

The main goal of this project is to design a scalable network by efficiently dividing an available IPv4 address space among multiple workgroups.

The implementation includes:

- Variable Length Subnet Masking (VLSM)
- Classless Inter-Domain Routing (CIDR)
- Supernetting
- IPv4 address planning
- Router configuration
- Serial interface addressing
- RIPv2 dynamic routing
- Default gateway configuration
- End-to-end connectivity testing

## 🏢 Network Scenario

The network represents an organization with multiple departments.

The departments include:

- Administration
- Classrooms
- Labs
- Student Accommodation
- Staff

Each department contains multiple workgroups with different host requirements.

The network is designed so that each workgroup receives an appropriately sized subnet.

## 🧮 VLSM

Variable Length Subnet Masking is used to allocate different subnet sizes depending on the number of hosts required by each workgroup.

This helps reduce unnecessary IP address waste compared with using the same subnet mask for every network.

The subnet design considers:

```text
Network Address
Subnet Mask
Usable Host Range
Broadcast Address
Router Interface Address
```

## 🌍 CIDR & Supernetting

CIDR is used to organize the available address space efficiently.

The project also considers route aggregation so that the organization can advertise a summarized network instead of multiple individual subnet routes.

This improves:

- Routing efficiency
- Address utilization
- Network scalability
- Routing table organization

## 🖧 Router Configuration

Routers connect the different departmental networks.

Configuration includes:

- IPv4 addresses
- Subnet masks
- FastEthernet interfaces
- Serial interfaces
- Interface activation
- Dynamic routing

## 🔄 RIPv2 Routing

The project uses **RIPv2** to support VLSM.

Example configuration:

```text
Router> enable
Router# configure terminal
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# no auto-summary
Router(config-router)# network <network-address>
Router(config-router)# end
```

Using:

```text
version 2
no auto-summary
```

allows routing updates to correctly support variable-length subnet masks.

## 🖥️ Default Gateways

Each host is configured with an appropriate default gateway corresponding to the router interface in its subnet.

Correct gateway configuration allows hosts to communicate with devices located in other networks.

## ✅ Connectivity Testing

The final implementation is tested using `ping`.

Tests include communication between:

```text
Host → Default Gateway
Host → Host in another subnet
Host → Host behind another router
```

The goal is to verify that all networks are correctly configured and reachable.

## 🛠 Technologies & Concepts

- Cisco Packet Tracer
- IPv4
- VLSM
- CIDR
- Supernetting
- Subnetting
- RIPv2
- Dynamic Routing
- Router CLI
- FastEthernet
- Serial Interfaces
- Default Gateways
- ICMP / Ping
- Network Address Planning

## 📂 Project Structure

```text
vlsm-cidr-packet-tracer-network/
│
├── network/
│   └── vlsm-cidr-network.pkt
│
├── screenshots/
│   └── network-topology.png
│
└── README.md
```

> The `screenshots` folder is optional but recommended because GitHub cannot preview Cisco Packet Tracer `.pkt` files directly.

## ▶️ Opening the Project

1. Install Cisco Packet Tracer.
2. Clone or download this repository.
3. Open:

```text
network/vlsm-cidr-network.pkt
```

4. Inspect the router and host configurations.
5. Use the Packet Tracer CLI or simulation tools to test connectivity.

## 🎯 Project Goals

The main goals of this project are to:

- Design an IPv4 addressing plan
- Apply VLSM to networks with different host requirements
- Use CIDR and supernetting concepts
- Configure router interfaces
- Configure RIPv2 routing
- Configure correct default gateways
- Minimize IP address waste
- Ensure successful communication between all hosts

## 🎓 Course Project

Developed as part of:

**CNG436 - Wireless Communication and Networks**

Middle East Technical University, Northern Cyprus Campus.

## 👤 Author

Fatih Sağlam