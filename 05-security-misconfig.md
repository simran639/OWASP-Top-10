# Security Misconfiguration

## What is it?
- Security Misconfiguration happens when systems or apps are insecure by default (e.g., debug mode enabled, default credentials, unpatched components, exposed sensitive files).

## Why is it dangerous?
- Attackers can gain shell access or sensitive info.
- Can lead to privilege escalation or data theft.
- Common in cloud services, frameworks, and containers.

## What I did in TryHackMe:
- Found Python Werkzeug Debug Console exposed to the web
- Used it to explore the server environment (import os; print(os.popen("ls -l").read()))
- Located the database file todo.db.
- Modified app.py to get tge flag (import os; print(os.popen("cat app.py").read())).
- Retrieved flag from its content: THM{Just_a_tiny_misconfiguration}

## Mitigation:
- Disable debug mode in production.
- Regularly audit infrastructure and third-party components.
- Use security headers and file permissions correctly.

