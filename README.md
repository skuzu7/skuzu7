# Antonio Caetano

**Application security · AI-agent security · Software engineering — Brazil**

I research web/API security and AI-agent trust boundaries through first-party,
local and expressly authorized work. My projects emphasize reproducible evidence,
root-cause analysis, verified fixes, regression tests and documented limitations.

[**Research and service templates**](https://github.com/skuzu7/CSA-LAB/blob/main/SERVICES.md) ·
[**Sample report**](https://github.com/skuzu7/CSA-LAB/blob/main/reports/sample-assessment-report.md) ·
[**Evidence index**](SECURITY_PORTFOLIO.md) ·
[**LinkedIn**](https://br.linkedin.com/in/antonioccjr) ·
[**Independent reviewer guide**](REVIEWER_GUIDE.md)

## Institutional-grade research discipline (work in progress)

I maintain an [independent-review portfolio](INSTITUTIONAL_PORTFOLIO.md) and a
[reviewer guide](REVIEWER_GUIDE.md) linking security claims to inspectable code,
CI results, test methodology and known limitations. The
[organizational-readiness plan](APPLICATIONS/ORGANIZATIONAL_CVP_READINESS.md)
separates publicly verifiable technical evidence from organizational controls,
permissions and third-party recognition **not evidenced by this portfolio**. The
[CVP Red Team evidence matrix](APPLICATIONS/CVP_RED_TEAM_EVIDENCE_MATRIX.md)
shows exact eligibility routes, verification standards and remaining gaps.



## What I do

- **Web and API security assessment** — manual testing against the OWASP Top 10 and
  API Top 10 classes, reported with root cause, proof, CVSS vector and fix.
- **Fix and retest** — minimal patches plus a regression test per finding that proves
  the flaw is gone and the feature still works.
- **Detection rules** — Sigma rules for each confirmed attack, validated against
  replayed traffic, with false positives and blind spots written down.
- **AI-agent and LLM application review** — threat model of the agent's tools and
  data, prompt-injection test cases, and a host-side authorization gate design.

Any external assessment requires prior written authorization and a defined
[rules-of-engagement process](https://github.com/skuzu7/CSA-LAB/blob/main/engagement/rules-of-engagement.md).
No owner authorization, no third-party testing.

## Evidence you can run

| Work | What it shows | Numbers asserted in CI |
| --- | --- | --- |
| [CSA-LAB](https://github.com/skuzu7/CSA-LAB) — full assessment cycle | Six deliberately planted local weaknesses: reproduction, classification, detection, fixes and retesting | 6 / 6 exploits reproduce · 6 / 6 fixes pass · CVSS v3.1 computed from vectors (6.5 – 8.6) |
| [Detection engineering](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | One Sigma rule per finding, replayed against real requests on the vulnerable and patched builds | 13 / 13 attack requests alerted · 0 / 22 benign alerted · rules parse in pySigma |
| [Adversary emulation plan](https://github.com/skuzu7/CSA-LAB/blob/main/docs/adversary-emulation-plan.md) | Six-step intrusion chain mapped to MITRE ATT&CK with procedure, telemetry, detection and control per step | Every cell backed by a test |
| [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) — AI-agent tool-use security | Multi-step replay where the host, not the model, authorizes each tool action; hash-chained traces | 16 paired cases · 26 tests · 8 / 8 scripted off-scope requests denied |
| [Scoped agent evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) and [tool-boundary benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | Prompt-injection proposal scoring and policy-gate checks, offline and deterministic | 24 cases · 14 tests · 19 / 19 policy decisions |
| [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) — hardening a real application | [STRIDE threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md), [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), [Next.js advisory remediation](https://github.com/skuzu7/freeband-nextjs/pull/10) | CI-verified dependency fix |

**Scope of these claims.** This is lab and first-party work on my own code with
synthetic data. The AI-agent figures come from scripted controls, not from a live
model. These documents do not establish an externally credited CVE, a bounty award,
a paid client engagement, an offensive certification or any restricted programme tier;
account-level access status must be checked in the provider's portal. The
[reviewer guide](REVIEWER_GUIDE.md) maps each claim to what you can inspect, and
[milestones](RESEARCH_MILESTONES.md) lists what is not yet demonstrated.

## Other engineering work

[TranslatePDF](https://github.com/skuzu7/TranslatePDF) — layout-aware PDF translation ·
[Shopping-Cart-Project](https://github.com/skuzu7/Shopping-Cart-Project) — commerce engineering ·
[Portfolio](https://github.com/skuzu7/Portfolio) — web portfolio

**Tech:** Python · TypeScript · Next.js · Rust · SQL · Docker · GitHub Actions

**Contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr)
