# Technique: JWT Token Manipulation

When to use:
- Application uses JWT authentication
- Token visible in cookies/local storage
- Privileges stored inside token

Steps:
1. Capture token
2. Decode using jwt.io
3. Modify payload (role/user/credits)
4. Re-encode
5. Replace token in browser
6. Refresh and test privilege escalation

Indicators:
- Token contains role/admin field
- No backend validation error

Risk:
Improper authentication control
