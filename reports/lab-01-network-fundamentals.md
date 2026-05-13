# Lab 01 — Network Fundamentals

## 1. Objective
Understand basic LAN communication using IPv4 addressing and verify device connectivity using ICMP (ping).

---

## 2. Network Setup
Two PCs were connected via a switch within a single subnet (192.168.1.0/24). No routing was required as all devices existed within the same broadcast domain.

**Key configuration:**
- PC1: 192.168.1.10
- PC2: 192.168.1.20

---

## 3. Methodology
Devices were configured manually using static IP addressing. Connectivity was tested using ICMP echo requests from PC1 to PC2.

Packet analysis was observed to confirm successful transmission and response.

---

## 4. Evidence

### Topology
<img width="720" height="508" alt="topology-overview" src="https://github.com/user-attachments/assets/313d0cc3-ca4e-438c-bd1c-6dfb937936e4" />


### IP Configuration
<img width="692" height="708" alt="pc1-ip-config" src="https://github.com/user-attachments/assets/3136cd2c-481d-400f-9877-376e6194966b" />
<img width="695" height="700" alt="pc2-ip-config" src="https://github.com/user-attachments/assets/126ac5d4-931b-44ad-a8cc-244982191664" />



### Ping Test
<img width="692" height="674" alt="ping-success" src="https://github.com/user-attachments/assets/634f12e6-6ea4-4938-90a2-03363e285934" />



### Router interface status
<img width="695" height="703" alt="router-interface-status" src="https://github.com/user-attachments/assets/becab077-c29c-4548-83d6-a554622403ef" />



---

## 5. Technical Observations
- ICMP Echo Requests were successfully transmitted and received.
- Switch behaviour allowed Layer 2 frame forwarding based on MAC address learning.
- Communication occurred without the need for a router due to shared subnet.

---

## 6. Issue Encountered
The router interface initially appeared inactive due to administrative shutdown state. This was resolved using the `no shutdown` command in global configuration mode.

---

## 7. Conclusion
The lab successfully demonstrated basic IPv4 communication within a LAN environment. Devices were able to communicate directly within the same subnet, confirming correct IP configuration and Layer 2 switching behaviour.
