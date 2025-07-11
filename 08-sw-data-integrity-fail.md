# Software and Data Integrity Failures

## What is it?
- Integrity is one of the component of CIA triad and refers that data remains unmodified. These flaws happen when apps deserialize untrusted data without validation and allowing attackers to inject malicious objects/code into memory.

## Why is it dangerous?
- Run Remote Code Execution (RCE).
- Data corruption or logic tampering.
- Attacks against CI/CD or update mechanisms.

## What I did in TryHackMe:
- For Software Integrity Failures
    - Used website https://www.srihash.org/. to generate hashes.
    - Input the given URL (https://code.jquery.com/jquery-1.12.4.min.js) using SHA-254 and get the value.

- For Data Integrity
    - Used default guest:guest user to login.
    - From the Storage got the JWT stored as a cookies value which is a base64 and decoded it.
    - Pasted the decoded value in jwt-session and changed the username from guest to admin.
    - Retrieved the flag after refreshing the page.

## Mitigation:
- Avoid using native deserialization of untrusted data.
- Use digital signatures to verify serialized data.
- Employ allowlists for object types and input validation

