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
| 7 | Vendor trusted-access programmes (Anthropic CVP, OpenAI Daybreak) | Official-portal status only. Per Anthropic's published tiers, an individual researcher qualifies for CVP Defense Access with a track record of reported vulnerabilities, and Red Team Access is for organizations; so milestones 4 and 5 come first. Daybreak's individual flow has account-level requirements (paid plan, Advanced Account Security, a FIDO2 hardware key, identity verification) that no repository can satisfy | **Not submitted; blocked on milestones 4–5** |

## Next technical experiments

1. Pre-register a multi-run comparison with baseline utility, attacker-goal proposal, invalid JSON and host-denial counts.
2. Add independent review of synthetic scenarios and classification labels before making model claims.
3. Build a true sandboxed agent tool integration **only with local dummy assets**, not live external systems.
4. Review a small, owner-authorized open-source dependency or authentication bug; submit a narrowly scoped, test-backed patch; wait for maintainer review.
5. Document negative results and false positives, not just apparent wins.

## Evidence acceptance policy

Do not count GitHub commits, number of repositories or fabricated CVEs as accepted vulnerabilities. A public PR is **submitted work**, not an accepted external review until the independent maintainer merges or acknowledges it. A self-authored benchmark is **synthetic research**; CI validates its execution but does not prove state-of-the-art AI safety. Program status cannot be inferred from a GitHub README.

**Working drafts (not client-facing, not submitted):** [CVP Defense Access](APPLICATIONS/ANTHROPIC_CVP_DEFENSE_ACCESS.md) and [Daybreak Blue](APPLICATIONS/OPENAI_DAYBREAK_BLUE.md).
