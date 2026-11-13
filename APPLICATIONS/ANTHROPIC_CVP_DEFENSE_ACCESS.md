# Anthropic Cyber Verification Program — Defense Access

**Status:** researcher-authored application statement draft; **not submitted** and **not evidence of approval**.  
**Applicant:** Antonio Caetano ([@skuzu7](https://github.com/skuzu7)), independent software engineer and defensive security researcher.

> **Eligibility check before submitting (updated 2026-11-13).** Anthropic's expanded programme has three tiers. Individual researchers can apply only for Defense Access, and the published criterion is a track record of reported vulnerabilities; Red Team Access is for organizations. This draft does not yet meet that criterion: no externally accepted report exists (see the last line). Do not submit until at least one accepted report or reviewed upstream security patch can be cited.

## Concise research statement

I conduct security research on software I own or have explicit permission to test, prioritizing reviewable root-cause analysis and verifiable fixes. My public [CSA-LAB](https://github.com/skuzu7/CSA-LAB) contains six intentionally planted application vulnerabilities, written scope, controlled reproduction, corresponding patches and regression checks run under GitHub Actions. My [19-case offline agent policy benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) exercises host-side constraints on AI-agent tool permissions. My [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) adds 24 synthetic, matched benign/attack scenarios, a documented methodology, optional model adapters, offline unit tests, and reproducible CI reporting.

My primary next-step research project is [TRACEGUARD — Agent Replay Lab](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab), a bounded multi-step AI-agent tool security experiment. It provides 16 matched synthetic benign/attack cases, 26 offline tests, a separate host-side authorization layer, tamper-evident (non-authenticated) hash-linked traces, and a CI-verifiable positive control that denies eight deliberately proposed out-of-scope actions. This demonstrates a reproducible **research harness**, not real Claude model robustness, and motivates a responsible, permissioned future evaluation with real models.

I am requesting individual **Defense Access** to support authorized defensive review, vulnerability triage, verification of remediation, and AI-assisted evaluation of agent trust boundaries. I intend to produce **public, reproducible defensive artifacts**: minimal root-cause demonstrations, unit/regression tests, scoped threat models, reviews of generated patches, and redacted research notes. I will not use access as a substitute for authorization.

## Exact planned workflow

1. Define the target and authorization, record relevant assets and threat boundaries.
2. Analyze only first-party or permitted source code and approved sanitized logs, with an explicit list of allowed files/tools.
3. Ask the model for hypotheses, risk explanations, safe reproductions and patches **for researcher review**.
4. Reproduce findings on a localhost fixture or explicitly permitted test environment, record negative controls, and compare vulnerable and patched behavior.
5. Independently validate results with local and CI tests. Use a host-side allowlist and human approval for write operations.
6. Publish sanitized, reproducible lessons; disclose any real third-party issue privately to its maintainer under the program's rules.

## Inspectable evidence

| Claim | Evidence | Important limitation |
| --- | --- | --- |
| Application vulnerability research | [Six documented findings](https://github.com/skuzu7/CSA-LAB/tree/main/writeups) and [test suites](https://github.com/skuzu7/CSA-LAB/tree/main/tests) | Deliberately planted first-party issues |
| Reproducibility | [CSA-LAB CI](https://github.com/skuzu7/CSA-LAB/actions) | CI is not independent external review |
| Severity and detection discipline | [Computed CVSS v3.1 and ATT&CK mapping](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md), [six Sigma rules with a replay scorer](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | In-sample check on a 35-request synthetic corpus |
| Agent authorization | [19-case policy checks](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | No actual LLM in those checks |
| Prompt-injection research protocol | [24-case matched eval](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) | No live-model benchmark results yet |
| Real first-party engineering | [Threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md), [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) | Not a commissioned audit |

## Responsible use and transparency

I will not scan third-party production systems, access real credentials, automate unauthorized exploitation, or repurpose restricted research access for third-party customers. I will keep model-generated proposals separate from the host's authorization decision and require human review before sensitive actions. I do **not** claim accepted external bounties, CVEs, professional penetration-testing credentials, institutional affiliation, special-program membership, or independent validation that is not actually documented.

## Remaining applicant-controlled steps

Confirm the current [Anthropic CVP tiers, eligibility and security requirements](https://support.claude.com/en/articles/14604842) and the [programme announcement](https://anthropic.com/news/cyber-verification-program), complete the official identity/security flow on the applicant's own account, and supply any private details only through the official program portal. The public text here is an evidence-backed statement, **not** a completed application.

**Current maturity:** authentic synthetic proof-of-work with strong reproducibility; independent public-source contribution or accepted external defensive report remains a research goal.
