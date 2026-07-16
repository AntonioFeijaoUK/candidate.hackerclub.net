# Candidate Security Architect

## Challenge 3 — Credential Exposure

The following response represents credentials retrieved from the simulated EC2 Instance Metadata Service.

These credentials are entirely fictional and provide no access to AWS or any other system.

Inspect the response and follow the clue contained in the session token.

```json
{
  "Notice": "These are simulated credentials and have no access to AWS.",
  "Code": "Success",
  "LastUpdated": "2026-07-16T10:30:00Z",
  "Type": "AWS-HMAC",
  "AccessKeyId": "ASIAFAKESECURITYARCHITECT",
  "SecretAccessKey": "THIS_IS_NOT_A_REAL_SECRET",
  "Token": "NEXT_CLUE=TXT:_security-architect.hackerclub.net",
  "Expiration": "2099-12-31T23:59:59Z"
}
```
