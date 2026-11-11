# Security Research — Independent Reviewer Guide

**Maintainer:** Antonio Caetano ([skuzu7](https://github.com/skuzu7))  
**Scope:** defensive AppSec on first-party code and local, intentionally vulnerable fixtures.  
**Status:** public evidence dossier; **not** proof of third-party accreditation, CVE attribution, bug-bounty acceptance, or approval to Anthropic/OpenAI cyber-access programs.

This document maps each claim to material a reviewer can inspect without trusting a biography, screenshot or claimed badge.

## Evidence matrix

| Capability | Direct evidence | What can be checked | Honest limitation |
| --- | --- | --- | --- |
| Vulnerability analysis | [CSA-LAB write-ups](https://github.com/skuzu7/CSA-LAB/tree/main/writeups) | Six intentionally planted issues with cause, minimal reproduction and fixes | Synthetic first-party scenarios only |
| Responsible scope | [Lab authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md) and [target inventory](https://github.com/skuzu7/CSA-LAB/blob/main/docs/scope.md) | Exactly what targets are authorized and excluded | No independent external scope approval is implied |
| Patch validation | [Vulnerable-case tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/security/test_findings_vulnerable.py) and [regressions](https://github.com/skuzu7/CSA-LAB/blob/main/tests/regression/test_fixes.py) | Six controlled demonstrations and six post-fix assertions | Passing source-level tests are not the same as an externally reviewed security assessment |
| CI reproducibility | [Proposed CI and runner correction](https://github.com/skuzu7/CSA-LAB/pull/2) and [Actions history](https://github.com/skuzu7/CSA-LAB/actions) | Whether tests actually execute successfully in CI | The PR must pass its checks and be merged before main-branch reproducibility is claimed |
| Production-oriented secure engineering | [freeband-nextjs STRIDE model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) and [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) | Auth/session trust boundaries, tests, findings, mitigations and known weaknesses | Scoped first-party review; not a commissioned or external audit |
| Engineering automation | [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian) | MCP integration, tests and documentation for controlled browser QA | Browser-automation capability is not evidence of authorized penetration tests |

## Five-minute verification path

1. Read [CSA-LAB authorization](https://github.com/skuzu7/CSA-LAB/blob/main/AUTHORIZATION.md) to establish ownership, limits and non-goals.
2. Inspect [FINDING-004](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-004.md) and [FINDING-006](https://github.com/skuzu7/CSA-LAB/blob/main/writeups/finding-006.md), including their root causes, remediations, regressions and residual limitations.
3. Inspect the [tests for intentionally vulnerable behavior](https://github.com/skuzu7/CSA-LAB/blob/main/tests/security/test_findings_vulnerable.py) alongside the [post-fix tests](https://github.com/skuzu7/CSA-LAB/blob/main/tests/regression/test_fixes.py).
4. Check [CSA-LAB PR #2](https://github.com/skuzu7/CSA-LAB/pull/2) and its checks for a reproducible local/CI runner; do not mistake a workflow YAML file for a successful test run.
5. Review [freeband-nextjs SECURITY_REVIEW](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), noting both implemented controls and open limitations.

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

1. Merge only after the CSA-LAB local/CI runner passes all planted-case and patch-regression checks.
2. Add machine-readable test reports and a concise failure/limitations matrix.
3. Contribute real, scoped fixes to third-party open-source projects via reviewed PRs and follow coordinated disclosure norms.
4. Publish accepted, non-confidential vulnerability/advisory references **only if** they actually occur and disclosure is permitted.
5. Maintain a transparent change log and state whether each result is self-tested, CI-tested, maintainer-reviewed or externally accepted.

**Public contact:** [LinkedIn](https://br.linkedin.com/in/antonioccjr).
