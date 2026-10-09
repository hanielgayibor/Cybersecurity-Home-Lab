# Phase 13 — Introduction to Penetration Testing

## Objective
Understand the structured penetration-testing process and practice safe reconnaissance in an isolated lab.

## Topics Covered
- Scope and written authorization
- Reconnaissance
- Enumeration
- Validation of potential weaknesses
- Evidence collection
- Reporting and remediation
- Retesting

## Activities
- Define the permitted lab targets before testing.
- Gather basic information about the target VM.
- Use limited Nmap scans against the confirmed lab IP.
- Separate observations from assumptions.
- Write a brief report with impact and remediation suggestions.

Example command:
```bash
nmap 192.168.56.3
```
Replace the example IP with the verified lab target.

## Analysis and Findings
- The earlier lab work introduced host discovery, port scanning, and service detection as reconnaissance techniques.
- Scan output must be interpreted carefully: filtered ports may indicate network filtering, and a detected service does not automatically mean it is exploitable.
- No successful exploit or confirmed compromise is documented here.
  
## What I Learned
A professional test begins with permission and a defined scope. Results should be reproducible and reported clearly, including limitations and recommended fixes.

## Cybersecurity Relevance
Penetration-testing methodology helps defenders understand how weaknesses are discovered and how to prioritize remediation.

## Next Phase
**Phase 14 — Web Application Security Basics**

## Safety and Authorization
Test only systems explicitly in scope. Do not run exploit attempts against public or third-party systems.
