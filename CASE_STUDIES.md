# Selected Security Case Studies

**Author:** Antonio Caetano · [GitHub](https://github.com/skuzu7) · [LinkedIn](https://www.linkedin.com/in/antonioccjr/)  
**Focus:** API security, application security, and AI-agent tool-use security.

These are independent, first-party engineering and research case studies. They use code I own, intentionally vulnerable local fixtures, and synthetic test data. They are not records of paid client engagements or assessments of third-party production systems.

## 1. API and web application security — CSA-LAB

**Goal:** demonstrate a complete, repeatable security-assessment and remediation workflow rather than publish isolated proof-of-concept exploits.

**Scope:** a deliberately vulnerable application running locally, with six planted weaknesses:

- Broken object-level authorization (BOLA/IDOR)
- SQL injection
- Path traversal
- Forgeable session token
- Negative-amount business-logic flaw
- Server-side request forgery (SSRF)

**Method:** define scope → reproduce each weakness → document root cause and impact → calculate CVSS v3.1 from the published vector → implement a focused fix → add a regression test → retest → validate detection logic.

**Inspectable results:**

- 6/6 intentionally planted findings reproduce in the vulnerable fixture.
- 6/6 corresponding regression checks pass against the patched fixture.
- Six Sigma detection rules are replayed against a small labelled corpus: 13/13 attack requests alerted and 0/22 benign requests alerted on the tested variants.
- CVSS values are calculated from vectors and covered by tests; the scores describe the modeled vulnerability, not real-world impact from this local fixture.

**Review the work:** [Repository](https://github.com/skuzu7/CSA-LAB) · [Finding write-ups](https://github.com/skuzu7/CSA-LAB/tree/main/writeups) · [Sample report](https://github.com/skuzu7/CSA-LAB/blob/main/reports/sample-assessment-report.md) · [CI workflow](https://github.com/skuzu7/CSA-LAB/blob/main/.github/workflows/ci.yml)

**Limitations:** first-party synthetic lab only. The detection corpus is small and in-sample; it is not a production detection-accuracy estimate.

## 2. AI-agent security — TRACEGUARD

**Goal:** explore how an application can constrain an AI agent's tool use when the model proposes actions based on untrusted input.

**Research question:** can a host-side policy layer enforce a narrowly defined task boundary, independently of the model's proposal?

**Method:** replay a bounded multi-step workflow using synthetic inputs, compare paired benign and adversarial scenarios, check each proposed action against a host-supplied plan and explicit authorization, and preserve a hash-linked trace.

**Inspectable results:**

- 16 paired synthetic scenarios.
- 26 offline tests.
- 8/8 scripted off-scope action attempts denied by the host-side policy in the documented positive-control run.
- Reproducible methodology, threat model, and results ledger.

**Review the work:** [TRACEGUARD source](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) · [Methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md) · [Threat model](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/THREAT_MODEL.md) · [Results](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/RESULTS.md)

**Limitations:** deterministic scripted controls, not a live-LLM jailbreak or robustness benchmark. The results do not establish production sandboxing, network isolation, or universal prompt-injection prevention.

## 3. Secure application engineering — Freeband (Next.js)

**Goal:** apply security engineering to a first-party Next.js/TypeScript application and make the relevant controls reviewable in code and CI.

**Work represented:**

- STRIDE threat model covering application assets and trust boundaries.
- Review of authentication and session-handling paths.
- Signed-session hardening and login-throttling controls.
- Automated tests, dependency auditing, linting, type-checking, production build, and browser smoke checks.
- CI-verified remediation of a Next.js dependency advisory.

**Review the work:** [Repository](https://github.com/skuzu7/freeband-nextjs) · [Threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) · [Security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) · [CI workflow](https://github.com/skuzu7/freeband-nextjs/blob/main/.github/workflows/ci.yml) · [Dependency remediation PR](https://github.com/skuzu7/freeband-nextjs/pull/10)

**Limitations:** first-party code and CI evidence. This is not a commissioned client audit, and CI checks do not prove the absence of all vulnerabilities or confirm that a production deployment has been updated.

## How I apply this work to an authorized client engagement

1. Agree on ownership, scope, test accounts, permitted methods, time window, exclusions, and emergency contacts.
2. Obtain written authorization before any testing.
3. Map assets, trust boundaries, identities, sensitive data, and API/agent capabilities.
4. Test only the agreed environment using controlled, non-destructive methods.
5. Deliver reproducible findings with impact, evidence, severity rationale, and prioritized remediation.
6. Retest fixes and provide regression tests or implementation guidance.

**No written authorization, no testing.** I do not test third-party systems outside their explicit permission and scope.

## What this portfolio does not claim

- No paid client penetration test or client audit is represented here.
- No CVE, accepted bug-bounty report, bounty award, or external vulnerability disclosure is claimed.
- No vendor certification, restricted-program membership, or independent accreditation is implied.
- Synthetic test counts are not presented as real-world attack rates or live-model security scores.

For the full evidence index, reproduction instructions, and reviewer notes, see the [Security Portfolio](SECURITY_PORTFOLIO.md) and [Reviewer Guide](REVIEWER_GUIDE.md).
