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

# DVWA – SQL Injection (Easy)

## Objective
Understand how improper input handling leads to SQL Injection.

## Vulnerability
SQL Injection

## Attack Explanation
User input was inserted directly into an SQL query, allowing manipulation of query logic.

## Evidence
Injected input returned multiple database records.

## Defense
- Use prepared statements
- Parameterized queries
- Input validation

## Lessons Learned
Never allow user input to control database queries.

# DVWA – XSS (Reflected) – Easy

## Objective
Understand how reflected user input can execute in the browser.

## Vulnerability
Reflected Cross-Site Scripting (XSS)

## Attack Explanation
User input was reflected in the HTTP response without proper encoding, allowing JavaScript execution.

## Evidence
Injected script executed in the browser.

## Defense
- Output encoding
- Input validation
- Content Security Policy

## Lessons Learned
Never trust reflected input in web responses.

