```md
# Lab 02 — DNS Packet Analysis

## 1. DNS Resolution Process

This lab demonstrated the process of DNS resolution using a Windows 10 virtual machine and Wireshark packet analysis.

When the `nslookup bbc.co.uk` command was executed, the system generated a DNS query requesting the IPv4 address associated with the domain name.

The DNS server then responded with an A record containing the resolved IP address required for communication.

This demonstrated how systems convert human-readable domain names into routable IP addresses.

---

## 2. DNS and UDP Behaviour

The captured traffic showed DNS communication occurring over UDP port 53.

UDP is commonly used for DNS because:
- low overhead improves performance
- no session establishment is required
- DNS queries are typically small and fast

This allows DNS resolution to occur efficiently before communication with remote hosts begins.

---

## 3. Relationship Between DNS and ICMP

The lab also demonstrated the relationship between DNS resolution and ICMP communication.

When executing:

```powershell
ping google.com
