# Injection

## What is it?
- Injection occurs when an input field is interpreted as a code/commands by the interpreter and is not trust worthy. Somr example of it are SQL, OS, or LDAP commands.

## Why is it dangerous?
Attackers can:
- Run arbitrary system commands
- Dump Databases
- Escalate privileges or pivot into internal systems

## What I did in TryHackMe:
-Used the input field to run system commands via a web-based cowsay endpoint which leaded me to some interesting information such as:
  - whoami -> apache
  - Retrived a suspicious file name drpepper.txt (ls)
  - Identified OS version (cat /etc/os-release)
-I did all by using the command injection by appending different shell commands to form input.

## Mitigation:
-Validate and sanitize all user inputs.
-Use parameterized queries and command execution libraries that avoid shell contexts.
