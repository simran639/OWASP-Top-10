# Vulnerable & Outdated Components

## What is it?
- In webapp we used many libraries, packages or dependencies that may contain known security flaws which makes our app vulnerable to exploitation.

## Why is it dangerous?
- Attackers can use public exploits (RCE, privilege escalation).
- Can result in full system compromise.
- Developers may not even be aware their stack is vulnerable.

## What I did in TryHackMe:
- Found a vulnerable bookstore application and searched it up in Exploit db site.
- Identified the tech stack and looked up CVEs.
- Download the exploit [47887.py] and run it.
- Retrieved flag from  /opt/flag.txt :THM{But_1ts_n0t_myf4ult!}

## Mitigation:
- Keep dependencies up to date (use tools like npm audit, pip-audit).
- Monitor for CVEs (Snyk, GitHub Dependabot).
- Remove unused services/components.

