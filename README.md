# Cisco-Packet-Tracer-project-03-Inter-VLAN-Routing-Lab-Router-on-a-Stick-with-VLAN-10-VLAN-20

I’m excited to share a fundamental networking project – an inter‑VLAN routing lab built in Cisco Packet Tracer. The topology is simple but powerful: one router (Router0), one Layer 2 switch (2960‑24T), and two PCs (PC0 and PC1) placed in VLAN 10 and VLAN 20 respectively.

![image alt](https://github.com/Sameera54321/Cisco-Packet-Tracer-project-03-Inter-VLAN-Routing-Lab-Router-on-a-Stick-with-VLAN-10-VLAN-20/blob/main/16.jpg?raw=true)

## 📌 Summary

Inter‑VLAN Routing Lab is a Cisco Packet Tracer simulation that demonstrates router‑on‑a‑stick – a method of routing between VLANs using a single router interface. The topology includes:

    1 router – Cisco 2911 or similar (Router0)

    1 switch – Cisco 2960‑24T (Switch1)

    2 PCs – PC0 (VLAN 10), PC1 (VLAN 20)

### VLAN & IP assignment :

| VLAN | Subnet | Gateway (Router subinterface) | PC IP |
| :--- | :--- | :--- | :--- |
| 10 | 192.168.10.0/24 | 192.168.10.1 | 192.168.10.10 |
| 20 | 192.168.20.0/24 | 192.168.20.1 | 192.168.20.10 |

### Key configurations:

    On Switch1:

        Create VLANs 10 and 20

        Assign access ports: PC0 to VLAN 10, PC1 to VLAN 20

        Configure the port connected to Router0 as a trunk (switchport mode trunk)

    On Router0:

        Create subinterfaces G0/0.10 and G0/0.20

        Enable encapsulation dot1Q 10 and dot1Q 20

        Assign IP addresses as gateways for each VLAN

        No ip routing needed – subinterfaces are directly connected

### Verification:
ping 192.168.20.10 from PC0 should succeed after correct configuration.

## ✨ Features

    ✅ 1 router – router‑on‑a‑stick with subinterfaces

    ✅ 1 Layer 2 switch – VLAN access ports and trunk

    ✅ Two VLANs (10, 20) – logical network segmentation

    ✅ Two PCs – end devices in different VLANs

    ✅ Inter‑VLAN routing – communication across VLANs

    ✅ Full Packet Tracer file (.pkt) – ready to open and practice

    ✅ Documentation – VLAN mapping, trunk config, subinterface configs

## 🛠️ Built With

    Cisco Packet Tracer – version 8.x

    CLI – router and switch configurations

## 🤝 Contributing

Contributions are welcome! To extend this lab:

    Fork the repository.

    Add more VLANs (e.g., VLAN 30) and an extra PC.

    Replace the router with a multilayer switch (SVI routing).

    Add a DHCP server to assign IPs automatically.

    Implement access control lists (ACLs) between VLANs.

    Open a pull request with a clear description.
