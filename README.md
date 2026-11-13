# Antonio Caetano

**Application security · AI-agent security · Software engineering — Brazil**

I test web applications, APIs and AI-agent integrations, and I hand engineering
teams something they can act on: reproducible findings, computed severity, fixes
with regression tests, and detection rules for what was found.

[**Services**](https://github.com/skuzu7/CSA-LAB/blob/main/SERVICES.md) ·
[**Sample report**](https://github.com/skuzu7/CSA-LAB/blob/main/reports/sample-assessment-report.md) ·
[**Evidence index**](SECURITY_PORTFOLIO.md) ·
[**LinkedIn**](https://br.linkedin.com/in/antonioccjr)

## What I do

- **Web and API security assessment** — manual testing against the OWASP Top 10 and
  API Top 10 classes, reported with root cause, proof, CVSS vector and fix.
- **Fix and retest** — minimal patches plus a regression test per finding that proves
  the flaw is gone and the feature still works.
- **Detection rules** — Sigma rules for each confirmed attack, validated against
  replayed traffic, with false positives and blind spots written down.
- **AI-agent and LLM application review** — threat model of the agent's tools and
  data, prompt-injection test cases, and a host-side authorization gate design.

Every engagement starts with signed
[rules of engagement](https://github.com/skuzu7/CSA-LAB/blob/main/engagement/rules-of-engagement.md).
No written authorization from the system owner, no testing.

## Evidence you can run

| Work | What it shows | Numbers asserted in CI |
| --- | --- | --- |
| [CSA-LAB](https://github.com/skuzu7/CSA-LAB) — full assessment cycle | Six vulnerabilities taken from authorization to report: exploit, classify, detect, fix, retest | 6 / 6 exploits reproduce · 6 / 6 fixes pass · CVSS v3.1 computed from vectors (6.5 – 8.6) |
| [Detection engineering](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | One Sigma rule per finding, replayed against real requests on the vulnerable and patched builds | 13 / 13 attack requests alerted · 0 / 22 benign alerted · rules parse in pySigma |
| [Adversary emulation plan](https://github.com/skuzu7/CSA-LAB/blob/main/docs/adversary-emulation-plan.md) | Six-step intrusion chain mapped to MITRE ATT&CK with procedure, telemetry, detection and control per step | Every cell backed by a test |
| [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) — AI-agent tool-use security | Multi-step replay where the host, not the model, authorizes each tool action; hash-chained traces | 16 paired cases · 26 tests · 8 / 8 scripted off-scope requests denied |
| [Scoped agent evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) and [tool-boundary benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | Prompt-injection proposal scoring and policy-gate checks, offline and deterministic | 24 cases · 14 tests · 19 / 19 policy decisions |
| [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) — hardening a real application | [STRIDE threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md), [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), [Next.js advisory remediation](https://github.com/skuzu7/freeband-nextjs/pull/10) | CI-verified dependency fix |

**Scope of these claims.** This is lab and first-party work on my own code with
synthetic data. The AI-agent figures come from scripted controls, not from a live
model. I do not claim a CVE, a bug-bounty award, a client engagement, a
certification or membership of any vendor access programme. The
[reviewer guide](REVIEWER_GUIDE.md) maps each claim to what you can inspect, and
[milestones](RESEARCH_MILESTONES.md) lists what is not yet demonstrated.

## Other engineering work

[TranslatePDF](https://github.com/skuzu7/TranslatePDF) — layout-aware PDF translation ·
[Shopping-Cart-Project](https://github.com/skuzu7/Shopping-Cart-Project) — commerce engineering ·
[Portfolio](https://github.com/skuzu7/Portfolio) — web portfolio

**Tech:** Python · TypeScript · Next.js · Rust · SQL · Docker · GitHub Actions

**Contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr)
