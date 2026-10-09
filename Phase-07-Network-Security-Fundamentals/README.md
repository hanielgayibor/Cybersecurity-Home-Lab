# Phase 7 — Network Security Fundamentals

## Objective
Learn core network security concepts and understand how firewalls and filtering affect connectivity and scan results.

## Lab Environment
- Ubuntu and Windows virtual machines
- Isolated home lab network
- Tools: operating-system networking utilities and Nmap, where appropriate

## Topics Covered
- Firewalls and traffic filtering
- Ports and network services
- TCP connection behavior
- Least privilege
- Basic network exposure review
- Interpreting filtered ports

## Activities
- Review the network settings on both VMs.
- Identify which services are intended to be reachable in the lab.
- Compare connectivity tests with authorized Nmap results.
- Review firewall settings without disabling protections unnecessarily.

## Analysis and Findings
- During earlier lab work, a scan result was described as filtered, with service/version information unavailable.
- A filtered port commonly means a firewall or network obstacle prevented Nmap from determining whether the port was open or closed.
- This behavior is consistent with traffic filtering, but the precise firewall rule or cause was not confirmed.
- A missing service/version result does not by itself prove that a service is absent or vulnerable.

## What I Learned
Network security depends on controlling which connections are permitted, not just whether a device is online. Firewalls can intentionally limit visibility and access.

## Cybersecurity Relevance
Understanding firewall behavior helps analysts interpret scan results, investigate connectivity issues, and reduce unnecessary network exposure.

## Next Phase
**Phase 8 — Wireshark & Packet Analysis**

## Safety and Authorization
Perform checks only on my own lab systems or systems I have explicit permission to test. Keep firewall protections enabled unless a controlled, authorized test requires a specific change.
