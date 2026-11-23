# Cyber research access — public evidence index

**Author:** Antonio Caetano ([@skuzu7](https://github.com/skuzu7))  
**Last public review:** 2026-11-23  
**Status:** research portfolio and application-preparation documents only — **not a verified approval, certification, affiliation, or application submission.**

This index exists for human reviewers of authorized cybersecurity research. Every positive claim should be traceable to source code, tests, methods, or a third-party issuer. Lab-only work must never be described as an accepted vulnerability disclosure.

## Start with independent evidence (5 minutes)

1. **[CSA-LAB](https://github.com/skuzu7/CSA-LAB)** — six intentionally vulnerable local fixtures, minimal reproductions, fixes, regression tests, detection rules and [running CI](https://github.com/skuzu7/CSA-LAB/actions).
2. **[TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab)** — 16 paired synthetic scenarios, 26 offline tests, host-side authorization and documented [methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md). These are scripted controls, **not** live-model security results.
3. **[Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals)** — 24 synthetic scenarios, 14 tests and a [results ledger](https://github.com/skuzu7/CSA-LAB/blob/main/agent_evals/RESULTS.md).
4. **[freeband-nextjs](https://github.com/skuzu7/freeband-nextjs)** — first-party application threat modeling, [documented security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), mitigation and CI.
5. **[Reviewer guide](../REVIEWER_GUIDE.md)** and **[public evidence index](../SECURITY_PORTFOLIO.md)** — claim-by-claim paths and limitations.

## Program-specific documentation

| Program and requested level | Who can apply | Current public evidence | Boundaries and gaps |
| --- | --- | --- | --- |
| [Anthropic CVP Defense](ANTHROPIC_CVP_DEFENSE_ACCESS.md) | Individuals and organizations | First-party AppSec and synthetic agent-security research | Individual account verification, controls and provider decision are private; no externally accepted disclosure is documented here |
| [Anthropic CVP Red Team](CVP_RED_TEAM_EVIDENCE_MATRIX.md) | Organizations only | Research methods and sample service templates | Actual organization route, authorized engagement, personnel and security controls **not publicly verified** |
| [Anthropic CVP Specialized](CVP_SPECIALIZED_EVIDENCE_MATRIX.md) | Authorized organizations doing high-risk testing of systemically important infrastructure | Only general first-party research so far | Critical-infrastructure authorization and need beyond Red Team **not evidenced** |
| [OpenAI Daybreak Blue](OPENAI_DAYBREAK_BLUE.md) | Eligible individuals and organizations | First-party defensive research and code review | Required hardware key, Advanced Account Security, identity and approval cannot be confirmed from GitHub |
| [OpenAI Daybreak Red](DAYBREAK_RED_ORGANIZATIONAL_READINESS.md) | Approved business/enterprise organizations; no direct individual application | Research portfolio, not organization approval | Separate organizational validation and access controls **not verified** |

**Provider rules checked 2026-11-23:** [Anthropic tiers](https://support.claude.com/en/articles/14604842-cyber-verification-program), [Anthropic security requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements), [OpenAI Daybreak](https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview). Provider rules and eligible model access can change: verify the live portal at submission.

## Proof standard

For each achievement, document **claim → who performed it → scope/authorization → evidence link or issuer → date → what it does not establish**. Independent validation should be separated from local CI execution. Examples:

- A merged **self-authored** pull request demonstrates shipped first-party changes, **not** third-party acceptance.
- Six planted vulnerabilities and green tests demonstrate reproducible lab work, **not** six discovered production CVEs.
- A local scripted denial demonstrates an offline policy gate, **not** a benchmark of Claude or GPT's live resilience.
- An independent maintainer's accepted security patch or an in-scope, publicly citable program-accepted report is stronger external evidence **only after it actually exists**.

## Privacy and responsible use

Never put identity documents, account recovery codes, security keys, private disclosures, customer contracts, internal network diagrams, personally identifying incident data, or credentials in public GitHub. Sensitive evidence belongs in the providers' official verification flows or in access-controlled records with disclosure permission. External testing requires owner permission and written scope.

**Next research milestone:** independently reviewed defensive contribution to a third-party project, with a documented threat model, reproducible test, minimal fix, maintainer approval, and explicit public disclosure permission.
