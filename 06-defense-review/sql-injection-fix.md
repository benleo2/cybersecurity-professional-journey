# SQL Injection – Defense Review

## Vulnerable Code
User input was directly concatenated into an SQL query.

## Root Cause
Lack of prepared statements and parameter binding.

## Secure Fix
- Use prepared statements
- Bind parameters
- Validate input types

## Security Lesson
User input must never alter SQL query logic.
