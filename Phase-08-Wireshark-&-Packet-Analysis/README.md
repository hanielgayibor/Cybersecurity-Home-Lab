# Phase 8 — Wireshark & Packet Analysis

## Objective
Capture and examine packets to understand how network traffic appears during communication between lab systems.

## Lab Environment
- Ubuntu VM: previously reported address `192.168.56.2`
- Windows VM: expected address `192.168.56.3`; verify before use
- Ubuntu interface observed during setup: `enp0s8`
- Tool: Wireshark

## Topics Covered
- Selecting the correct capture interface
- Generating test traffic
- Packet lists and packet details
- Display filters
- ICMP, TCP, DNS, and HTTP concepts
- Troubleshooting empty captures

## Activities
Example test traffic:
```bash
ping -c 4 192.168.56.3
```
Example display filters:
```text
icmp
dns
tcp
ip.addr == 192.168.56.3
```
Use the actual target IP and only list filters as tested if they were actually used.

## Analysis and Findings
- The Ubuntu VM's `enp0s8` interface appeared during setup.
- Network connectivity and interface selection required troubleshooting.
- An earlier ping test reported four packets transmitted, zero received, and 100% packet loss; connectivity later began working, but the exact cause was not confirmed.
- At one point, no packets appeared in Wireshark. This can happen when the wrong interface is selected, no matching traffic is generated, or the capture filter/interface configuration is unsuitable.
- The total packet count and final list of observed protocols were not recorded.

## What I Learned
Packet analysis depends on capturing traffic on the interface that actually carries it. Display filters help narrow a capture to relevant traffic, but a filter cannot display packets that were never captured.

## Cybersecurity Relevance
Wireshark is useful for network troubleshooting, protocol analysis, and investigating potentially suspicious communications.

## Next Phase
**Phase 9 — Advanced Networking**

## Safety and Privacy
Capture only authorized lab traffic. Do not publish raw packet captures that may contain credentials, tokens, private messages, or other sensitive information.
