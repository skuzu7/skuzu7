# Anthropic CVP Red Team — evidence-first application dossier

**Reviewed:** 2026-11-19  
**Owner:** Antonio Caetano (GitHub: [skuzu7](https://github.com/skuzu7))  
**Status:** Public preparation artifact; **NOT** an Anthropic approval, a submitted organization application, or proof of Red Team eligibility.

## Decision in one minute

The individual-researcher route is **Defense Access only**. Red Team Access is available only to **organizations**, through Team, Enterprise or API. A LinkedIn headline, personal GitHub, synthetic bug lab or newly created CNPJ does **not** override these requirements.

**Current independently inspectable evidence:** first-party secure engineering and synthetic research.  
**Organization eligibility:** unverified.  
**Red Team approval status:** not evidenced by this dossier.  
**External third-party recognition:** no accepted bounty, attributed CVE, awarded client penetration test or offensive certification is claimed in this dossier.

**Authoritative requirements:**
- [Anthropic CVP (tiers, organizations and acceptable proofs)](https://support.claude.com/en/articles/14604842-cyber-verification-program)
- [Anthropic CVP Security Requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements)
- [Verification Portal](https://portal.anthropic.com/programs/cvp)

## Evidence with independent reproduction paths

| Capability | Evidence | What it proves | Explicit limitation |
| --- | --- | --- | --- |
| AppSec root-cause review | [CSA-LAB](https://github.com/skuzu7/CSA-LAB), [six writeups](https://github.com/skuzu7/CSA-LAB/tree/main/writeups) | Reproducible examples, patches and regression coverage for six planted weaknesses | Intentional local fixtures; not third-party bugs or CVEs |
| Agent tool-boundary engineering | [TRACEGUARD methods](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/METHODS.md), [results](https://github.com/skuzu7/CSA-LAB/blob/main/agent_replay_lab/RESULTS.md) | 16 synthetic paired cases, 26 offline tests, scripted host decisions | No live-model security score, external audit or production isolation claim |
| Agent evaluation methodology | [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) | 24 synthetic scenarios and 14 offline tests, with model adapters available for separately authorized runs | No real provider run is claimed |
| Remediation engineering | [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs), [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md) | Threat modeling, application hardening, CI-verifiable patches | First-party application, not a paid engagement |
| Detection and severity reporting | [Detection rules](https://github.com/skuzu7/CSA-LAB/tree/main/detections), [classification](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md) | Rules/replay and transparent CVSS/CWE mapping | In-sample synthetic measurements |
| Independent review navigation | [Reviewer guide](../REVIEWER_GUIDE.md), [portfolio index](../SECURITY_PORTFOLIO.md) | Paths for an outside reviewer to inspect claims | A guide is not independent certification |

## Red Team eligibility routes (choose exactly the actual organization type)

| Route | Anthropic requirement | Evidence status here |
| --- | --- | --- |
| **Qualified cybersecurity/pentest firm** | In the **firm's name**, at least one of: CVE Numbering Authority listing; FIRST full membership; recent CVE credit; CREST, CHECK or FedRAMP 3PAO accreditation | **NOT VERIFIED** |
| **Smaller testing firm without the above** | All: company registered for **at least 1 year**, public testing-services description, **two** offensive-security-certified testers, and redacted statement of work, test report or customer reference from the last **12 months** | **NOT VERIFIED** |
| **In-house red team** | Organization security-program proof (annual cybersecurity report, current ISO 27001, SOC 2 Type II, or paid bug bounty running for 12+ months), team lead and size, authorization authority, and at least one accepted team-evidence option | **NOT VERIFIED** |
| **Individual researcher** | Not a Red Team route; individuals can apply to Defense Access | **NOT ELIGIBLE AS INDIVIDUAL** |

Do not count a personal CVE as a CVE **in the firm's name** without official attribution. Do not confuse **participating in** bug bounty programs with **operating a paid bounty program** for at least 12 months.

## Operational safeguards: verify *implementation*, not a document

These are requirements, not controls already deployed:

| Control | Required verification artifact | Status |
| --- | --- | --- |
| Phishing-resistant MFA (FIDO2/passkey/PIV) | Enterprise IdP policy and a redacted successful sign-in test | NOT VERIFIED |
| Company-domain accounts for approved users | Domain ownership, identity assignments, user listing | NOT VERIFIED |
| Short-lived workload identities; no static long-lived model keys | Credential policy and configuration evidence | NOT VERIFIED |
| Org-controlled and updated endpoints | MDM/patch compliance or equivalent controlled-device inventory | NOT VERIFIED |
| Enforced outbound allow-list **off the agent host**, with logging | Network policy, deny/allow test and anonymized logs | NOT VERIFIED |
| Personnel identity/background verification | HR/legal confirmation respecting local law | NOT VERIFIED |
| Credential revocation within 24 hours | Procedure and exercise record | NOT VERIFIED |
| Offboarding within 3 business days | Workflow and test record | NOT VERIFIED |
| Incident reporting and response procedure | Named security contact; protocol and incident exercise | NOT VERIFIED |
| Approved-user and workspace separation | Workspace roster and least-privilege access review | NOT VERIFIED |

See [the exact security requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements). Do not publish screenshots with IDs, account numbers, secrets, customer data, device identifiers or personnel background records.

## Highest-leverage gaps and acceptance criteria

1. **Choose a legitimate organization path.** Evidence: signed role or company registration, official issuer page and authorized signer. A personal account alone is insufficient.
2. **Secure independent validation.** Evidence: upstream maintainer-accepted security patch, program-accepted report or verifiable CVE credit; distinguish personal credits from company credits. Public disclosure only with permission.
3. **Prove genuinely authorized offensive practice.** Evidence: actual signed rules of engagement and a redacted report or customer reference, where permitted. Synthetic sample reports do not count.
4. **Show staff credentials relevant to the chosen route.** Evidence: certificates with verifiable issuers and named professionals; course completions are not automatically offensive certifications.
5. **Deploy organizational controls and test them.** Evidence: reviewer-accessible, redacted configuration and logs. A checklist alone does not meet the requirement.
6. **Build a private submission pack.** Evidence: legal identity, company registration, signatory, team, scope, business domain, customer reference, required controls, current CVP application status.
7. **Request Red Team only when a real route is satisfied.** Submission is a separate action in the Anthropic portal. Eligibility is not a promise of approval.

## Reusable application claim format

For every claim, keep five fields:

- **Claim:** a narrowly worded verifiable statement.
- **Issuer/source:** official registry, certification issuer, CVE record, program receipt, maintainer PR, or observed test log.
- **Who it covers:** individual researcher, named team, or registered legal entity.
- **Date and validity:** issue/expiry window and program's requested period.
- **Limitations:** what this evidence does *not* establish.

**Example of a supportable technical claim:** "I maintain a public, locally reproducible AppSec lab with six deliberately vulnerable scenarios and regression-tested fixes." [Evidence](https://github.com/skuzu7/CSA-LAB).

**Unsupported claim to avoid:** "I discovered six production CVEs" or "our firm is an approved red team" based on the lab alone.

## Research and external proof workflow

Record each external opportunity in a private ledger with program name, written rules, in-scope asset, tests allowed, disclosure timeline, validity/duplicate status, submitted/acknowledged dates and permitted public citation. Do not test third-party production without valid scope. A useful measure is **independently accepted findings**, not volume of scanner output or AI-written reports.

## Privacy and review

Keep sensitive legal documents, background checks, signed customer contracts, invoices, security configs and CVP portal screenshots in a private controlled folder. Put only redacted, permissioned public evidence on GitHub. Never display an organization's private client results to make a profile look stronger.

**Reviewer next steps:** [Technical evidence index](../SECURITY_PORTFOLIO.md) → [Independent reviewer guide](../REVIEWER_GUIDE.md) → [Organizational readiness register](ORGANIZATIONAL_CVP_READINESS.md).
