# Command Injection – Defense Review

## Vulnerable Code
User input was passed directly into shell_exec without validation.

## Root Cause
Trusting user input in a system-level command.

## Secure Fix
- Avoid shell execution
- Validate input strictly
- Use allowlists

## Security Lesson
Never execute OS commands with untrusted input.
