# Phase 6 — Windows Networking

## Objective
Understand Windows network configuration and practice basic connectivity troubleshooting.

## Lab Environment
- Windows virtual machine in my home lab
- Ubuntu virtual machine as a potential test peer
- Tools: Windows Command Prompt or PowerShell

## Topics Covered
- IP configuration
- Network adapters
- Default gateway and DNS servers
- Ping and name-resolution tests
- Windows network troubleshooting

## Commands and Activities
```powershell
ipconfig /all
route print
ping 192.168.56.2
nslookup www.google.com
netstat -ano
```
These commands display network configuration, routes, connectivity, DNS resolution, and active network connections. Replace example addresses with the verified IP addresses in the lab.

## Analysis and Findings
- Windows networking tools provide information similar to Linux tools, but use Windows-specific commands and output.
- `ipconfig /all` can show adapter addresses, gateways, and DNS configuration.
- `route print` can help explain how Windows chooses a route.
- `ping` and `nslookup` can help separate connectivity problems from DNS problems.
- Exact command output and the Windows VM's final IP address were not recorded in the available lab notes, so no specific Windows scan or connectivity result is claimed here.

## What I Learned
Comparing Windows and Linux network tools helps build cross-platform troubleshooting skills. Checking addressing, routing, and DNS in order makes it easier to narrow down common connection issues.

## Cybersecurity Relevance
Security analysts often investigate Windows endpoints, network connections, and unexpected listening services. Basic Windows networking knowledge supports help-desk work, endpoint troubleshooting, and incident response.

## Next Phase
**Phase 7 — Network Security Fundamentals**

## Safety and Authorization
Use these commands only on systems and networks I own or have permission to inspect. Do not publish credentials or sensitive system output.
