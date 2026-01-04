# DVWA – Command Injection (Easy)

## Objective
Understand how user input can be executed as system commands.

## Vulnerability
Command Injection

## Attack Explanation
User input was passed directly to a system command without validation.

## Evidence
Observed command output from injected input.

## Defense
- Validate input
- Avoid system calls
- Use allowlists

## Lessons Learned
Never trust user input at the system level.
