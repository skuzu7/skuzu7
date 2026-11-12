# Antonio Caetano

**Software Engineer · Defensive Application Security · Brazil**

I build and review software with an evidence-first security workflow: **written scope → threat model → controlled reproduction → root cause → remediation → regression test → reviewable documentation**.

[**Security evidence index**](SECURITY_PORTFOLIO.md) · [**Five-minute reviewer guide**](REVIEWER_GUIDE.md) · [**GitHub**](https://github.com/skuzu7) · [**LinkedIn**](https://br.linkedin.com/in/antonioccjr)

## Selected security work

| Project | Inspectable artifacts | What they demonstrate |
| --- | --- | --- |
| [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | [Six local case studies](https://github.com/skuzu7/CSA-LAB/tree/main/writeups), [authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md), [vulnerable tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/security/test_findings_vulnerable.py), [regression tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/regression/test_fixes.py) | Intentionally planted IDOR, SQLi, path traversal, session forgery, business-logic flaw and SSRF; controlled validation and patch checks |
| [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) | [STRIDE threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md), [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), [CI workflow](https://github.com/skuzu7/freeband-nextjs/blob/main/.github/workflows/ci.yml) | First-party authentication/session hardening, secure code review, test coverage and documented residual risks |
| [Agent tool-boundary benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | [Offline policy harness](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/offline_benchmark.py), [methodology and limitations](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/README.md), [CI artifacts](https://github.com/skuzu7/CSA-LAB/actions) | 19 synthetic, reproducible allow/deny checks for host-approved agent tools; **not** a live LLM prompt-injection benchmark |

**Reproducibility:** [CSA-LAB CI correction PR #2](https://github.com/skuzu7/CSA-LAB/pull/2) and [agent tool-boundary benchmark PR #3](https://github.com/skuzu7/CSA-LAB/pull/3) are merged; both associated GitHub Actions checks passed. The agent test suite has 19 **synthetic, deterministic policy cases**, not 19 real-world vulnerabilities or an LLM jailbreak score. [Methodology and limits](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/README.md).

## Security research focus

- Application-security triage, authorization and session-boundary reviews.
- Defensive vulnerability reproduction and patch verification on owned/local fixtures.
- Threat modeling and test design for first-party web applications and AI-agent workflows.
- Human-reviewed, auditable AI assistance in security engineering.

**Research boundaries:** No unsanctioned scanning, exploitation of third-party systems or access to real credentials/data. The CSA-LAB exercises are deliberately constructed and are **not** external pentest findings, CVEs, paid bounties or professional certifications. I make no claim of privileged-access-program approval. See the [evidence and limitations guide](REVIEWER_GUIDE.md).

## Other engineering work

[TranslatePDF](https://github.com/skuzu7/TranslatePDF) — layout-aware PDF translation · [Shopping-Cart-Project](https://github.com/skuzu7/Shopping-Cart-Project) — commerce engineering · [Portfolio](https://github.com/skuzu7/Portfolio) — web portfolio · [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian) — browser QA automation for authorized environments

**Tech:** Python · TypeScript · Next.js · Rust · SQL · Docker · GitHub Actions

**Contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr)
