# Security Research Milestones and Evidence Requirements

This is an evidence ledger / forward plan, not a claim of professional credentials or eligibility. **Priority: quality and external review rather than quantity of repositories.**

| Priority | Milestone | Verification standard | State |
| --- | --- | --- | --- |
| 1 | Reproducible first-party vulnerability demonstrations and patch regressions | Six planted write-ups, tests, and passing GitHub Actions | **Done — synthetic** |
| 2 | Reviewable host-policy security evaluation | 19 offline scenarios with documented limits | **Done — synthetic** |
| 3 | Versioned matched AI-agent action proposal dataset | 24 cases; 14 unit tests; two opposing scripted controls with CI reports; optional explicit provider adapters | **Done — synthetic; no live model run** |
| 3a | Bounded multi-step agent-security research project | [TRACEGUARD](https://github.com/skuzu7/CSA-LAB/tree/main/agent_replay_lab): 16 paired synthetic cases; 26 tests; 8/8 scripted off-scope actions blocked; passing [CI PR #14](https://github.com/skuzu7/CSA-LAB/pull/14) | **Done — synthetic only; no real-model data** |
| 3b | Classification, detection and reporting for the lab findings | [Computed CVSS v3.1 and ATT&CK mapping](https://github.com/skuzu7/CSA-LAB/blob/main/docs/classification.md); [six Sigma rules](https://github.com/skuzu7/CSA-LAB/tree/main/detections) with 13/13 attack and 0/22 benign requests alerted on both builds; [sample report](https://github.com/skuzu7/CSA-LAB/blob/main/reports/sample-assessment-report.md); passing [CI PR #18](https://github.com/skuzu7/CSA-LAB/pull/18) | **Done — synthetic, in-sample** |
| 4 | External open-source defensive contribution | Upstream maintainer reviews and accepts a security-hardening/test PR | **Not yet demonstrated** |
| 5 | Authorized independently accepted security report | Program acknowledgement and permission to publish a redacted finding | **Not yet demonstrated** |
| 6 | Live model security evaluation with complete provenance | Verified provider run; model/version; repeated trials; raw classifications; negative controls; honest limits | **Not yet run** |
| 7 | Anthropic CVP Defense (individual) | The official portal, not public GitHub, determines account-level status. Individual applicants can obtain Defense Access; independent reports help credibility but a LinkedIn/GitHub portfolio alone cannot verify grants. | **Access status not publicly evidenced here; check portal** |
| 8 | Anthropic CVP Red Team (organization) | Actual eligible organization on Team/Enterprise/API, correct route-specific proof and implemented security controls. [Evidence matrix](APPLICATIONS/CVP_RED_TEAM_EVIDENCE_MATRIX.md). | **Organization eligibility and controls not yet evidenced** |
| 8a | Anthropic CVP Specialized (organization) | Authorized high-risk testing on systemically important infrastructure, need beyond Red Team, and operational controls. [Evidence gate](APPLICATIONS/CVP_SPECIALIZED_EVIDENCE_MATRIX.md). | **Critical-infrastructure authority, organization and approval not evidenced by this portfolio** |
| 8b | OpenAI Daybreak Red (organization) | Approved business/enterprise organization, permitted advanced cyber work, separate provider verification; GPT-6 Cyber requires additional approval. [Readiness matrix](APPLICATIONS/DAYBREAK_RED_ORGANIZATIONAL_READINESS.md). | **Organizational approval and onboarding not evidenced by this portfolio** |
| 9 | Other restricted vendor programs | Treat each vendor's current official requirements and portal status separately; never infer eligibility from another provider's access. | **Not independently verified here** |

## Next technical experiments

1. Pre-register a multi-run comparison with baseline utility, attacker-goal proposal, invalid JSON and host-denial counts.
2. Add independent review of synthetic scenarios and classification labels before making model claims.
3. Build a true sandboxed agent tool integration **only with local dummy assets**, not live external systems.
4. Review a small, owner-authorized open-source dependency or authentication bug; submit a narrowly scoped, test-backed patch; wait for maintainer review.
5. Document negative results and false positives, not just apparent wins.

## Evidence acceptance policy

Do not count GitHub commits, number of repositories or fabricated CVEs as accepted vulnerabilities. A public PR is **submitted work**, not an accepted external review until the independent maintainer merges or acknowledges it. A self-authored benchmark is **synthetic research**; CI validates its execution but does not prove state-of-the-art AI safety. Program status cannot be inferred from a GitHub README.

**Reference drafts (not portal-status records):** [historical CVP Defense statement](APPLICATIONS/ANTHROPIC_CVP_DEFENSE_ACCESS.md), [CVP Red Team evidence matrix](APPLICATIONS/CVP_RED_TEAM_EVIDENCE_MATRIX.md), [organizational readiness](APPLICATIONS/ORGANIZATIONAL_CVP_READINESS.md), and [Daybreak Blue notes](APPLICATIONS/OPENAI_DAYBREAK_BLUE.md).
