# SSH Brute Force Detection

## Attack Type
SSH Brute Force

## Log Source
Linux auth.log

## Indicators
- Repeated failed login attempts
- Same source IP
- Multiple usernames

## Detection Method
Filtered auth.log for failed password events.

## SOC Response
- Blocked attacker IP
- Monitored for successful logins

## SOC Insight
Brute force attacks are detected through repetition and timing.
