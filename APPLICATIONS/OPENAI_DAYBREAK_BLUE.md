# OpenAI Daybreak Blue — Individual Defensive Research Statement

**Status:** researcher-authored application draft; **not submitted** and **not an approval claim**.  
**Applicant:** Antonio Caetano ([@skuzu7](https://github.com/skuzu7)), Brazil.  
**Institutional affiliation:** none (applicant-reported).  
**Academic publications:** none (applicant-reported).

> **Access boundary (official rules checked 2026-11-14).** The individual application path is for **Daybreak Blue**. OpenAI's current FAQ says Daybreak Red is available only to approved business and enterprise organizations and cannot be requested through the individual application flow; Blue approval does not include Red. With no reported institutional/business affiliation, do not submit as an organization or claim Red eligibility. Sources: [Daybreak overview](https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview) · [troubleshooting and individual FAQ](https://help.openai.com/en/articles/20001259-troubleshooting-openai-daybreak).

## Proposed defensive use case

I want to use Daybreak Blue for authorized vulnerability discovery and validation, remediation, threat modeling and defensive investigation on first-party applications and explicitly permitted open-source projects. I use a reproducible workflow: define written authorization, model trust boundaries, analyze code, develop a minimal test, validate a fix, and record results and limitations. My goal is to improve practical AI-assisted security reviews without turning untrusted model outputs into execution authority.

## Why this is concrete

My public [CSA-LAB](https://github.com/skuzu7/CSA-LAB) maintains six intentionally vulnerable educational cases with patched versions and test/CI evidence. The [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) project provides 12 matched benign/attack pairs (24 synthetic cases) for evaluating the **actions proposed by AI models**, an independent host-side tool policy, JSON scoring, optional OpenAI and Anthropic API adapters, and offline tests. The earlier [agent-security benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) exercises 19 deterministic host-side policy scenarios. The lab findings are classified with [computed CVSS v3.1 scores and ATT&CK techniques](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md) and covered by [six Sigma rules validated by traffic replay](https://github.com/skuzu7/CSA-LAB/tree/main/detections). These are research prototypes, not third-party incidents or accepted disclosures.

A first-party app, [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs), contains a [STRIDE threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md) and a [scoped code review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md). A dependency advisory in Next.js was addressed in a [reviewable CI-verified update](https://github.com/skuzu7/freeband-nextjs/pull/10). Performance PRs [#23](https://github.com/skuzu7/freeband-nextjs/pull/23) and [#24](https://github.com/skuzu7/freeband-nextjs/pull/24) are merged. The portfolio route's initial JavaScript fell from 1,901 KB to 624 KB (67.2%), with the longest observed task falling from 565 ms to 0 ms in CI. This demonstrates defensive first-party engineering rather than an external bug bounty.

## Flagship AI-agent project

[TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) implements a test-backed multi-step agent workflow under untrusted retrieved content. Its 16 paired cases and 26 offline tests verify host policy, trace-integrity checks and eight controlled denials from a scripted adversarial strategy, with exact [methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md) and reproducible [GitHub Actions](https://github.com/skuzu7/CSA-LAB/pull/14). It supports optional paid-provider model proposals but contains **no public real GPT/Claude evaluation yet**. I want to apply this research discipline to permitted defensive workflows, while keeping all execution permissions outside model control.

## Expected use and measurable outputs

- Review defined authorization/session and dependency trust boundaries in owned applications.
- Compare legitimate tasks with untrusted content attempting to redirect agent tool proposals.
- Triangulate model suggestions using static code review, human decision-making, unit/regression tests and independent CI.
- Record exact model identifiers, dataset versions, denominators, invalid outputs, benign utility and attacker-targeted proposal rates when actual provider evaluations are performed.
- Fix confirmed first-party issues and submit responsibly disclosed, scoped findings or reviewed open-source patches where permitted.

## Guardrails and disclosure ethics

All testing must target owned systems or explicitly authorized programs. Never include real credentials, private third-party material, unauthorized endpoints or external exploit payload execution. AI responses are hypotheses, not verified vulnerability reports. Host-side policy remains separate from model suggestions; potentially sensitive writes require explicit human approval. Any third-party finding should follow responsible disclosure. Synthetic cases cannot be described as paid bounties or independently verified vulnerabilities.

## Individual Daybreak Blue requirements

The official [Daybreak overview](https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview) currently specifies the following individual path:

1. Use an eligible paid ChatGPT plan and be at least 18 years old.
2. Enroll in Advanced Account Security in Settings → Security. It is available only to eligible personal accounts in supported regions; if it is absent from Settings, it is not available for that account.
3. Register at least two secure sign-in methods, including one that works across devices.
4. Include at least one compatible **physical FIDO2 hardware security key**. A software or synced passkey alone does not satisfy the Daybreak hardware-key requirement. Another eligible passkey or hardware key can be the second sign-in method.
5. Save recovery keys privately. Advanced Account Security disables password sign-in, email/SMS sign-in codes, and standard email recovery. Losing all sign-in methods and recovery keys may make the account unrecoverable.
6. Return to the official Daybreak setup flow, finish identity verification, and complete the separate Daybreak key setup.
7. Check the account's live status. Completing setup does not guarantee approval.

Do not send recovery keys, identity documents, hardware-key secrets, or account-security details to ChatGPT, GitHub, or another person. Complete all account steps yourself at [chatgpt.com/cyber](https://chatgpt.com/cyber).

## Why Daybreak Red is not the current application path

OpenAI's current FAQ states that Daybreak Red is available only to approved business and enterprise organizations; it is not available through the individual application process. Some individual exceptions may exist, but the FAQ says there is no direct individual Red application. Daybreak Red also requires separate approval and stronger verification. A personal Blue application cannot be presented as a Red request.

## Honest standing

I have implemented public self-authored defensive projects with executable tests and transparent limitations. I am **not** asserting Daybreak approval, model-specific live security results, external accepted bug bounties, CVEs, or a production security certification. I am seeking access to deepen reproducible defensive research and to make independently reviewable contributions.