# Broken Authentication

## What is it?
- Authentication is a key to a secure web application which allows user to gain access to web applications by verifying their identities. It it's broken then attacker can successfully gain access to other users account.

## Why is it dangerous?
Attackers can:
- Run brute force attacks allowing then to guess the username and pswd using multiple attempts.
- Successfully gain access to other users’ accounts.
- Access sensitive data (depending on the purpose of the application)

## What I did in TryHackMe:
- There was a mistake in the input field which developer forgets to sanitize and was very easy to    exploit i.e re-registration of an existing user
  - In the webapp login page if we put the username "darren", it showed user already exists so we      know darren is a user.
  - In the register page I tried to register darren again but with the space in front(" darren")       and try to login and it was successfull, I was redirected to darren account.
  - Repeated the same steps for the other user "arthur"

## Mitigation:
- Ensure the application has strong password policy.
- Limit the number of failed attempts.
- Implement multi factor authentication.

