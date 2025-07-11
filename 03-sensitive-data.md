# Sensitive Data Exposure(Cryptographic Failures)

## What is it?
- In webapp sensitive data can often be refered to the data direclty linked to the customers (e.g. names, dates-of-birth, financial information, etc), but could also be more technical information, such as usernames and passwords. It can be exposed when data is inadequately protected during storage or transmission.

## Why is it dangerous?
Attackers can:
- Steal or crack credentials.
- Intercept sensitive data over insecure channels (like HTTP).
- Compromise user accounts, especially reused passwords

## What I did in TryHackMe:
- In the webapp source page discovered a folder named "webapp.db" from "assets/" folder.
- Inside the database file found bunch of users with their hashed password.
- Extracted the MD5 hash of admin user and used "https://crackstation.net/" to crack the hash      password.
- Logged in as admin and retrieved the flag.
  
## Mitigation:
- Use modern hashing algorithms (bcrypt, scrypt, Argon2).
- Enforce HTTPS for all data transmission




