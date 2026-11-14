# Anthropic Cyber Verification Program — Individual Defense Access

**Status:** researcher-authored application statement draft; **not submitted** and **not evidence of approval**.  
**Applicant:** Antonio Caetano ([@skuzu7](https://github.com/skuzu7)), independent software engineer and defensive security researcher.  
**Institutional affiliation:** none (applicant-reported).  
**Academic publications:** none (applicant-reported).

> **Eligibility boundary (official rules checked 2026-11-14).** Independent researchers may apply as individuals for **Defense Access only**. Red Team Access and Specialized Access are organization-only. The program announcement lists individual researchers with a track record of reported vulnerabilities as an example of qualifying Defense Access applicants. The public portfolio currently documents no independently accepted external vulnerability report, so eligibility is not established. Do not submit this draft as a Red Team application. Sources: [CVP Help Center](https://support.claude.com/en/articles/14604842-cyber-verification-program) · [program announcement](https://www.anthropic.com/news/cyber-verification-program).

## Concise research statement

I conduct security research on software I own or have explicit permission to test, prioritizing reviewable root-cause analysis and verifiable fixes. My public [CSA-LAB](https://github.com/skuzu7/CSA-LAB) contains six intentionally planted application vulnerabilities, written scope, controlled reproduction, corresponding patches and regression checks run under GitHub Actions. My [19-case offline agent policy benchmark](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) exercises host-side constraints on AI-agent tool permissions. My [Scoped Agent Evals](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) adds 24 synthetic, matched benign/attack scenarios, a documented methodology, optional model adapters, offline unit tests, and reproducible CI reporting.

My primary next-step research project is [TRACEGUARD — Agent Replay Lab](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab), a bounded multi-step AI-agent tool security experiment. It provides 16 matched synthetic benign/attack cases, 26 offline tests, a separate host-side authorization layer, tamper-evident (non-authenticated) hash-linked traces, and a CI-verifiable positive control that denies eight deliberately proposed out-of-scope actions. This demonstrates a reproducible **research harness**, not real Claude model robustness.

I am requesting individual **Defense Access** to support authorized defensive review, vulnerability triage, verification of remediation, and AI-assisted evaluation of agent trust boundaries. I intend to produce public, reproducible defensive artifacts: minimal root-cause demonstrations, unit/regression tests, scoped threat models, reviews of generated patches, and redacted research notes. I will not use access as a substitute for authorization.

## Exact planned workflow

1. Define the target and authorization, record relevant assets and threat boundaries.
2. Analyze only first-party or permitted source code and approved sanitized logs, with an explicit list of allowed files/tools.
3. Ask the model for hypotheses, risk explanations, safe reproductions and patches **for researcher review**.
4. Reproduce findings on a localhost fixture or explicitly permitted test environment, record negative controls, and compare vulnerable and patched behavior.
5. Independently validate results with local and CI tests. Use a host-side allowlist and human approval for write operations.
6. Publish sanitized, reproducible lessons; disclose any real third-party issue privately to its maintainer under the program's rules.

## Inspectable evidence

| Claim | Evidence | Important limitation |
| --- | --- | --- |
| Application vulnerability research | [Six documented findings](https://github.com/skuzu7/CSA-LAB/tree/main/writeups) and [test suites](https://github.com/skuzu7/CSA-LAB/tree/main/tests) | Deliberately planted first-party issues |
| Reproducibility | [CSA-LAB CI](https://github.com/skuzu7/CSA-LAB/actions) and [scope PR #20 merged](https://github.com/skuzu7/CSA-LAB/pull/20) | CI is not independent external review |
| Severity and detection discipline | [Computed CVSS v3.1 and ATT&CK mapping](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md), [six Sigma rules with a replay scorer](https://github.com/skuzu7/CSA-LAB/tree/main/detections) | In-sample check on a 35-request synthetic corpus |
| Agent authorization | [19-case policy checks](https://github.com/skuzu7/CSA-LAB/tree/main/agent_security) | No actual LLM in those checks |
| Prompt-injection research protocol | [24-case matched eval](https://github.com/skuzu7/CSA-LAB/tree/main/agent_evals) | No live-model benchmark results yet |
| Real first-party engineering | [Threat model](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md), [security review](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md), [performance PR #23 merged](https://github.com/skuzu7/freeband-nextjs/pull/23) | Not a commissioned audit |
| Browser/MCP boundary hardening | [CSA-Obsidian PR #4 merged](https://github.com/skuzu7/CSA-Obsidian/pull/4) | [host allowlist/Windows ACL PR #5 is merged with Linux and Windows CI passing](https://github.com/skuzu7/CSA-Obsidian/pull/5); neither PR is an independent audit |

## Individual Defense Access security requirements

Before applying, and throughout any approved grant, the applicant must follow Anthropic's [CVP security requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements):

- Sign in to the grant-holding Anthropic account only through Google or an equivalent identity provider and enable MFA.
- By **2026-12-15**, use phishing-resistant MFA: a FIDO2/WebAuthn security key, a passkey, or smartcard/PIV. Email magic-link sign-in must be disabled. SMS, voice, emailed codes, authenticator-app codes, and push approvals do not qualify.
- By **2026-12-15**, do not use static or long-lived API keys to access the model. Claude Code, Claude Console, and claude.ai use OAuth; workloads, where offered, must use Workload Identity Federation. Until the cutoff, one API key is permitted only if stored in a password manager/local secrets store, never shared or committed, and rotated at least every seven days.
- The grant is personal: no shared sign-ins/sessions and no browser extension or proxy that exposes the session to others.
- All individual grant traffic is retained and monitored; zero data retention is not available.
- Individual grants are subject to incident reporting, cooperation, and ongoing review requirements.

## Why Red Team Access is not the current application path

Anthropic's current CVP rules list Red Team Access as organization-only. The organization track has substantially stronger controls, including phishing-resistant MFA for workspace/identity/cloud/admin systems, organization-domain accounts, short-lived credentials, managed devices, logged off-host network egress allowlisting for offensive/agentic work, documented incident procedures, background checks where lawful, and 24-hour credential revocation. The current applicant has reported no institutional or business affiliation. Do not represent an individual account as an organization or claim these controls without evidence.

## Responsible use and transparency

I will not scan third-party production systems, access real credentials, automate unauthorized exploitation, or repurpose restricted research access for third-party customers. I will keep model-generated proposals separate from the host's authorization decision and require human review before sensitive actions. I do **not** claim accepted external bounties, CVEs, professional penetration-testing credentials, institutional affiliation, special-program membership, or independent validation that is not documented.

## Remaining applicant-controlled steps

Confirm the current [CVP tiers and individual eligibility](https://support.claude.com/en/articles/14604842-cyber-verification-program), [CVP security requirements](https://support.claude.com/en/articles/17202708-cyber-verification-program-security-requirements), and the [program announcement](https://www.anthropic.com/news/cyber-verification-program). Verify any independently accepted disclosure evidence from personal records. Complete identity/security steps only through the official Verification Portal. This public text is an evidence-backed statement draft, **not** a completed application.

**Current maturity:** authentic synthetic proof-of-work with strong reproducibility; independently accepted external defensive report or upstream-reviewed contribution remains an evidence gap.