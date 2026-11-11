# Defensive Security Portfolio — Evidence Index

**Maintainer:** Antonio Caetano (@skuzu7)  
**Focus:** application security, threat modeling, remediation, and regression testing in owned or explicitly authorized environments.  
**Updated:** 2026-11-10

This document indexes public, inspectable work. It is not a certification, a claim of professional penetration-testing engagements, or evidence of CVEs/bug bounties. Claims below are limited to the documented repository contents. Test instructions are provided for independent reproduction; results were not re-executed as part of this index update.

## 1. Evidence at a glance

| Area | Project | Inspectable evidence |
| --- | --- | --- |
| Vulnerability analysis and remediation | [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | Six local-lab findings, root-cause write-ups, patched variants, security/regression tests |
| Scope and authorization | [CSA-LAB authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md) | Explicit localhost/owned-code boundaries and prohibited actions |
| Automated defensive testing | [CSA-LAB CI](https://github.com/skuzu7/CSA-LAB/blob/main/.github/workflows/ci.yml) | GitHub Actions definition exercising vulnerable and patched test suites |
| Threat modeling | [freeband-nextjs STRIDE model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) | Assets, trust boundaries, threats, mitigations, and test references for authentication |
| Secure code review | [freeband-nextjs security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) | Scoped review of first-party authentication/session code, evidence and limitations |
| Remediation engineering | [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) | Signed sessions, login throttling, security tests and CI as documented in the project |
| Controlled QA automation | [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian) | MCP/browser tooling for authorized QA, accessibility and agent evaluation |

## 2. Reproducible local case studies

The six CSA-LAB cases use intentionally vulnerable software, synthetic fixtures and a local test target — **not real-world victim systems**.

| Finding | Weakness | Documentation |
| --- | --- | --- |
| 001 | Broken object-level authorization (IDOR) | [Root cause, reproduction, fix and regression](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-001.md) |
| 002 | SQL injection | [Root cause, reproduction, fix and regression](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-002.md) |
| 003 | Path traversal | [Root cause, reproduction, fix and regression](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-003.md) |
| 004 | Forgeable session token | [Root cause, reproduction, fix and regression](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-004.md) |
| 005 | Negative-amount business-logic flaw | [Root cause, reproduction, fix and regression](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-005.md) |
| 006 | Server-side request forgery (SSRF) | [Root cause, reproduction, fix and regression](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-006.md) |

**To reproduce in your own local clone:** follow the [CSA-LAB README](https://github.com/skuzu7/CSA-LAB#quick-start-windows--linux) and its [CI workflow](https://github.com/skuzu7/CSA-LAB/blob/main/.github/workflows/ci.yml). The vulnerable variant is intentionally insecure; never publish its service on a network.

The defensive workflow is: **document scope → model the threat → reproduce in a local fixture → identify root cause → patch → write a regression test → record limitations**.

## 3. First-party application review

In [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs):

- The [STRIDE threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) identifies the protected proposal editor, session cookies and authentication boundaries.
- The [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) records its reviewed code paths, controls, findings and limits.
- The [security policy](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY.md) distinguishes source/local testing from production or third-party testing.
- The [CI workflow](https://github.com/skuzu7/freeband-nextjs/blob/main/.github/workflows/ci.yml) is available for independent review of automated checks.

## 4. Authorized research boundaries

- **In scope:** personal code, owned local or staging deployments, deliberately vulnerable local apps, and educational environments within their published rules.
- **Out of scope:** third-party production systems, real credentials/data, phishing, credential theft, persistence, unauthorized scanning, and unsanctioned exploitation.
- **No current active bug bounty** is asserted by [the lab scope inventory](https://github.com/skuzu7/CSA-LAB/blob/main/docs/scope.md).
- All findings in the lab are educational and **do not** represent verified external breaches, public CVEs, paid assessments or professional certifications.
- Report genuine issues privately through a project's published security policy; do not publish secrets or exploit payloads in public issues.

## 5. Research direction

Further reproducible, defensive work on first-party systems: vulnerability triage, secure-code review, detection engineering, patch verification, and concise write-ups that record evidence as well as uncertainty. Any future external security work will require explicit authorization and an updated scope.

**Contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr) · [GitHub](https://github.com/skuzu7).
