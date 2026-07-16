# Candidate Security Architect

## Challenge 2 — AWS Architecture Review

You have reached a simulated AWS architecture review.

Review the architecture below and identify the most significant security weakness.

For your notes, record the weakness and your recommended remediation.  
You will submit both at the final stage.

To reach the next challenge, replace the word `unlock` in the URL with your 1 work answer

> e.g.  
> https://candidate.hackclub.net/security-architect/unlock
> https://candidate.hackclub.net/security-architect/"YOUR_ANSWER"

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

