# Security Research Milestones and Evidence Requirements

This is an evidence ledger / forward plan, not a claim of professional credentials or eligibility. **Priority: quality and external review rather than quantity of repositories.**

| Priority | Milestone | Verification standard | State |
| --- | --- | --- | --- |
| 1 | Reproducible first-party vulnerability demonstrations and patch regressions | Six planted write-ups, tests, and passing GitHub Actions | **Done — synthetic** |
| 2 | Reviewable host-policy security evaluation | 19 offline scenarios with documented limits | **Done — synthetic** |
| 3 | Versioned matched AI-agent action proposal dataset | 24 cases; 14 unit tests; two opposing scripted controls with CI reports; optional explicit provider adapters | **Done — synthetic; no live model run** |
| 4 | External open-source defensive contribution | Upstream maintainer reviews and accepts a security-hardening/test PR | **Not yet demonstrated** |
| 5 | Authorized independently accepted security report | Program acknowledgement and permission to publish a redacted finding | **Not yet demonstrated** |
| 6 | Live model security evaluation with complete provenance | Verified provider run; model/version; repeated trials; raw classifications; negative controls; honest limits | **Not yet run** |
| 7 | Anthropic CVP Defense Access / OpenAI Daybreak Blue submission | Actual official-portal status and applicant-controlled trust verification | **Not submitted through this repository** |

## Next technical experiments

1. Pre-register a multi-run comparison with baseline utility, attacker-goal proposal, invalid JSON and host-denial counts.
2. Add independent review of synthetic scenarios and classification labels before making model claims.
3. Build a true sandboxed agent tool integration **only with local dummy assets**, not live external systems.
4. Review a small, owner-authorized open-source dependency or authentication bug; submit a narrowly scoped, test-backed patch; wait for maintainer review.
5. Document negative results and false positives, not just apparent wins.

## Evidence acceptance policy

Do not count GitHub commits, number of repositories or fabricated CVEs as accepted vulnerabilities. A public PR is **submitted work**, not an accepted external review until the independent maintainer merges or acknowledges it. A self-authored benchmark is **synthetic research**; CI validates its execution but does not prove state-of-the-art AI safety. Program status cannot be inferred from a GitHub README.

**Program-specific drafts:** [CVP Defense Access](APPLICATIONS/ANTHROPIC_CVP_DEFENSE_ACCESS.md) and [Daybreak Blue](APPLICATIONS/OPENAI_DAYBREAK_BLUE.md).
