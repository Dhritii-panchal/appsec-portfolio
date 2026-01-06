# Unprotected Admin Functionality

## Platform
PortSwigger Web Security Academy

## Vulnerability
Broken Access Control

## Description
The application exposes an administrative interface that is not
protected by authentication or authorization checks.

## Steps to Reproduce
1. Access the application as an unauthenticated user.
2. Discover the admin endpoint via robots.txt or page source.
3. Navigate directly to the admin panel URL.
4. Perform administrative actions.

## Proof of Exploitation
![Admin Panel Access](../screenshots/admin-panel-access.png)

## Impact
Any attacker can access administrative functionality and delete
user accounts.

## Mitigation
Restrict admin functionality with strict server-side authentication
and authorization controls.
