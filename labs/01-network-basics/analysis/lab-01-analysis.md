# Lab 01 — Network Fundamentals (Analysis)

## 1. Layer 2 Behaviour (Switching)

In this lab, the switch operated at Layer 2 of the OSI model. When PC1 communicated with PC2, the switch forwarded frames based on MAC address learning.

Initially, the switch did not know which port each device was connected to. After the first communication attempt, it built a MAC address table by associating each device’s MAC address with the correct switch port.

This allowed subsequent traffic to be forwarded directly to the correct device instead of being broadcast to all ports.

---

## 2. ICMP Communication (Ping)

The ping test used ICMP (Internet Control Message Protocol) to verify connectivity between the two devices.

The process observed:

- PC1 sent an ICMP Echo Request to PC2
- PC2 responded with an ICMP Echo Reply

This confirmed that:
- IP configuration was correct
- Both devices were reachable within the same subnet
- No routing was required for communication

---

## 3. Subnet Behaviour

Both devices were configured within the same subnet (192.168.1.0/24). Because of this, communication occurred directly at Layer 2 without the need for a default gateway or router involvement.

This demonstrates a key networking principle:
> Devices within the same subnet communicate directly using MAC addressing, not routing.

---

## 4. Router Interface Observation

The router interface was initially in an administratively down state. This required manual activation using the `no shutdown` command.

Although the router was not required for communication in this lab, this highlights an important real-world concept:
> Network interfaces are disabled by default for security and must be explicitly enabled.

---

## 5. Key Learning Outcomes

- Understood how switches learn MAC addresses dynamically
- Observed ICMP request/response behaviour in a LAN
- Confirmed direct communication within a single subnet
- Recognised the role of administrative interface states on routers
- Gained understanding of Layer 2 vs Layer 3 responsibilities

---

## 6. Conclusion

This lab demonstrated the fundamentals of LAN communication. It showed how devices interact within a single subnet, how switches manage traffic at Layer 2, and how ICMP can be used to verify connectivity between hosts.
