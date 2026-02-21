# JWT Basics

JWT = JSON Web Token

Structure:
HEADER.PAYLOAD.SIGNATURE

Header:
{
  "alg": "HS256",
  "typ": "JWT"
}

Payload:
{
  "user": "admin",
  "role": "user",
  "credits": 100
}

Signature:
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret
)

---

Common Vulnerabilities:

1. No signature validation
2. Weak secret key
3. Algorithm confusion (none attack)
4. Trusting client-side values

---

Always check:
- Can token be modified?
- Is signature verified?
- Is "alg" changeable?
