# TryHeartMe - TryHackMe

## Category
Web Exploitation

## Difficulty
Easy

## Objective
Purchase the hidden "Valenflag" item.

---

## Initial Recon

- Opened the web application
- Explored UI functionality
- Used browser DevTools (Inspect Element)
- Observed authentication token stored in cookies/local storage

---

## Discovery

Found a JWT token.

Decoded it using:
https://jwt.io

Payload revealed:
{
  "user": "guest",
  "credits": 10
}

---

## Exploitation

1. Modified payload:
   - Changed "user" to "admin"
   - Changed "credits" to 1000

2. Re-encoded the token.
3. Replaced the original JWT in browser.
4. Refreshed page.
5. Gained admin-level access.
6. Purchased hidden item.
7. Retrieved flag.

---

## Vulnerability

Improper JWT validation.

- No signature verification
OR
- Weak secret key
OR
- Token trust without verification

Server trusted client-side token blindly.

---

## Key Learning

- JWTs should never be trusted without signature validation.
- Client-side data can be manipulated.
- Always inspect tokens.
- Privilege escalation can occur via token tampering.

---

## Tools Used

- Browser DevTools
- jwt.io
- Manual payload editing

---

## What I Would Try Next Time

- Check if signature is verified
- Attempt algorithm switching (none → HS256)
- Test for weak secret brute force
