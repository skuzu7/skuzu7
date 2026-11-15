# Antonio Caetano

**Application Security Engineer | API Security | AI Agent Security**

I help teams secure APIs and AI-powered applications by combining software engineering with evidence-first security work: scoped testing, reproducible findings, practical remediation, and regression tests.

**Focus:** API and web application security · AI-agent tool-use security · secure code review · threat modeling · remediation and retesting.

[**Case studies**](CASE_STUDIES.md) · [**Evidence portfolio**](SECURITY_PORTFOLIO.md) · [**Reviewer guide**](REVIEWER_GUIDE.md) · [**Services and engagement process**](https://github.com/skuzu7/CSA-LAB/blob/main/SERVICES.md) · [**Sample report**](https://github.com/skuzu7/CSA-LAB/blob/main/reports/sample-assessment-report.md)

## What I work on

- **API and web application security** — authorization and access-control flaws (including BOLA/IDOR), authentication and session handling, injection, SSRF, path traversal, and business-logic weaknesses.
- **AI-agent security** — threat modeling for tools and data, prompt-injection test design, untrusted tool-output handling, excessive agency, and host-side authorization boundaries.
- **Secure remediation** — root-cause analysis, focused code changes, regression tests, and retesting.
- **Detection engineering** — Sigma rules and replay-based validation for the behaviors covered by a test.

## Evidence you can inspect

| Project | What it demonstrates | Evidence and limits |
| --- | --- | --- |
| [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | End-to-end application-security workflow: scope, reproduce, classify, detect, patch, and retest | Six intentionally planted vulnerabilities in a local lab; 6/6 reproductions and 6/6 regression checks. CVSS v3.1 vectors are computed and tested. Synthetic first-party fixtures only. |
| [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) | Multi-step AI-agent tool-use authorization and traceability | 16 paired synthetic cases, 26 offline tests, and 8/8 scripted off-scope requests denied. Deterministic host-policy tests; not a live-LLM robustness score. |
| [Agent policy and scoped evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | Tool-boundary policy checks and proposal-level evaluation methodology | 19 synthetic policy decisions and 24 proposal scenarios. No live model benchmark is claimed. |
| [Freeband — Next.js](https://github.com/skuzu7/freeband-nextjs) | Security-focused engineering of a first-party web application | STRIDE threat model, session hardening, security review, automated tests, and CI-verified dependency remediation. Not a commissioned client audit. |

For a concise, client-facing walkthrough, see [case studies](CASE_STUDIES.md). For the full evidence map, reproduction steps, and limitations, see the [security portfolio](SECURITY_PORTFOLIO.md).

## How I work

1. **Scope and authorization** — define assets, accounts, test window, exclusions, and written permission before testing.
2. **Threat model** — map trust boundaries, sensitive data, identities, and agent tools.
3. **Test and reproduce** — use controlled, non-destructive checks within the agreed scope.
4. **Report and remediate** — explain impact and root cause, prioritize fixes, and provide practical implementation guidance.
5. **Retest** — add or run regression tests and document residual risk.

I only test systems I own or am explicitly authorized to assess. No written authorization, no testing.

## Technical toolkit

**Languages:** Python · TypeScript · JavaScript · SQL · Rust  
**Application engineering:** Node.js · Next.js · React · REST APIs · PostgreSQL  
**Security:** OWASP Top 10 · OWASP API Security Top 10 · Burp Suite · threat modeling · secure code review · CVSS v3.1  
**Delivery:** Docker · GitHub Actions · automated tests · CI/CD

## Scope and transparency

The public security work here is independent, first-party research using intentionally vulnerable local applications and synthetic data. The AI-agent measurements are deterministic scripted evaluations, not real-model performance results.

I do not claim client penetration-testing engagements, accepted CVEs, bug-bounty awards, external certifications, or membership in vendor restricted-access programmes unless a separately verifiable record exists. See the [research milestones](RESEARCH_MILESTONES.md) for what remains unverified.

## Contact

- [LinkedIn](https://www.linkedin.com/in/antonioccjr/)
- [Upwork](https://www.upwork.com/freelancers/~01b32820f48485fe92)
- [GitHub repositories](https://github.com/skuzu7?tab=repositories)

Based in Brazil (UTC−3). Portuguese: native. English: technical working proficiency (B2).
