# Authentication – Defense Review

## Vulnerability
Weak authentication logic allowed unlimited login attempts.

## Root Cause
Missing rate limiting, lockout, and secure session controls.

## Secure Fix
- Implement rate limiting
- Use account lockout
- Apply generic error messages
- Secure session handling

## Security Lesson
Authentication must assume attackers will try repeatedly.
