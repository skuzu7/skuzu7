# GitHub remediation and application-readiness report

**Prepared:** 2026-11-14  
**Account/repositories reviewed:** `skuzu7` public profile and selected first-party projects  
**Disposition:** four technical PRs merged; one follow-up performance PR is under CI; the provider application pack remains draft; no provider application submitted.

## Pull requests and verification

| Repository | PR | Purpose | Current status |
|---|---:|---|---|
| [skuzu7/skuzu7](https://github.com/skuzu7/skuzu7/pull/11) | #11 | Anthropic CVP / OpenAI Daybreak evidence pack | Open, draft; applicant fact checks and account-level steps remain. |
| [CSA-LAB](https://github.com/skuzu7/CSA-LAB/pull/20) | #20 | Reconcile authorization scope with offline agent research | Merged; Local Security Evidence and CodeQL checks passed. |
| [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian/pull/4) | #4 | Remove service-specific token capture and harden browser/MCP data handling | Merged; Ruff, formatter and unit tests passed. |
| [CSA-Obsidian](https://github.com/skuzu7/CSA-Obsidian/pull/5) | #5 | Fail-closed host allowlist and Windows ACL hardening | Open; Linux and Windows CI are being completed. |
| [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs/pull/23) | #23 | Reduce shared JavaScript bundle and correct CLS measurement | Merged; full GitHub Actions workflow passed. |
| [freeband-nextjs](https://github.com/skuzu7/freeband-nextjs/pull/24) | #24 | Defer portfolio PDF engine until user click | Open; full CI/performance verification in progress. |

## Changes delivered

### CSA-LAB
- Merged authorization and target-inventory updates distinguishing local synthetic fixtures, offline agent benchmarks, optional provider API evaluations, and external targets.
- No external lab or bug-bounty target is represented as active.

### CSA-Obsidian
- Merged PR #4: removed Binance-specific token capture; redacted sensitive and unknown request-header values; reduced captured URLs to scheme and host; redacted MCP cookie values; validated session paths; protected POSIX session writes.
- Merged PR #5 adds a fail-closed context-wide HTTP(S) host allowlist with exact hosts, optional wildcard subdomains and explicit non-standard ports. Empty/unset configuration denies network requests. Firefox service workers are disabled to keep Playwright request routing effective. Linux and Windows CI passed, including actual Windows ACL integration checks.
- PR #5 also adds private POSIX 0700/0600 modes and Windows ACL handling for profile/session directories, session JSON, Chrome cache/export files and temporary Chrome cookie database copies. It uses private same-volume staging before writing sensitive JSON.
- Residual limit: this is a browser host policy, not an OS sandbox or IP-level egress firewall. It does not pin DNS answers or prevent an allowlisted hostname from resolving to a private IP. Direct Python APIs and arbitrary page JavaScript remain privileged.

### Freeband
- Merged PR #23: removed the unused `tailwind-merge` runtime dependency and corrected CLS measurement to use session windows.
- Full CI passed: 15-page visual smoke, reduced-motion smoke, and five-route performance budget. Shared JavaScript measured 622 KB on `/`, 654 KB on `/palco`, `/arquivo`, and `/historia`; CLS was 0 on those routes and 0.0007 on `/portfolio`. LCP ranged from 160–348 ms.
- Follow-up PR #24 defers the PDF renderer and seven-page portfolio document graph until the user clicks Download, aiming to remove the prior 1,901 KB initial JS and 565 ms post-load task from the initial route. Do not mark this optimization complete until PR #24's CI measurements pass.

## Program eligibility and evidence limits

- Anthropic CVP: individuals may apply for Defense Access only. Red Team Access and Specialized Access are organization-only. The program announcement lists individual researchers with a track record of reported vulnerabilities as an example of qualifying applicants; the public evidence pack currently does not document an accepted external vulnerability report. Eligibility is not established.
- Anthropic individual Defense Access has strict account requirements: Google/equivalent IdP sign-in, MFA now, phishing-resistant FIDO2/passkey/smartcard by 2026-12-15, no email magic links, no long-lived static API keys after the cutoff, personal-only access, and retained/monitored traffic with no ZDR.
- OpenAI Daybreak: the individual application path is Daybreak Blue. Daybreak Red is only for approved business/enterprise organizations and is not available through the individual application flow. Blue approval does not include Red.
- Daybreak individual requirements include eligible paid plan, Advanced Account Security, two secure sign-in methods (one cross-device), a physical FIDO2 key, private recovery keys, identity verification, separate Daybreak key setup, and approval. Account-level status cannot be verified from GitHub.
- No CVE, bounty, client engagement, certification, institutional affiliation, live Claude/GPT security benchmark, or program approval is claimed. Synthetic lab findings are not third-party disclosures.

## Official program references

- Anthropic CVP: https://support.claude.com/en/articles/14604842-cyber-verification-program
- Anthropic CVP security requirements: https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements
- Anthropic program announcement: https://www.anthropic.com/news/cyber-verification-program
- OpenAI Daybreak overview: https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview
- OpenAI Daybreak troubleshooting: https://help.openai.com/en/articles/20001259-troubleshooting-openai-daybreak
- Advanced Account Security: https://help.openai.com/en/articles/20001221-advanced-account-security

## Submission and merge policy

All technical changes described above were pushed through pull requests. PRs #20, #4, #5 and #23 are merged. PR #24 remains subject to complete CI. PR #11 remains draft pending applicant fact review. No provider application was submitted, and no organization or account-security facts were fabricated.