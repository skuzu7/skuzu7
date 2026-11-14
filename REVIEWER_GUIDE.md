# Security Research — Independent Reviewer Guide

**Maintainer:** Antonio Caetano ([skuzu7](https://github.com/skuzu7))  
**Scope:** defensive AppSec on first-party code and local, intentionally vulnerable fixtures.  
**Status:** public evidence dossier; **not** proof of third-party accreditation, CVE attribution, bug-bounty acceptance, or approval to Anthropic/OpenAI cyber-access programs.

This document maps each claim to material a reviewer can inspect without trusting a biography, screenshot or claimed badge.

## Evidence matrix

| Capability | Direct evidence | What can be checked | Honest limitation |
| --- | --- | --- | --- |
| **Multi-step agent security research** | [TRACEGUARD source](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab), [26 offline tests](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/tests/test_replay.py), [CI PR #14](https://github.com/skuzu7/CSA-LAB/pull/14), [threat model](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/THREAT_MODEL.md) | 16 matched synthetic cases, bounded agent action sequence, strict host tool authorization, eight intentionally denied off-scope actions and hash-linked logs | Scripted controls only; no empirical real-model exploit/safety statistics or external review |
| Vulnerability analysis | [CSA-LAB write-ups](https://github.com/skuzu7/CSA-LAB/tree/main/writeups) | Six intentionally planted issues with cause, minimal reproduction and fixes | Synthetic first-party scenarios only |
| Responsible scope | [Lab authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md) and [target inventory](https://github.com/skuzu7/CSA-LAB/blob/main/docs/scope.md) | Exactly what targets are authorized and excluded | No independent external scope approval is implied |
| Classification and severity | [classification.md](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md), [CVSS calculator](https://github.com/skuzu7/CSA-LAB/blob/main/classification/cvss31.py), [tests](https://github.com/skuzu7/CSA-LAB/blob/main/classification/tests/test_classification.py) | CWE, OWASP, ATT&CK and CVSS v3.1 per finding; every score derived from its vector and checked against published reference vectors | Scores rate the weakness as if internet-facing; the fixture's real risk is nil. ATT&CK mapping is analyst judgement |
| Detection engineering | [Sigma rules](https://github.com/skuzu7/CSA-LAB/tree/main/detections/rules), [labelled traffic](https://github.com/skuzu7/CSA-LAB/blob/main/detections/traffic.jsonl), [replay scorer](https://github.com/skuzu7/CSA-LAB/blob/main/detections/validate.py) | 13/13 attack requests alerted and 0/22 benign alerted on both builds; rules load in pySigma | Rules and corpus share an author: an in-sample regression harness, not a measure of efficacy on unseen traffic |
| Patch validation | [Vulnerable-case tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/security/test_findings_vulnerable.py) and [regressions](https://github.com/skuzu7/CSA-LAB/blob/main/tests/regression/test_fixes.py) | Six controlled demonstrations and six post-fix assertions | Passing source-level tests are not the same as an externally reviewed security assessment |
| CI reproducibility | [Merged CI runner correction](https://github.com/skuzu7/CSA-LAB/pull/2) and [Actions history](https://github.com/skuzu7/CSA-LAB/actions) | Local vulnerable/patch regressions ran successfully under GitHub Actions | Passing CI is not third-party validation or proof of complete vulnerability coverage |
| Tool-boundary authorization for AI agents | [Merged offline benchmark](https://github.com/skuzu7/CSA-LAB/pull/3) and [methodology](https://github.com/skuzu7/CSA-LAB/blob/main/agent_security/README.md) | 19 synthetic allow/deny policy assertions, structured report, first-party CI | No live model, prompt-injection robustness rate or production sandbox claim |
| Scoped agent action-proposal evaluation | [Merged 24-case research harness](https://github.com/skuzu7/CSA-LAB/pull/11) and [methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/METHODS.md) | 12 paired benign/attack fixtures, 14 offline tests, separate host authorization, JSON scoring and optional real provider adapters | A deterministic baseline is **not** an LLM vulnerability or robustness score; no live runs yet |
| Production-oriented secure engineering | [freeband-nextjs STRIDE model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) and [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) | Auth/session trust boundaries, tests, findings, mitigations and known weaknesses | Scoped first-party review; not a commissioned or external audit |
| Dependency advisory remediation | [Next.js correction PR](https://github.com/skuzu7/freeband-nextjs/pull/10) and [case-study PR](https://github.com/skuzu7/freeband-nextjs/pull/19) | A critical advisory detected in CI, patched dependency+lockfile and passing full validation |
| Browser/MCP data handling | [CSA-Obsidian PR #4 merged](https://github.com/skuzu7/CSA-Obsidian/pull/4), [follow-up PR #5](https://github.com/skuzu7/CSA-Obsidian/pull/5) | PR #4 implements request/header and cookie redaction, origin-only URL capture, session-path validation and service-specific token-task removal. PR #5 adds fail-closed HTTP(S) host routing and Windows ACLs; Linux and Windows CI passed | Browser policy is not an OS sandbox or IP-level firewall; DNS rebinding and direct Python APIs remain outside this boundary | Does not prove a successful exploit or that the production deployment updated |

## Five-minute verification path

1. Inspect [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab), its [measurements](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md), and [successful CI checks](https://github.com/skuzu7/CSA-LAB/pull/14). The eight denied actions are produced by a scripted control, not a real LLM test.
2. Read [CSA-LAB authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md) to establish ownership, limits and non-goals.
3. Inspect [FINDING-004](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-004.md) and [FINDING-006](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-006.md), including their root causes, remediations, regressions and residual limitations.
4. Inspect the [tests for intentionally vulnerable behavior](https://github.com/skuzu7/CSA-LAB/blob/main/tests/security/test_findings_vulnerable.py) alongside the [post-fix tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/regression/test_fixes.py).
5. Run or read the [detection replay](https://github.com/skuzu7/CSA-LAB/tree/main/detections) and the [classification page](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md); both are regenerated and asserted in [CI](https://github.com/skuzu7/CSA-LAB/actions/workflows/ci.yml).
6. Check the successful [CI runner PR #2](https://github.com/skuzu7/CSA-LAB/pull/2), [offline policy benchmark PR #3](https://github.com/skuzu7/CSA-LAB/pull/3) and actual [Actions history](https://github.com/skuzu7/CSA-LAB/actions). Review results as self-authored code with executed CI—not as external validation.
7. Inspect [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals), including its [dataset](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/cases.jsonl), [14 tests](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/test_evaluate.py) and [results ledger](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/RESULTS.md). The [scripted positive control](https://github.com/skuzu7/CSA-LAB/pull/12) intentionally proposes all 12 attacker targets, all denied by the host. No model scores should be inferred from either synthetic control.
8. Review [freeband-nextjs SECURITY_REVIEW](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), noting controls and open limitations.

## Research purpose and intended authorized workflows

I am developing an evidence-first defensive security practice around my own applications, test fixtures and software I am expressly permitted to assess. I use AI assistance for:

- Threat modeling of first-party applications and agent integrations.
- Static inspection and triage of security-relevant code paths.
- Controlled reproduction of vulnerabilities on localhost-owned fixtures.
- Root-cause analysis, minimal remediation and regression-test design.
- Comparison and review of agent-generated fixes, with human validation.
- Redacted findings and responsible coordination with maintainers when a genuine externally reportable issue is discovered.

The intended outputs are **defensive artifacts**: a precise finding, a reproducible test, a verified patch, a limitations section and a reviewable commit or pull request. Test targets and methods must remain within their governing scope. The researcher retains responsibility for all actions; AI access is not a substitute for authorization.

## Claims that are *not* made

- No claim of Anthropic CVP, OpenAI Daybreak or other restricted-program membership.
- No assertion of currently accepted bug-bounty reports, paid rewards or assigned CVEs.
- No claim that educational findings are discoveries in third-party production systems.
- No claim that GitHub Actions succeeded until individual run logs show success.
- No claim that automated or AI-assisted reviews replace expert testing.

## Next independently verifiable milestones

1. Continue testing and reviewing the merged CSA-LAB local/CI runner and its 19-case policy benchmark; track newly discovered edge cases as reproducible regressions.
2. Independently review and extend the newly published 24-case evaluation harness, then run it on actual models only with proper permission, reproducibility and report provenance before claiming model security measurements.
3. Contribute real, scoped fixes to third-party open-source projects via reviewed PRs and follow coordinated disclosure norms.
4. Publish accepted, non-confidential vulnerability/advisory references **only if** they actually occur and disclosure is permitted.
5. Maintain a transparent change log and state whether each result is self-tested, CI-tested, maintainer-reviewed or externally accepted.

**Research plan:** [Evidence milestones](RESEARCH_MILESTONES.md).

**Public contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr).
