# Candidate Security Architect

## Challenge 2 — AWS Architecture Review

You have reached a simulated AWS architecture review.

Review the architecture below and identify the most significant security weakness.

For your notes, record:

- the security weakness;
- the potential impact;
- your recommended remediation.

You will submit these at the final stage.

To reach the next challenge, replace `unlock` in the current URL with the insecure EC2 metadata-service version shown in the diagram.

Use lowercase characters in the URL.

> Example format:
>
> `https://candidate.hackerclub.net/security-architect/unlock/`
>
> `https://candidate.hackerclub.net/security-architect/your-answer/`

---

## Architecture

```text
                          Internet
                              │
                              ▼
                    Application Load Balancer
                              │
                              ▼
                  EC2 URL Preview Application
              ┌──────────────────────────────────┐
              │ Accepts a user-supplied URL      │
              │ and retrieves its content        │
              │                                  │
              │ Instance profile:                │
              │ CandidateApplicationRole         │
              │                                  │
              │ IMDSv1: enabled                  │
              │ IMDSv2: optional                 │
              └───────────────┬──────────────────┘
                              │
                              ▼
                     Private Amazon S3 bucket
```
