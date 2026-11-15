# Institutional Cybersecurity Portfolio — Independent Review Dossier

**Individual researcher / software engineer based in Brazil.**  
**Evidence status:** public first-party defensive research and software engineering; not state affiliation, a procurement qualification, an audited government system, a CVP membership, a professional certification, or an approved critical-infrastructure testing authority.

## Executive scope

Research in secure software engineering, web/API application security, synthetic vulnerability assessment, host-enforced AI-agent tool authorization, and auditable remediation. Work is limited to first-party code, localhost fixtures and properly authorized external activities.

For a government or critical-infrastructure reviewer, evidence is more important than branding: each claim is linked to code, tests, findings, limitations and change history.

## Priority evidence

| Area | Evidence | Verification | Boundary |
| --- | --- | --- | --- |
| Reproducible AppSec | [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | [CI](https://github.com/skuzu7/CSA-LAB/actions/workflows/ci.yml), [six findings](https://github.com/skuzu7/CSA-LAB/tree/main/writeups), [patch regressions](https://github.com/skuzu7/CSA-LAB/tree/main/tests/regression) | Planted local vulnerabilities, not external disclosures |
| Agent-control research | [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) | [Methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md) and [results](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/RESULTS.md) | Scripted offline controls, not a validated live-model security rate |
| Detection engineering | [Sigma and traffic replay](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | [Detection workflow](https://github.com/skuzu7/CSA-LAB/blob/main/.github/workflows/ci.yml) | Small in-sample synthetic dataset |
| Browser automation safety | [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian) | [Policy tests](https://github.com/skuzu7/CSA-Obsidian/blob/main/tests/test_policy.py), [CI](https://github.com/skuzu7/CSA-Obsidian/actions/workflows/ci.yml) | Local research, not a production network sandbox |
| Software hardening | [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) | [Threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md), [review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) | First-party work; performance workflow had a documented failure on 2026-11-14 |
| Systems engineering | [claw-code](https://github.com/skuzu7/claw-code) | [Rust CI](https://github.com/skuzu7/claw-code/actions) and source | Distinguish upstream author contributions; no standalone CVP evidence inferred |

## Audit-ready change proposals (not yet merged)

- [CSA-LAB assurance PR #22](https://github.com/skuzu7/CSA-LAB/pull/22): versioned control register, claim-validation tests and institutional readiness roadmap.
- [CSA-Obsidian hardening PR #6](https://github.com/skuzu7/CSA-Obsidian/pull/6): secret/session path guard, evidence map and CI defense in depth.

Pull requests are proposals until reviewed and merged; CI execution is not external assurance.

## Program-readiness evidence gates

| Goal | What can be offered today | Evidence or approval still required |
| --- | --- | --- |
| Individual CVP Defense | Public synthetic research, engineering reports, traceable scope | Relevant accepted external vulnerability reporting track record as applicable, provider identity check and approval |
| Organizational CVP Red Team | Engineering methodology and sample professional templates | Actual legal organization, qualified staff, authorized engagements, organizational MFA/SSO, managed devices and enforceable network controls |
| CVP Specialized | No claim of eligibility | Demonstrable authorization from a critical-infrastructure operator, necessity beyond ordinary red-team work, stringent security review and provider decision |
| Government supplier in Brazil | Technical evidence and sample deliverables | Verified legal/tax registration, procurement eligibility, applicable legal/privacy obligations and an awarded/authorized contract |
| External research recognition | Reproducible local work | Independent accepted patch/disclosure, third-party review or legally issued credential |

**Control families for future work, not compliance claims:** secure development lifecycle (NIST SSDF), risk and systems controls (NIST SP 800-53), AppSec maturity (OWASP SAMM), privacy requirements (LGPD) and, when appropriate, independent audits.

## Responsible engagement

Before any third-party test: verify owner authority and approved scope, sign rules of engagement, identify data classes and allowed methods, specify point of contact and incident stop conditions, and keep sensitive evidence only in an owner-approved private environment. Written authorization is essential, and a public GitHub repository never confers it.

- [Authorization boundaries](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md)
- [Sample rules of engagement](https://github.com/skuzu7/CSA-LAB/blob/main/engagement/rules-of-engagement.md)
- [Research milestones](RESEARCH_MILESTONES.md)
- [Reviewer guide](REVIEWER_GUIDE.md)

**External milestones to earn:** a security patch accepted by an independent maintainer; a vulnerability report acknowledged by an authorized program; independently reviewed model-security measurements with a disclosed methodology; verifiable organizational controls and contracts. **None are declared achieved here.**
