# Phase 14 — Web Application Security Basics

## Objective
Learn common web application security concepts and understand how to examine a web application's behavior in a controlled lab.

## Lab Environment
- Local or intentionally vulnerable lab application, such as OWASP Juice Shop, if configured
- Web browser
- Developer tools or an intercepting proxy, if available

## Topics Covered
- HTTP requests and responses
- Methods, status codes, and headers
- Authentication and sessions
- Input validation
- Access control
- Common web application risks

## Activities
- Navigate the lab application normally.
- Inspect request and response details using browser developer tools.
- Identify where the application uses authentication or sessions.
- Read security guidance and document potential risks without testing outside the lab.

## Analysis and Findings
- HTTP traffic consists of requests and responses, including methods, headers, status codes, and sometimes a body.
- HTTPS encrypts traffic in transit; packet captures may still show metadata, but application contents are generally not readable without appropriate decryption context.
- OWASP Juice Shop was identified as a planned lab application

## What I Learned
Web security requires attention to both the browser-facing behavior and the server-side decisions that protect data and functionality.

## Cybersecurity Relevance
Web application security knowledge helps analysts assess authentication, access control, data handling, and common attack surfaces.

## Next Phase
**Phase 15 — Web Application Penetration Testing**

## Safety and Authorization
Use an intentionally vulnerable local application or a target where testing is explicitly authorized. Do not test real websites without permission.
