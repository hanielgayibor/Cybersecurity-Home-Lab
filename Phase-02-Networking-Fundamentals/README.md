# Phase 2 — Networking Fundamentals

## Objective

This phase focused on learning the fundamentals of computer networking and how devices communicate over a network. These concepts provide the foundation for network security, packet analysis, vulnerability assessment, and penetration testing.

## Lab Environment

* **Host computer:** Apple Mac with M1 chip
* **Linux system:** Ubuntu virtual machine
* **Windows system:** Windows virtual machine
* **Lab network:** Virtual network used for authorized exercises

## Topics Covered

* IP addresses and network interfaces
* Private and public IP addresses
* MAC addresses
* Default gateways
* Subnet masks
* TCP and UDP
* DNS (Domain Name System)
* HTTP and HTTPS
* Ports and protocols
* Routers and switches
* Ping and basic connectivity troubleshooting
* The role of networking in cybersecurity

## Networking Commands

The following commands can be used to inspect network configuration and test connectivity.

| Command                     | Purpose                                                               |
| --------------------------- | --------------------------------------------------------------------- |
| `ip addr`                   | Displays Linux network interfaces and IP addresses                    |
| `ip route`                  | Displays Linux routing information                                    |
| `ping -c 4 192.168.56.3`    | Sends four ICMP echo requests to a lab target                         |
| `ifconfig`                  | Displays network interface information when the utility is installed  |
| `traceroute www.google.com` | Traces a network path when traceroute is installed                    |
| `nslookup www.google.com`   | Queries DNS information                                               |
| `netstat -an`               | Displays network connections and listening ports on supported systems |

## Key Concepts

### IP Address

An IP address identifies a device's network interface and helps route traffic to the correct destination.

### MAC Address

A MAC address identifies a network interface at the data-link layer. It is commonly used for communication within a local network.

### Default Gateway

A default gateway forwards traffic from a local network toward other networks when no more specific route applies.

### TCP and UDP

TCP provides a connection-oriented transport service with reliable, ordered delivery. UDP provides a connectionless transport service without TCP's delivery guarantees.

### DNS

The Domain Name System translates domain names, such as `www.google.com`, into IP addresses and other DNS records.

### Ports

Ports help a computer direct network traffic to the appropriate application or service. Examples include TCP port 443 for HTTPS and TCP port 22 for SSH.

## Why Networking Matters in Cybersecurity

Cybersecurity professionals use networking knowledge to understand traffic, investigate suspicious connections, identify exposed services, troubleshoot connectivity problems, and evaluate network security controls.

Understanding IP addresses, ports, protocols, and routing also makes it easier to interpret Nmap scan results and analyze packets in Wireshark.

## Lessons Learned

This phase introduced the core concepts needed to understand how computers communicate. Networking fundamentals matter because many cybersecurity tasks involve identifying devices, understanding connections, analyzing protocols, and tracing how information moves between systems.

## Next Steps

The next phase focuses on network scanning with Nmap, including discovering hosts and identifying open ports in an authorized lab environment.

## Lab Safety

Network scanning and testing in this project are restricted to systems I own or have explicit permission to test.
