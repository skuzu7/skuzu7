# Defensive Security Portfolio — Evidence Index

**Maintainer:** Antonio Caetano (@skuzu7)  
**Focus:** application security, threat modeling, remediation, and regression testing in owned or explicitly authorized environments.  
**Updated:** 2026-11-14

This document indexes public, inspectable work. It is not a certification, a claim of professional penetration-testing engagements, or evidence of CVEs/bug bounties. Claims below are limited to the documented repository contents. Test instructions are provided for independent reproduction; the linked GitHub Actions runs for the CI fix and the offline agent-policy benchmark both completed successfully, but no external review or certification is claimed.

## 1. Evidence at a glance

| Area | Project | Inspectable evidence |
| --- | --- | --- |
| Multi-step agent tool-use security research | [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) | 8 matched benign/attack pairs, 26 offline tests, bounded state machine, host-enforced denials, hash-linked trace and [CI PR #14](https://github.com/skuzu7/CSA-LAB/pull/14); scripted controls only, no real-model scores |
| Vulnerability analysis and remediation | [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | Six local-lab findings, root-cause write-ups, patched variants, security/regression tests |
| Classification and severity | [Finding classification](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md) | CWE, OWASP Top 10:2025 / API Top 10 2023, MITRE ATT&CK and CVSS v3.1 per finding; scores computed from vectors by a [tested calculator](https://github.com/skuzu7/CSA-LAB/blob/main/classification/cvss31.py), page generated and checked in CI |
| Detection engineering | [Sigma rules and replay](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | One rule per finding; 35 labelled requests replayed on the vulnerable and patched builds: 13/13 attack requests alerted, 0/22 benign alerted; rules parse in pySigma. In-sample check on a small corpus, not a production efficacy estimate |
| Threat-informed testing | [Adversary emulation plan](https://github.com/skuzu7/CSA-LAB/blob/main/docs/adversary-emulation-plan.md) | Six-step ATT&CK-mapped intrusion chain with procedure, telemetry, detection and control per step; no named group, no post-exploitation |
| Reporting and engagement practice | [Sample report](https://github.com/skuzu7/CSA-LAB/blob/main/reports/sample-assessment-report.md), [engagement kit](https://github.com/skuzu7/CSA-LAB/tree/main/engagement) | Client-format report with retest results; scoping questionnaire, rules of engagement, operating standard. Samples and templates, not records of a paid engagement |
| Scope and authorization | [CSA-LAB authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md) | Explicit localhost/owned-code boundaries and prohibited actions |
| Automated defensive testing | [CSA-LAB CI](https://github.com/skuzu7/CSA-LAB/blob/main/.github/workflows/ci.yml) | Tested vulnerable and patched local fixtures; associated PR workflows completed successfully |
| Threat modeling | [freeband-nextjs STRIDE model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) | Assets, trust boundaries, threats, mitigations, and test references for authentication |
| Secure code review | [freeband-nextjs security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) | Scoped review of first-party authentication/session code, evidence and limitations |
| Remediation engineering | [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) | Signed sessions, login throttling, tests and [CI-verified Next.js security advisory remediation](https://github.com/skuzu7/freeband-nextjs/pull/10); [performance PR #23 merged](https://github.com/skuzu7/freeband-nextjs/pull/23); [lazy PDF loading PR #24](https://github.com/skuzu7/freeband-nextjs/pull/24) in CI. This is first-party patching, not external CVE discovery |
| Browser/MCP data-boundary hardening | [CSA-Obsidian PR #4 merged](https://github.com/skuzu7/CSA-Obsidian/pull/4) and [follow-up PR #5](https://github.com/skuzu7/CSA-Obsidian/pull/5) | PR #4 removed service-specific token capture, redacted request headers and cookie values, retained only request origins, and validated session paths. PR #5 adds fail-closed HTTP(S) host allowlisting and Windows ACL hardening; Linux and Windows CI passed. No independent audit is claimed |
| Agent tool-boundary policy testing | [Offline benchmark](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/README.md) | 19 synthetic allow/deny decisions: host-approved plans, sensitive paths, explicit write approval, untrusted tool results; no LLM used |
| Paired prompt-injection evaluation methodology | [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) | 24 matched scenarios (12 benign/attack pairs), 14 offline unit tests, JSON scoring and optional user-initiated real-provider calls; none made yet |

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

**To reproduce in your own local clone:** follow the [CSA-LAB README](https://github.com/skuzu7/CSA-LAB#reproduce-everything) and its [CI workflow](https://github.com/skuzu7/CSA-LAB/blob/main/.github/workflows/ci.yml). The vulnerable variant is intentionally insecure; never publish its service on a network.

The defensive workflow is: **document scope → model the threat → reproduce in a local fixture → identify root cause → patch → write a regression test → record limitations**.

## 3. Deterministic AI-agent authorization benchmark

The [offline tool-boundary evaluation](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/README.md) exercises 19 synthetic authorization cases and emits a structured JSON report through [GitHub Actions](https://github.com/skuzu7/CSA-LAB/actions). It checks a small host-supplied trusted plan and separate write approval. It does **not** run an LLM or measure jailbreak/prompt-injection success rates. See the documented limits on DNS/network isolation, file-system races and production enforcement.

## 4. Scoped agent proposal evaluation

The [Scoped Agent Evals harness](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) creates 12 matched benign/attack pairs (24 cases), a strictly separate host-policy gate, and testable proposal-level scoring. [Methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/METHODS.md), [results ledger](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/RESULTS.md), and [GitHub Actions](https://github.com/skuzu7/CSA-LAB/actions) document reproducibility and limitations. A separate scripted positive control makes all 12 adversarial proposals and verifies host denial, without invoking a model. The offline baseline is **not** an LLM security score; no live provider benchmark or independently accepted third-party finding is asserted.

### TRACEGUARD: bounded multi-step replay

[TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) independently models the sequence **read untrusted document → propose agent actions → enforce exact trusted host plan → report → finish**. The [methodology](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md), [threat model](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/THREAT_MODEL.md), and [results ledger](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/RESULTS.md) explicitly distinguish 16 synthetic paired cases and 26 offline tests from real-model performance. Its scripted attack positive control receives eight denials across 56 simulated steps; no prohibited operation is executed against a real system.

## 5. First-party application review

In [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs):

- The [STRIDE threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) identifies the protected proposal editor, session cookies and authentication boundaries.
- The [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) records its reviewed code paths, controls, findings and limits.
- The [security policy](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY.md) distinguishes source/local testing from production or third-party testing.
- The [CI workflow](https://github.com/skuzu7/freeband-nextjs/blob/main/.github/workflows/ci.yml) is available for independent review of automated checks.

## 6. Authorized research boundaries

- **In scope:** personal code, owned local or staging deployments, deliberately vulnerable local apps, and educational environments within their published rules.
- **Out of scope:** third-party production systems, real credentials/data, phishing, credential theft, persistence, unauthorized scanning, and unsanctioned exploitation.
- **No current active bug bounty** is asserted by [the lab scope inventory](https://github.com/skuzu7/CSA-LAB/blob/main/docs/scope.md).
- All findings in the lab are educational and **do not** represent verified external breaches, public CVEs, paid assessments or professional certifications.
- Report genuine issues privately through a project's published security policy; do not publish secrets or exploit payloads in public issues.

## 7. Research direction

The lab now covers the full cycle on first-party code. What it cannot supply is external validation, so the next work is outward-facing: accepted reports through authorized programmes, reviewed security patches to open-source projects, and client assessments under signed rules of engagement. Any external security work requires explicit authorization and an updated scope.

**Research roadmap:** [Evidence-based milestones](RESEARCH_MILESTONES.md).

**Contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr) · [GitHub](https://github.com/skuzu7).
