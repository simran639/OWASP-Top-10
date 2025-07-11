# Broken Access Control

# What is it?
- In web-based app every user have their own roles and permission, broken access control occurs when users are able to access data or perform tasks that should be restricted according to their role or authentication level.

# Why is it dangerous?
Attackers can:
- Access or modify other users data.
- Escalate privileges (e.g., from regular user to admin).
- Exfiltrate sensitive records.

# What I did in TryHackMe:
- It provided me the username and password for user:noot.
- After login in the URL my id was shown as note_id = 1, and when i try to access a different id eg note_id = 0 which belonged to a different user, exposing private notes.
- Retrieved flag: flag{fivefourthree} by exploiting Insecure Direct Object Reference (IDOR).

# Mitigation
- Implement server-side access controls.
- Avoid trusting user input like IDs in URLs.
