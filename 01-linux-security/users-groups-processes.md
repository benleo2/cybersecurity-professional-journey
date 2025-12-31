# Linux Users, Groups & Process Security

## What it is
Linux controls access using users, groups, and process ownership.

## Why it matters in security
Privilege escalation attacks target misconfigured users and services running as root.

## Commands Used
- whoami
- id
- useradd
- usermod
- su
- ps
- top
- kill

## Hands-on Practice
- Created a test user
- Switched user contexts
- Modified group membership
- Observed process ownership
- Terminated processes safely

## How attackers abuse this
Attackers try to add themselves to sudo or run malicious processes as root.

## How to defend
- Principle of least privilege
- Monitor user changes
- Limit root services
