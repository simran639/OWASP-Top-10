# Security Logging and Monitoring Failures

## What is it?
- Logging is the process of keeping track of every action performed by the user in webapp and is important so that we can trace malicious behaviour in the system.

## Why is it dangerous?
- Allows attackers to operate undetected.
- Delays response and containment.
- Violates compliance requirements (e.g., PCI-DSS, HIPAA).

# What I did in TryHackMe:
- Reviewed sample log files.
- Detected repeated brute-force login attempts from 49.99.13.16
- Identified lack of alerts or lockouts, making the attack easy to miss.

## Mitigation:
- Implement centralized logging and alerting.
- Monitor login attempts, permission changes, etc.
- Automate detection with tools like ELK, Wazuh, or SIEMs.


