# Lab 01 — Notes (Raw Learning)

## Commands Used

- ping 192.168.1.20 → tested connectivity between hosts
- ipconfig → checked Windows IP configuration
- ip a → checked Linux IP configuration
- show ip interface brief → checked router interface status

---

## Wireshark Filters (future reference)

- icmp → view ping traffic
- arp → view address resolution
- ip → view all IP traffic

---

## Mistakes / Issues Encountered

- Router interface was initially down due to "shutdown" state
- Resolved using `no shutdown` in CLI
- Needed to ensure both PCs were in the same subnet before ping worked

---

## Key Reminders

- Switch = Layer 2 (MAC addresses, not IP routing)
- Router interfaces are OFF by default
- Devices must be in same subnet for direct communication
- Ping uses ICMP, not TCP/UDP

---

## Quick Understanding Notes

- Subnet = defines local network boundary
- MAC address = used for local delivery inside LAN
- IP address = used for logical addressing
- ICMP = used for testing connectivity, not data transfer
