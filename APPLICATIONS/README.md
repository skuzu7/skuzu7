# Research Access Applications — Evidence Pack

**Applicant:** Antonio Caetano ([`@skuzu7`](https://github.com/skuzu7))  
**Profile:** independent software engineer and defensive security researcher, Brazil  
**Institutional affiliation:** none (applicant-reported)  
**Academic publications:** none (applicant-reported)  
**Status:** preparation only — neither application below is submitted, approved, or endorsed by the provider.  
**Official requirements checked:** 2026-11-14.

This index is a navigation and readiness document. It does not claim eligibility, certification, program membership, accepted vulnerability reports, client engagements, or independent validation.

## Application drafts

| Program | Draft | Current disposition |
| --- | --- | --- |
| Anthropic Cyber Verification Program — Defense Access | [Research statement](ANTHROPIC_CVP_DEFENSE_ACCESS.md) | **Hold before submission.** The current evidence pack demonstrates self-authored labs and first-party defensive engineering, but does not document an independently accepted vulnerability report. Re-check the official eligibility criteria and required evidence immediately before applying. |
| OpenAI Daybreak Blue — Individual | [Research statement](OPENAI_DAYBREAK_BLUE.md) | **Preparation only.** The repository cannot verify account-level eligibility or security settings. The applicant must complete any required account, identity, and hardware-key checks directly through the official flow. |

## Official programme references checked on 2026-11-14

- **Anthropic CVP:** [Help Center — tiers, individual eligibility and access](https://support.claude.com/en/articles/14604842-cyber-verification-program); [6 October 2026 programme announcement](https://www.anthropic.com/news/cyber-verification-program). The announcement identifies individual researchers with a track record of reported vulnerabilities among examples of qualifying Defense Access applicants. Red Team and Specialized Access are organization-only.
- **OpenAI Daybreak:** [Trusted Access for Cyber overview](https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview); [troubleshooting and account requirements](https://help.openai.com/en/articles/20001259-troubleshooting-openai-daybreak). Individual access requires an eligible paid plan, Advanced Account Security, two secure sign-in methods (including one that works across devices), and at least one compatible physical FIDO2 key; identity verification and approval are separate steps, and regional availability may vary.

## Evidence reviewers can inspect

| Capability | Evidence | Scope and limitation |
| --- | --- | --- |
| Application-security research | [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | Six deliberately planted findings in a local, synthetic fixture; patches, regression tests, write-ups, and CI. Not third-party vulnerability discoveries. |
| Multi-step AI-agent tool-use security | [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) | 16 paired synthetic cases, 26 offline tests, and eight scripted off-scope denials. No real-model robustness result. |
| Agent action-proposal evaluation | [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) | 24 synthetic cases and 14 offline tests. No live provider evaluation has been recorded. |
| Host-side tool authorization | [Agent security benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | 19 deterministic synthetic policy decisions; no LLM is involved in this benchmark. |
| Detection engineering | [Sigma detections](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | Six rules replayed against a small labelled synthetic corpus; in-sample results are not production detection efficacy. |
| First-party secure engineering | [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) | Threat model, scoped security review, tests, and a first-party dependency remediation. Not a commissioned external audit. |

For claim-by-claim evidence and reproduction instructions, see [SECURITY_PORTFOLIO.md](../SECURITY_PORTFOLIO.md) and [REVIEWER_GUIDE.md](../REVIEWER_GUIDE.md).

## Applicant facts to confirm before submission

The following items must be completed by the applicant from verifiable records. Blank or unverified items must not be converted into positive claims.

- [ ] Certifications: names, issuer, date, and verification URL, or explicitly state none.
- [ ] External vulnerability disclosures: program/vendor, report identifier, acceptance status, disclosure permission, and public reference where permitted; otherwise state none.
- [ ] Client or professional security engagements: scope, authorization, dates, role, and references that may legally be disclosed; otherwise state none.
- [ ] Upstream open-source security contributions: PR URL, maintainer review/acceptance status, and exact contribution.
- [ ] Account-level requirements for each program: verify personally in the provider's official portal; never publish recovery codes, identity documents, hardware-key secrets, or account security details.
- [ ] Contact details and any organization/business information only if the official application asks for them.

## Submission rules

1. Verify the provider's current official eligibility and program rules on the date of submission.
2. Keep synthetic, first-party, independently reviewed, and externally accepted evidence clearly separated.
3. Do not claim real-model results unless a reproducible run records provider, model/version, dataset version, trial count, raw outcomes, negative controls, and limitations.
4. Do not claim a CVE, bounty, client engagement, certification, institutional affiliation, or program approval without documentary evidence.
5. Submit personal identity and account-security information only through the provider's official application flow.
6. Keep this public repository free of secrets, private reports, client data, and sensitive account information.

## Next evidence milestones

1. Obtain an independently reviewed and accepted upstream defensive contribution, or a properly authorized and accepted vulnerability report.
2. Add a real-model agent evaluation with explicit permission, a preregistered protocol, repeated trials, negative controls, and complete provenance.
3. Publish only redacted results whose disclosure is permitted.
4. Reassess program eligibility against the current official rules before submitting either application.

**Last prepared:** 2026-11-14.  
**No application has been submitted by this repository change.**
