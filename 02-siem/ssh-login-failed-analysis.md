# SSH Failed Login Attempts – Basic Analysis

## Context
While reviewing the Linux authentication logs, multiple failed SSH login
attempts were observed.

## Log source
- /var/log/auth.log
- Service: SSH

## Observations
The following patterns were identified:
- Multiple failed login attempts
- Source IP addresses were visible in the logs
- Each attempt included timestamp, username, source IP, and port

Some entries indicated attempts using invalid usernames.

## Initial assessment
Repeated failed login attempts within a short period of time may indicate
either user error or automated brute force activity.

At this stage, no successful login related to these attempts was observed.

## Next steps
- Correlate attempts by source IP 
- Check for successful authentication after failures
- Implement alerting for repeated failed logins

