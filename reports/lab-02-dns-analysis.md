# Lab 02 — DNS Analysis and Packet Inspection

## 1. Objective

The objective of this lab was to observe and analyse DNS traffic generated from a Windows 10 virtual machine using Wireshark. The lab focused on understanding how domain names are resolved into IP addresses before communication occurs.

---

## 2. Environment

The lab environment consisted of:

- Windows 10 Virtual Machine
- Wireshark packet analyser
- Internet connectivity for external DNS resolution

Tools used:
- Wireshark
- nslookup
- ping

<img width="971" height="720" alt="02-dns-query-response-wireshark" src="https://github.com/user-attachments/assets/0ce98480-612e-4fe3-833c-50e8be74206c" />


Domains tested:
- bbc.co.uk
- google.com


<img width="976" height="549" alt="02_dns_query_response_capture" src="https://github.com/user-attachments/assets/6980c988-f613-488a-8c0a-36893928c3cd" />


---

## 3. Methodology

Wireshark was configured to capture traffic on the active network interface of the Windows 10 virtual machine.

DNS traffic was filtered using:

`dns`

and

`udp.port == 53`

<img width="1756" height="870" alt="02_nslookup_bbc_co_uk_output" src="https://github.com/user-attachments/assets/5a97d9d9-1891-4c54-aa0b-e8f3e119a71c" />

## ICMP Connectivity Test

<img width="972" height="654" alt="Screenshot 2026-05-14 141608" src="https://github.com/user-attachments/assets/2f2ab81d-272b-4f3a-bfec-48e6e3067d73" />


The following commands were used to generate DNS traffic:

```powershell
nslookup bbc.co.uk
ping google.com




