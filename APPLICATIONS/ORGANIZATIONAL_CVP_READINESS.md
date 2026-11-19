# Organizational CVP Red Team readiness register

**Reviewed:** 2026-11-19  
**Status:** Preparation only. No organizational approval, verified company, client engagement, issued offensive certification or company-attributed CVE is claimed by this document.

[Official CVP rules](https://support.claude.com/en/articles/14604842-cyber-verification-program) · [Binding security requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements) · [Detailed evidence matrix](CVP_RED_TEAM_EVIDENCE_MATRIX.md)

## First gate: organization and tier

- Individual researchers and bug bounty hunters can seek **Defense Access**, not organizational **Red Team Access**.
- Red Team is for real penetration-testing firms and authorized in-house red teams, on Team, Enterprise or API.
- For a **smaller testing firm without a qualifying organizational accreditation**, the published route requires **all**: company registration at least **one year old**, public testing services, at least **two offensive-security-certified testers**, and a recent redacted test report / statement of work / client reference.
- An established pentest firm can instead present at least one accepted issuer-side credential **in the firm's name** (CNA listing, FIRST full membership, recent CVE credit, CREST/CHECK/FedRAMP 3PAO).
- An in-house red team has a different route, including its organization's security-program evidence, advance test authorization, named team and qualifying proof of team work.
- A self-authored portfolio, a freshly registered business, a personal certification or merely participating in HackerOne/Wordfence cannot bypass the organization's route.

## Evidence inventory

| Item | Verification acceptance criterion | Status |
| --- | --- | --- |
| Registered legal entity | Official registration and age; legal name matches submitted identity | Not evidenced publicly |
| Relevant organization route | Exact chosen official CVP route and credible issuer-owned proof | Not evidenced publicly |
| Organizational testing service | Public page specifying services and authorized methodology | Only sample research services currently documented |
| Testing team and certificates | Two or more issued, verifiable offensive certifications **if the small-firm route is used** | Not evidenced publicly |
| Genuine recent engagement | Redacted client report, SOW or customer reference from the past 12 months | Not evidenced publicly |
| Independent accepted security work | Credited CVE, maintainer-accepted upstream security patch or verified bounty, without overclaiming | Not evidenced by current portfolio |
| Authorized testing | Explicit target authority, scope and rules of engagement | First-party templates only |
| Verified individual research | [CSA-LAB](https://github.com/skuzu7/CSA-LAB) and [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) | Public synthetic work documented |

## Operational control register

For Red Team, the organization must **implement**, not merely describe:

| Control | Proof to collect privately | Status |
| --- | --- | --- |
| Named security contact and incident response | Incident runbook, contact chain, exercise, 24h revocation test | Not verified |
| Phishing-resistant MFA | FIDO2/passkey/PIV enforcement and redacted test | Not verified |
| Organization-domain accounts | Identity provider and domain ownership evidence | Not verified |
| Credential management | No static/long-lived keys for model access; short-lived identities and rotation evidence | Not verified |
| Managed devices | Company-controlled endpoints, OS patching records | Not verified |
| Network egress restriction | Agent execution outbound allow-list enforced off-host and logging | Not verified |
| Personnel verification | Identity/background checks according to applicable law | Not verified |
| Account offboarding | Completion of removal within three business days | Not verified |
| Record of users/workspaces | Least-privilege access roster | Not verified |
| Incident notification | Procedure satisfying Anthropic reporting obligations | Not verified |

### Defense-to-Red-Team transition note

Anthropic's current individual Defense rules additionally require phishing-resistant MFA by **2026-12-15**, and prohibit static/long-lived credentials after that date. This is a *separate* obligation from applying for organizational Red Team Access. The current security requirements also prohibit sharing granted individual sessions with other people.

## How to build a legitimate application pack

1. Verify the organization's **legal identity and organizational tier**, then choose its actual CVP route.
2. Map each assertion to independently verifiable evidence; record issue/expiration date, issuer, holder and limitations.
3. Keep company registration, signed contracts, customer references, staff background checks and control screenshots **private**.
4. Publish only permissioned excerpts: a professional services page, authorized research notes, reproducible code and sanitized test reports.
5. Measure actual gap closure; do not label unimplemented controls "completed".
6. Recheck official documentation on submission day. The applicant must complete the Anthropic portal process themselves.

## Claim hygiene

- A lab-generated SQLi does **not** imply a third-party security vulnerability.
- A CI-green branch does **not** imply independent audit or proven real-model jailbreak prevention.
- A certificate of course completion does **not** automatically satisfy offensive-security certification criteria.
- A personal CVE does **not** automatically satisfy **company-attributed** CVE-credit requirements.
- Joining bug bounty programs does **not** count as operating a paid bug bounty program for 12 months.
- This public file never attests to privately held company controls or CVP access.

**External evidence path:** [Portfolio](../SECURITY_PORTFOLIO.md) · [Reviewer guide](../REVIEWER_GUIDE.md) · [Red Team evidence dossier](CVP_RED_TEAM_EVIDENCE_MATRIX.md).
