## Antonio Caetano — Software Engineer / Defensive Security Researcher

Independent developer working on application security: secure code review, threat modeling, and
vulnerability remediation with regression coverage. Based in Araraquara, Brazil.

**Focus:** finding real flaws in software I own or am authorized to test, fixing them, and proving
the fix holds with automated tests.

---

### What I test

Only software I build, deliberately vulnerable applications I create, and local containerized labs.
No third-party systems. Scope and authorization are documented explicitly in each project —
see [AUTHORIZATION.md](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md).

### Method

`discovery → controlled validation → root cause → remediation → regression test → write-up`

The deliverable is the patch and the test that keeps the flaw from coming back — not the exploit.

---

### Selected work

| Project | What it demonstrates |
|---|---|
| **[CSA-LAB](https://github.com/skuzu7/CSA-LAB)** | Reproducible AppSec lab. 5 documented findings (IDOR, SQLi, path traversal, session forgery, business-logic) with proof-of-concept tests, patched variants, and a passing regression suite. Localhost only. |
| **[freeband-nextjs](https://github.com/skuzu7/freeband-nextjs)** | Next.js/TypeScript app with a STRIDE threat model, documented security review, authentication hardening, regression tests and GitHub Actions CI. |
| **[Shopping-Cart-Project](https://github.com/skuzu7/Shopping-Cart-Project)** | Server-side Stripe payment integration with documented trust boundaries and a vulnerability reporting policy. |
| **[CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian)** | Browser automation toolkit (Camoufox + MCP server) for authorized QA, accessibility auditing and agent evaluation. |
| **[TranslatePDF](https://github.com/skuzu7/TranslatePDF)** | PDF translation preserving layout, fonts and images. |

---

### Stack

TypeScript · Next.js · Python · Rust · PostgreSQL · Docker · GitHub Actions

### Contact

[LinkedIn](https://br.linkedin.com/in/antonioccjr)
