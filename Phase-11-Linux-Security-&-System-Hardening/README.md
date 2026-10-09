# Phase 11 — Linux Security & System Hardening

## Objective
Learn basic ways to inspect and improve the security of an Ubuntu Linux system.

## Lab Environment
- Ubuntu virtual machine
- Linux terminal
- Tools: `whoami`, `id`, `sudo`, `ss`, and package-management utilities

## Topics Covered
- User and group permissions
- Least privilege
- Software updates
- Listening services
- File permissions
- Basic host hardening

## Commands and Activities
```bash
whoami
id
sudo apt update
ss -tuln
```
Review commands before using administrative privileges. `apt update` refreshes package metadata; it does not itself upgrade installed packages.

## Analysis and Findings
- Linux commands can show the current account, group memberships, and listening network sockets.
- Package updates are an important part of maintaining a secure system.
- The exact account/group output, listening ports, and update status were not recorded in the available notes, so no specific service or misconfiguration is claimed.
- Hardening should be deliberate: understand a service before disabling it, and preserve access to the VM.

## What I Learned
System hardening involves reducing unnecessary exposure, keeping software maintained, and applying appropriate permissions without breaking required functionality.

## Cybersecurity Relevance
Linux hardening is relevant to securing servers, cloud workloads, and analyst workstations.

## Next Phase
**Phase 12 — Basic Vulnerability Assessment**

## Safety and Authorization
Make configuration changes only on my own VM. Keep backups or snapshots before significant changes, and never publish passwords, keys, or sensitive configuration files
