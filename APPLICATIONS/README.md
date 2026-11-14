# Research Access Applications — Evidence Pack

**Applicant:** Antonio Caetano ([`@skuzu7`](https://github.com/skuzu7))  
**Profile:** independent software engineer and defensive security researcher, Brazil  
**Institutional affiliation:** none (applicant-reported)  
**Academic publications:** none (applicant-reported)  
**Status:** preparation only — neither application below is submitted, approved, or endorsed by the provider.  
**Official requirements rechecked:** 2026-11-14.

This pack distinguishes what the public repositories demonstrate from provider-controlled eligibility, account settings, and evidence that the applicant has not supplied. It must not be treated as proof of program eligibility.

## Application paths and hard eligibility limits

| Program | Individual path | Current disposition |
| --- | --- | --- |
| Anthropic CVP — Defense Access | Individuals may apply for Defense Access on a paid Claude plan. | **Hold before submission.** The public portfolio does not document an independently accepted external vulnerability report or upstream security contribution. |
| Anthropic CVP — Red Team / Specialized | Organization applications only; not available to an individual applicant. | **Not available under the current individual profile.** No institutional or business affiliation has been reported. Do not apply as an individual for these tiers. |
| OpenAI Daybreak Blue | Individual application path exists. | **Preparation only.** Requires account security setup, eligible paid plan, physical FIDO2 key, identity verification, and separate approval. |
| OpenAI Daybreak Red | Approved business/enterprise organizations only; not available through the individual application flow. | **Not available under the current individual profile.** Blue approval does not include Red. |

## Official requirements checked on 2026-11-14

### Anthropic CVP

- The CVP Help Center says individuals (including independent researchers) may apply for Defense Access only. Red Team Access and Specialized Access are organization-only.
- The public program announcement gives individual researchers with a track record of reported vulnerabilities as an example of qualifying Defense Access applicants. This is an example of the evidence Anthropic values, not a universal checklist item stated in the Help Center. The current public portfolio does not document an accepted external report, so eligibility is not established.
- Individual Defense Access requires sign-in through Google or an equivalent identity provider and MFA. By **2026-12-15**, individual accounts must use phishing-resistant MFA (FIDO2/WebAuthn key, passkey, or smartcard/PIV); email magic-link sign-in is prohibited. SMS, voice, emailed codes, authenticator-app codes, and push approvals do not qualify.
- By **2026-12-15**, individuals must not use static or long-lived API keys to access the model. Claude Code, Claude Console, and claude.ai use OAuth; workload access, where offered, must use Workload Identity Federation. Until the cutoff, one API key is permitted only if kept in a password manager/local secrets store, never shared or committed, and rotated at least every seven days.
- Individual access is personal only: no shared sign-ins or sessions, and no browser extension/proxy that exposes the session to others. All traffic under an individual grant is retained and monitored; zero data retention is not available.
- Red Team Access is not an individual upgrade path. Organization Red Team requires phishing-resistant MFA across workspace, identity provider, cloud and credential systems; organization-domain accounts; managed devices; logged off-host network egress allowlisting for offensive/agentic work; documented incident procedure; background checks where lawful; and rapid credential revocation/offboarding.

### OpenAI Daybreak

- Individuals can request **Daybreak Blue**. The official FAQ says Daybreak Red is available only to approved business and enterprise organizations; it cannot be requested through the individual application flow. Blue approval does not include Red.
- Individual Daybreak requires an eligible paid plan, Advanced Account Security, at least two secure sign-in methods (one must work across devices), and at least one compatible **physical FIDO2 hardware key**. A software or synced passkey alone does not satisfy the hardware-key requirement.
- The individual checklist also requires saved recovery keys, identity verification, and a separate Daybreak key setup step. Completing these checks does not guarantee approval.
- Advanced Account Security disables password sign-in, email/SMS sign-in codes, and standard email recovery. Losing all enrolled sign-in methods and recovery keys may make the account unrecoverable. The applicant must store recovery keys privately; never send them to ChatGPT, GitHub, or another person.
- Check live availability in the official account flow. If Advanced Account Security does not appear in Settings > Security, it is not currently available for that account.

## Evidence reviewers can inspect

| Capability | Evidence | Scope and limitation |
| --- | --- | --- |
| Application-security research | [CSA-LAB](https://github.com/skuzu7/CSA-LAB) | Six deliberately planted findings in a local synthetic fixture; patches, regression tests, write-ups, and CI. Not third-party vulnerability discoveries. |
| Multi-step AI-agent tool-use security | [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) | 16 paired synthetic cases, 26 offline tests, and eight scripted off-scope denials. No real-model robustness result. |
| Agent action-proposal evaluation | [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) | 24 synthetic cases and 14 offline tests. No live provider evaluation has been recorded. |
| Host-side tool authorization | [Agent security benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | 19 deterministic synthetic policy decisions; no LLM is involved in this benchmark. |
| Detection engineering | [Sigma detections](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | Six rules replayed against a small labelled synthetic corpus; in-sample results are not production detection efficacy. |
| First-party secure engineering | [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) | Threat model, scoped security review, tests, first-party dependency remediation, [performance PR #23 merged](https://github.com/skuzu7/freeband-nextjs/pull/23), and [lazy PDF loading PR #24](https://github.com/skuzu7/freeband-nextjs/pull/24) pending final CI. Not a commissioned external audit. |
| Browser/MCP data-boundary hardening | [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian) | [PR #4 merged](https://github.com/skuzu7/CSA-Obsidian/pull/4): removed service-specific token capture, redacted request metadata and cookie values, origin-only URL capture, and session-path validation. [PR #5](https://github.com/skuzu7/CSA-Obsidian/pull/5) adds fail-closed host allowlisting and Windows ACL hardening; CI validation pending. |
| Scope and authorization | [CSA-LAB PR #20 merged](https://github.com/skuzu7/CSA-LAB/pull/20) | Authorization and target inventory reconciled with current offline agent research surfaces. No external target is represented as authorized. |

For claim-by-claim evidence and reproduction instructions, see [SECURITY_PORTFOLIO.md](../SECURITY_PORTFOLIO.md) and [REVIEWER_GUIDE.md](../REVIEWER_GUIDE.md).

## Applicant facts still to confirm

- [ ] Certifications: names, issuer, date, and verification URL, or explicitly state none.
- [ ] External vulnerability disclosures: program/vendor, report identifier, acceptance status, disclosure permission, and public reference where permitted; otherwise state none.
- [ ] Client or professional security engagements: scope, authorization, dates, role, and references that may legally be disclosed; otherwise state none.
- [ ] Upstream open-source security contributions: PR URL, maintainer review/acceptance status, and exact contribution.
- [ ] Complete provider account-security and identity checks only in the provider's official portal.
- [ ] Provide contact and organization/business information only if the official application asks for it and it is truthful.

## Submission rules

1. Verify current official eligibility on the day of submission.
2. Keep synthetic, first-party, independently reviewed, and externally accepted evidence clearly separated.
3. Do not claim real-model results unless a reproducible run records provider, model/version, dataset version, trial count, raw outcomes, negative controls, and limitations.
4. Do not claim a CVE, bounty, client engagement, certification, institutional affiliation, or program approval without documentary evidence.
5. Submit identity and account-security information only through the provider's official flow. Never publish recovery keys, identity documents, or hardware-key secrets.
6. Keep this public repository free of secrets, private reports, client data, and sensitive account information.

## Current disposition

- Anthropic: the only individual route is Defense Access. The evidence pack is not yet strong enough to claim the program's example track record of reported vulnerabilities; keep the draft on hold pending independently verifiable evidence and the applicant's own portal review.
- OpenAI: individual Daybreak Blue is the available path. The applicant must complete Advanced Account Security, register two secure sign-in methods including a cross-device method and a physical FIDO2 key, save recovery keys privately, finish identity verification and Daybreak key setup, then wait for approval.
- Anthropic Red Team and OpenAI Daybreak Red require an actual approved organization path. Do not fabricate an institution, company, domain, managed-device posture, or security controls.

**Last prepared:** 2026-11-14.  
**No application has been submitted.**