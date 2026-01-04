# Web Attack Detection via Logs

## Attack Types
- SQL Injection
- Cross-Site Scripting

## Log Source
Web server access logs

## Indicators
- Suspicious parameters
- Encoded payloads
- Repeated requests from same IP

## Detection Method
Correlated access log entries over time.

## SOC Response
- Blocked source IP
- Preserved logs
- Notified application team

## SOC Insight
Web attacks are detected through patterns, not single requests.
