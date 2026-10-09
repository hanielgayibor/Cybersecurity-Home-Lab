# Phase 9 — Advanced Networking

## Objective
Build a deeper understanding of network addressing, routes, connectivity, and how traffic moves between systems.

## Lab Environment
- Ubuntu and Windows virtual machines
- Virtual home lab network
- Tools: `ip`, `ping`, `traceroute` or `tracepath`, and DNS utilities

## Topics Covered
- Routing tables
- Gateways and network paths
- DNS resolution
- Latency and packet loss
- Private IPv4 addressing
- Differences between local and external destinations

## Commands and Activities
```bash
ip addr
ip route
ping -c 4 192.168.56.3
traceroute www.google.com
nslookup www.google.com
```
If `traceroute` is not installed, use an available equivalent or document the installation issue. Confirm the target address before testing the Windows VM.

## Analysis and Findings
- The lab troubleshooting notes included both `192.168.56.2` and `10.0.3.2`, suggesting that more than one network interface or network configuration was present.
- Multiple VM interfaces can connect a guest to different virtual networks, so the interface and route used for each test matter.
- Earlier connectivity troubleshooting included packet loss before connectivity later worked.
- Exact traceroute hops and route-table output were not recorded, so this README does not claim a particular network path or latency result.

## What I Learned
A device can have more than one IP address and route. Understanding which interface and gateway are used is important when diagnosing communication between virtual machines or to the internet.

## Cybersecurity Relevance
Routing knowledge supports network troubleshooting, segmentation reviews, and understanding how an attacker or analyst might reach systems across network boundaries.

## Next Phase
**Phase 10 — Security Fundamentals**

## Safety and Authorization
Use only authorized destinations. Avoid scanning or probing public systems beyond ordinary permitted connectivity tests.
