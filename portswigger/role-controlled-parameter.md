# User Role Controlled by Request Parameter

## Platform
PortSwigger Web Security Academy

## Vulnerability
Broken Access Control / Privilege Escalation

## Description
The application determines user privileges based on a client-controlled
request parameter. By modifying this parameter, a low-privileged user
can gain administrative access.

## Steps to Reproduce
1. Login as a normal user.
2. Capture an admin access request using Burp Suite.
3. Modify the Admin parameter from false to true.
4. Replay the request using Burp Repeater.

## Proof of Exploitation
See screenshot showing modified request and successful response.

## Impact
An attacker can escalate privileges to administrator and perform
unauthorized actions such as deleting user accounts.

## Mitigation
Enforce server-side authorization checks and never trust
client-controlled role parameters.
