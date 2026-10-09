# Phase 4 — Wireshark & Packet Analysis

## Objective

Learn how to capture and analyze network traffic using Wireshark. This phase focuses on understanding how devices communicate and how packet analysis can help with network troubleshooting and security monitoring.

## Lab Environment

* **Host Machine:** MacBook with Apple M1
* **Virtual Machines:** Ubuntu and Windows
* **Tool:** Wireshark
* **Network:** Home lab virtual network

## Topics Covered

* Network packet capture
* Network interfaces
* Source and destination IP addresses
* MAC addresses
* TCP and UDP
* DNS queries
* HTTP traffic
* Wireshark display filters
* Packet details and protocol analysis

## Activities and Commands

### 1. Identify Network Interfaces

On Ubuntu, use:

```bash
ip addr
```

This displays network interfaces and their assigned IP addresses. Identify the interface connected to the lab network before capturing traffic.

### 2. Start a Packet Capture

1. Open Wireshark.
2. Select the correct network interface.
3. Start capturing packets.
4. Generate traffic in the lab, such as pinging another lab VM or performing a DNS lookup.
5. Stop the capture after collecting enough traffic to analyze.

Only capture traffic from systems and networks you own or have permission to monitor.

### 3. Generate Test Network Traffic

Example ping command:

```bash
ping -c 4 192.168.56.3
```

Replace the example address with the actual IP address of my Windows lab VM. This sends four ping requests on Linux and can generate packets to inspect in Wireshark.

### 4. Use Display Filters

Examples of Wireshark display filters:

```text
dns
```

Shows DNS packets.

```text
icmp
```

Shows ICMP traffic, including typical ping packets.

```text
tcp
```

Shows TCP packets.

```text
ip.addr == 192.168.56.3
```

Shows IPv4 packets with the specified address as either the source or destination.

```text
http
```

Shows packets Wireshark identifies as HTTP traffic, if any are present in the capture.

### 5. Inspect Packet Details

Select a packet and examine its protocol layers. Depending on the packet, useful fields include:

* Source and destination addresses
* Protocol type
* TCP or UDP source and destination ports
* Packet length
* TCP flags
* DNS query names and responses, when present

## Analysis and Findings

Complete this section using observations from my own capture.

* **Interface captured:** [enx080027c4221d]
* **Packets captured:** [Packet count was not recorded.]
* **Protocols observed:** [ICMP, TCP, DNS, and HTTP are relevant protocols for this lab.]
* **Source and destination IPs:** [The lab has used 192.168.56.2 for Ubuntu and 192.168.56.3 as the expected Windows VM address.]
* **Display filters tested:** [Filters such as dns, icmp, tcp, and ip.addr == 192.168.56.3 were used]
* **Interesting observation:** [Wireshark allows network communication to be examined packet by packet. Filters make it easier to
focus on particular protocols or IP addresses instead of reviewing all captured traffic.]
* **Troubleshooting notes:** [During setup, network connectivity and interface selection required troubleshooting. A successful
  ping does not guarantee that the correct interface is being captured or that matching packets will appear in Wireshark.]

## What I Learned

This phase demonstrates how Wireshark can make network communication visible by breaking traffic into individual packets and showing their protocol details. Display filters help narrow down large captures to the traffic relevant to a particular question.

Packet captures can help troubleshoot connectivity problems and investigate unusual network activity, but findings must be interpreted in context.

## Cybersecurity Relevance

Packet analysis is useful in security operations, incident response, and network troubleshooting. Analysts can inspect traffic patterns, investigate DNS activity, and look for communication that may require further investigation.

Encrypted protocols may hide the contents of application data, even when packet metadata remains visible.

## Next Phase

**Phase 5 — Linux Networking**

## Safety and Privacy

Capture only authorized lab traffic. Packet captures may contain sensitive information, so do not publish raw captures or disclose passwords, session tokens, private messages, or other confidential data in this repository.
