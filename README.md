# Antonio Caetano

**Defensive Application Security · Agentic AI Security Research · Software Engineering · Brazil**

I build and review software with an evidence-first security workflow: **written scope → threat model → controlled reproduction → root cause → remediation → regression test → reviewable documentation**.

[**Security evidence index**](SECURITY_PORTFOLIO.md) · [**Five-minute reviewer guide**](REVIEWER_GUIDE.md) · [**GitHub**](https://github.com/skuzu7) · [**LinkedIn**](https://br.linkedin.com/in/antonioccjr)

## Selected security work

| Project | Inspectable artifacts | What they demonstrate |
| --- | --- | --- |
| [**TRACEGUARD — Agent Replay Lab**](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) | [26 offline tests](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/tests/test_replay.py), [16 paired scenarios](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/scenarios.jsonl), [host-side enforcement](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/core.py), [methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md), [CI reports](https://github.com/skuzu7/CSA-LAB/actions) | Flagship **multi-step** synthetic AI-agent trust-boundary lab: untrusted tool observations, 8 blocked off-scope requests in scripted control, hash-chained traces; **not** a real-model robustness score |
| [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | [Six local case studies](https://github.com/skuzu7/CSA-LAB/tree/main/writeups), [authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md), [vulnerable tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/security/test_findings_vulnerable.py), [regression tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/regression/test_fixes.py) | Intentionally planted IDOR, SQLi, path traversal, session forgery, business-logic flaw and SSRF; controlled validation and patch checks |
| [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) | [STRIDE threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md), [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), [CI workflow](https://github.com/skuzu7/freeband-nextjs/blob/main/.github/workflows/ci.yml), [critical advisory remediation](https://github.com/skuzu7/freeband-nextjs/pull/10), [case-study PR](https://github.com/skuzu7/freeband-nextjs/pull/19) | First-party authentication/session hardening, secure code review, test coverage and documented residual risks |
| [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) | [24 matched benign/attack scenarios](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/cases.jsonl), [14 unit tests](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/test_evaluate.py), [methodology](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/METHODS.md), [GitHub Actions](https://github.com/skuzu7/CSA-LAB/actions) | Offline, reproducible host-policy evaluation with **optional** live OpenAI/Anthropic model adapters. No real-model results claimed. |
| [Agent tool-boundary benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | [Offline policy harness](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/offline_benchmark.py), [methodology and limitations](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/README.md), [CI artifacts](https://github.com/skuzu7/CSA-LAB/actions) | 19 synthetic, reproducible allow/deny checks for host-approved agent tools; **not** a live LLM prompt-injection benchmark |

**Reproducibility:** [CSA-LAB CI runner](https://github.com/skuzu7/CSA-LAB/pull/2), [19-case host policy benchmark](https://github.com/skuzu7/CSA-LAB/pull/3), and the [24-case scoped evaluation PR](https://github.com/skuzu7/CSA-LAB/pull/11) are merged; their GitHub Actions checks passed. These are **synthetic first-party exercises**, not third-party vulnerability findings. A scripted [adversarial positive control](https://github.com/skuzu7/CSA-LAB/pull/12) verifies that the host blocks all 12 attack-goal proposals; it is **not** a live model test. The [TRACEGUARD research PR #14](https://github.com/skuzu7/CSA-LAB/pull/14) is also merged with passing GitHub Actions; its **26 offline tests, 16 synthetic cases and 8 scripted host denials** are reproducible. The optional live model research has **not** yet been run.

## Security research focus

- Application-security triage, authorization and session-boundary reviews.
- Defensive vulnerability reproduction and patch verification on owned/local fixtures.
- Threat modeling, multi-step agent tool-trust boundaries and test design for first-party systems.
- Human-reviewed, auditable AI assistance in security engineering.

**Research boundaries:** No unsanctioned scanning, exploitation of third-party systems or access to real credentials/data. The CSA-LAB exercises are deliberately constructed and are **not** external pentest findings, CVEs, paid bounties or professional certifications. I make no claim of privileged-access-program approval. See the [evidence and limitations guide](REVIEWER_GUIDE.md).

## Independent review and research direction

[Five-minute reviewer guide](REVIEWER_GUIDE.md) · [Evidence index](SECURITY_PORTFOLIO.md) · [Research milestones](RESEARCH_MILESTONES.md)

I maintain application-specific defensive research statements for [Anthropic CVP Defense Access](APPLICATIONS/ANTHROPIC_CVP_DEFENSE_ACCESS.md) and [OpenAI Daybreak Blue](APPLICATIONS/OPENAI_DAYBREAK_BLUE.md). These are **draft research statements, not submitted applications or evidence of program approval**.

## Other engineering work

[TranslatePDF](https://github.com/skuzu7/TranslatePDF) — layout-aware PDF translation · [Shopping-Cart-Project](https://github.com/skuzu7/Shopping-Cart-Project) — commerce engineering · [Portfolio](https://github.com/skuzu7/Portfolio) — web portfolio · [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian) — browser QA automation for authorized environments

**Tech:** Python · TypeScript · Next.js · Rust · SQL · Docker · GitHub Actions

**Contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr)
