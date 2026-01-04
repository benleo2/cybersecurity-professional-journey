# XSS – Defense Review

## Vulnerable Code
User input was reflected directly into HTML output without encoding.

## Root Cause
Missing output encoding caused the browser to execute injected scripts.

## Secure Fix
- Encode output using htmlspecialchars
- Implement Content Security Policy

## Security Lesson
Always encode output, even if input is validated.
