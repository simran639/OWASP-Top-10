# Insecure Design

## What is it?
- Insecure Design refers to security flaws in the application's architecture or logic, such as missing security controls or predictable flows (e.g., password resets based on weak knowledge questions).

## Why is it dangerous?
Attackers can:
- Bypass authentication or authorization.
- Manipulate app behaviour.

## What I did in TryHackMe:
- Initiated a password reset for user joseph.
- Security question was easily brute-forced (What is your favourite color? → Green)
- The system automatically generates a new temp password, reset the password and gained access.
- Retrieved flag: THM{Not_3ven_c4tz_c0uld_sav3_U!}
  
## Mitigation:
- Design apps with security at the core (threat modeling, abuse cases)
- Avoid knowledge-based authentication
- Use strong reset mechanisms with token validation




