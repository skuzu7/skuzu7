# Anthropic CVP Specialized Access — critical-infrastructure evidence gate

**Reviewed:** 2026-11-23  
**Status:** organizational future-readiness documentation only. **No claim of critical-infrastructure authorization, organizational approval or Specialized Access.**

## Hard eligibility boundary

[Anthropic's CVP guidance](https://support.claude.com/en/articles/14604842-cyber-verification-program) identifies Specialized Access as an **organization-only** tier for teams that require high-risk, authorized offensive assessment of **systemically important** infrastructure. Examples include flight operating systems, power grids and interbank transfer infrastructure. Most critical-infrastructure operators conducting defensive work do **not** need Specialized.

The applicant must establish **both**:
1. Genuine authority to test relevant critical systems with high-risk activities, and
2. A technically specific explanation of the activities that cannot be performed with the **Red Team Access** tier.

Anthropic says every Specialized application undergoes an in-depth review in collaboration with the US government. The provider decides eligibility. A GitHub portfolio, business registration or ordinary pentesting qualification cannot substitute for that determination.

## Evidence matrix

| Requirement | What acceptable evidence could look like | Public portfolio status |
| --- | --- | --- |
| Qualifying legal organization | Business, public-sector, or other organization registered and verifiable in official issuer records | **Not publicly verified** |
| Critical-system mandate | Operator authorization, scope owner, system category, and contractual or statutory testing mandate | **Not evidenced** |
| Why Red Team cannot suffice | Specific blocked, lawful testing methodology, systems risk, necessary guardrails and justification | **Not evidenced** |
| Human authorization and Rules of Engagement | Signed scope, accountable approver, exclusions, stop conditions and incident contact; **private** if sensitive | **Only sample lab templates exist** |
| Phishing-resistant MFA | Enforced FIDO2/WebAuthn, passkey or PIV on applicable identities; redacted control tests | **Not verified** |
| Company-domain SSO | Organization-domain federated identities; no personal/webmail accounts for approved users | **Not verified** |
| Short-lived credentials | Platform-native short-lived access and documented revocation/offboarding controls | **Not verified** |
| Managed and malware-protected devices | Organization-owned/managed endpoints with updates and enforce-mode application controls or protective EDR | **Not verified** |
| Network egress | Off-host enforced allowlisting and logs wherever offensive or agentic work runs | **Not verified** |
| Personnel verification and response | Lawful background/identity checks, incident procedure, appointed security contact | **Not verified** |
| Provider-granted tier | Verified Specialized decision in the official Verification Portal | **Not publicly established** |

**Security standards:** the [binding CVP Security Requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements) govern the actual requirements, including named security contacts and incident duties. Every required control must be *implemented* and independently attestable; a markdown checklist never proves compliance.

## What the current projects genuinely demonstrate

- [CSA-LAB](https://github.com/skuzu7/CSA-LAB) — six planted local application weaknesses, reproducible fixes, classification, detection and regressions.
- [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab) — synthetic multi-step agent authorization controls, not testing of an actual critical system.
- [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs) — secure engineering on a first-party web app, not an air-traffic, utility-grid or interbank assessment.
- [Independent reviewer guide](../REVIEWER_GUIDE.md) — verification of research artifacts, not accreditation.

These technical artifacts are useful background, but do not close any **critical infrastructure authority** gate.

## Practical progression without misrepresentation

1. Strengthen the **individual Defense** evidence with authentic, externally reviewed defensive contributions.
2. If there is a real organization and genuine authorized offensive work, assess **Red Team** eligibility under the [organization evidence matrix](CVP_RED_TEAM_EVIDENCE_MATRIX.md).
3. Pursue **Specialized** only if the organization legitimately tests systemically important infrastructure and can document why Red Team is insufficient.
4. Have legal, operational and security stakeholders review the exact authorization scope and controls before an application.
5. Submit sensitive evidence only to the authorized [Anthropic Verification Portal](https://portal.anthropic.com/); never publish contracts, infrastructure topology, identities or secrets in the repository.

**Official sources:** [CVP tiers and application criteria](https://support.claude.com/en/articles/14604842-cyber-verification-program) · [security requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements).

**Index:** [Program readiness](README.md) · [Public evidence](../SECURITY_PORTFOLIO.md).
