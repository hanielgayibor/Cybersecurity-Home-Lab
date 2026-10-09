# Phase 5 — Linux Networking

## Objective

Learn how to inspect and troubleshoot network settings in Linux using command-line tools. This phase focuses on network interfaces, IP addresses, routing tables, connectivity testing, and DNS resolution.

## Lab Environment

* **Host Machine:** MacBook with Apple M1
* **Virtual Machine:** Ubuntu Linux
* **Network Interface:** `enp0s8`
* **Lab IP address previously reported:** `192.168.56.2`
* **Tools:** Linux terminal and networking utilities

## Topics Covered

* Linux network interfaces
* IPv4 addresses and subnet masks
* MAC addresses
* Default gateways and routing tables
* Ping and connectivity testing
* DNS resolution
* Network troubleshooting

## Commands and Activities

### 1. Inspect Network Interfaces

```bash
ip addr
```

Displays network interfaces, IP addresses, and interface states.

### 2. View the Routing Table

```bash
ip route
```

Shows available routes and the default gateway, if configured.

### 3. Test Connectivity

```bash
ping -c 4 192.168.56.3
```

Sends four ICMP echo requests to the example Windows VM address. Confirm the actual target IP before running the command.

### 4. Check DNS Resolution

```bash
nslookup www.google.com
```

Queries DNS to find address records for a domain. The result depends on DNS connectivity and configuration.

### 5. Inspect Listening and Network Sockets

```bash
ss -tuln
```

Displays listening TCP and UDP sockets and their associated port numbers. This can help identify services listening on the Linux machine.

## Analysis and Findings

* **Network interface:** `enp0s8` appeared in the Ubuntu networking setup.
* **IP addressing:** The lab used `192.168.56.2` as the Ubuntu address. Another address, `10.0.3.2`, was also reported during troubleshooting, indicating that more than one network interface or network configuration may have been involved.
* **Routing:** The `ip route` command can be used to identify the active routes and default gateway. The exact route output was 192.168.56.0/24.
* **Connectivity testing:** An earlier ping test reported four packets transmitted, zero received, and 100% packet loss. 
* **DNS resolution:** DNS testing can help determine whether a domain name resolves to an IP address. 
* **Troubleshooting lesson:** A VM may have multiple network interfaces, and each can serve a different purpose. The correct interface, IP address, and route must be identified before diagnosing connectivity problems.

## What I Learned

Linux networking commands provide a practical way to understand how a computer connects to a network. `ip addr` shows interface configuration, `ip route` explains how traffic is routed, and `ping` tests reachability. DNS tools help investigate name resolution, while `ss` shows listening network sockets.

When a connection fails, checking the interface, IP address, routing table, and destination helps narrow down the cause.

## Cybersecurity Relevance

Cybersecurity analysts use Linux networking tools to investigate connectivity issues, understand network configurations, identify listening services, and support incident investigations. Knowing how a system is connected makes it easier to recognize unexpected settings and troubleshoot security problems.

## Next Phase

**Phase 6 — Windows Networking**

## Safety and Authorization

All connectivity tests should be limited to systems and networks I own or have permission to test. Do not publish sensitive configuration details, credentials, or private network data in this repository.
