# Phase 3 — Network Scanning with Nmap

## Objective

Learn how to use Nmap (Network Mapper) to discover devices on a network, identify open ports, and investigate the services running on a target system.

## Lab Environment

* **Host Machine:** MacBook with Apple M1
* **Virtual Machines:** Ubuntu and Windows
* **Target:** My own Windows virtual machine on my isolated home lab network
* **Tool:** Nmap

> **Note:** Confirm the target machine's IP address before scanning. The commands below are examples; only record commands as completed after running them.

## Topics Covered

* Introduction to Nmap
* Host discovery
* IP addresses and target identification
* TCP ports and port states
* Open, closed, and filtered ports
* Service and version detection
* Interpreting scan results
* Safe and authorized network scanning

## Commands

### 1. Check the Nmap Installation

```bash
nmap --version
```

Displays the installed Nmap version and confirms whether the command is available.

### 2. Discover Hosts on the Lab Network

```bash
nmap -sn 192.168.56.0/24
```

Performs host discovery without a port scan. Use this command only if `192.168.56.0/24` is confirmed to be my isolated lab subnet.

### 3. Scan the Windows Virtual Machine

```bash
nmap 192.168.56.3
```

Scans the target's most common TCP ports. Replace the example IP address if the Windows VM uses a different address.

### 4. Identify Services and Versions

```bash
nmap -sV 192.168.56.3
```

Attempts to identify the services and software versions associated with discovered ports.

## Understanding the Results

| Port State | Meaning                                                                                                 |
| ---------- | ------------------------------------------------------------------------------------------------------- |
| Open       | A service is accepting connections on the port.                                                         |
| Closed     | The target is reachable, but no service is listening on that port.                                      |
| Filtered   | A firewall or other network obstacle prevents Nmap from determining whether the port is open or closed. |

Nmap results can help identify services that need to be reviewed or secured. A port being open does not automatically mean that the system is vulnerable.

## Findings and Results

Complete this section after running the scans.

* **Target IP address:** [192.168.56.3]
* **Host discovery result:** [I recorded ports 20,80,445]
* **Open ports found:** [20/TDP, 80/TDP, 445/TDP]
* **Services identified:** [Port 20 - ftp/data, Port 80 - http, Port 445 - microsoft/ds]
* **Filtered ports or unexpected results:** [All the ports observed were filtered, meaning Windows Firewall was blocking them.]
* **Troubleshooting notes:** [Was able to identify both the state and service of the Port.]

## What I Learned

This phase introduces network scanning and shows how Nmap can help identify active hosts, open ports, and services. Understanding these results is useful for network inventory, troubleshooting, and security assessments.

The results must be interpreted in context because firewalls, network configuration, and the scan method can affect what Nmap detects.

## Cybersecurity Relevance

Network scanning is a useful skill for cybersecurity analysts, penetration testers, and system administrators. It can help teams understand which services are exposed and determine whether those services need further investigation or security improvements.

## Next Phase

**Phase 4 — Wireshark and Packet Analysis**

## Safety and Authorization

All scans must be limited to systems and networks I own or have explicit permission to test. This phase focuses on my isolated home lab environment.
