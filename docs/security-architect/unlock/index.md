# Candidate Security Architect

## challenge 2

Is there a security weakness in this architecture?

For the next challenge, add the 1 word weakness in the the url (e.g.  https://candidate.hackclub.net/security-architect/unlock/"YOUR_ANSWER"


```
                         Internet
                            │
                            ▼
                    Application Load Balancer
                            │
                            ▼
                EC2 URL Preview Application
                ┌────────────────────────────┐
User URL ──────▶│ Fetches user-supplied URLs │
                │                            │
                │ Instance profile:          │
                │ CandidateApplicationRole   │
                │                            │
                │ IMDSv1: enabled            │
                │ IMDSv2: optional           │
                └─────────────┬──────────────┘
                              │
                              ▼
                       Amazon S3 bucket
```

