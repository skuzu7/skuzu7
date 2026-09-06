# Antonio Caetano

**Software engineer focused on application security, secure code review and testable remediation.**

I build web applications and automation tools with TypeScript, Next.js and Python. My security work focuses on authentication, session handling, server-side trust boundaries and regression tests. This portfolio links the code, threat models and validation evidence behind that work.

[LinkedIn](https://www.linkedin.com/in/antonioccjr/) · [Public repositories](https://github.com/skuzu7?tab=repositories)

## Security work with public evidence

### 1. Authentication and session security · freeband-nextjs

A Next.js and TypeScript application with a maintainer security review covering administrative authentication and session management.

- **Assessment:** [scope, controls, four findings and retest criteria](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md).
- **Threat modeling:** [STRIDE analysis and trust boundaries](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md).
- **Regression coverage:** [session tests](https://github.com/skuzu7/freeband-nextjs/blob/main/src/lib/__tests__/session.test.ts) for expiry, tampering, invalid signatures and legacy cookie rejection.
- **Recorded validation:** [CI run #19](https://github.com/skuzu7/freeband-nextjs/actions/runs/33989576172) completed successfully on **September 5, 2026**, at commit [d3160b5](https://github.com/skuzu7/freeband-nextjs/commit/d3160b541aedc80e302d0a7c61eb91c5568f3b2c). Its Vitest report records **91 passing tests across 8 files** in the project suite.

The August 29 review documents a separate baseline with 33 passing tests. It identifies limitations in per-instance rate limiting, forwarded-address trust, legacy tokens in URLs and session revocation. Use the [current source and CI history](https://github.com/skuzu7/freeband-nextjs/actions) to assess later changes; the test totals do not establish that every finding has been resolved.

### 2. Payment boundaries · Shopping-Cart-Project

A Next.js shopping cart integrating Stripe checkout. The [payment security architecture](https://github.com/skuzu7/Shopping-Cart-Project/blob/main/docs/SECURITY_ARCHITECTURE.md) documents the browser/server boundary, backend secret handling and checkout validation.

[Repository](https://github.com/skuzu7/Shopping-Cart-Project) · [Security policy](https://github.com/skuzu7/Shopping-Cart-Project/blob/main/SECURITY.md) · [CI history](https://github.com/skuzu7/Shopping-Cart-Project/actions)

### 3. Browser automation and MCP · CSA-Obsidian

A Python project combining Camoufox, persistent browser sessions, a CLI and a 17-tool Model Context Protocol server. Documented use cases include authorized QA, accessibility, browser compatibility and agent evaluation. Browser profiles, cookies and saved sessions are sensitive data and require explicit scope and careful handling.

[Project and test instructions](https://github.com/skuzu7/CSA-Obsidian#readme) · [Architecture](https://github.com/skuzu7/CSA-Obsidian/blob/main/docs/ARCHITECTURE.md) · [Security design](https://github.com/skuzu7/CSA-Obsidian/blob/main/docs/SECURITY_ARCHITECTURE.md) · [Security policy](https://github.com/skuzu7/CSA-Obsidian/blob/main/SECURITY.md) · [CI history](https://github.com/skuzu7/CSA-Obsidian/actions)

## AI-assisted defensive engineering

My focus is using AI assistance for code understanding, threat modeling, test design and remediation review, with human review of findings and changes. The intended outcome is a reproducible finding, a reviewable fix and a regression test.

1. **Define scope:** work on my own projects or systems explicitly authorized for testing, in controlled test environments.
2. **Trace the risk:** connect authentication, authorization, input validation and secret-handling concerns to specific code paths and trust boundaries.
3. **Validate the finding:** check assumptions against source and reproducible tests before treating an AI-generated finding as confirmed.
4. **Review and retest:** evaluate the proposed change, run the relevant checks and document remaining limitations.
5. **Protect sensitive data:** keep credentials, session exports and confidential information out of public issues and shared examples; follow the affected project's security reporting policy.

The linked assessments are maintainer reviews and project documentation. CI results are evidence of the configured checks at the referenced commit.

## Technical toolkit

**Development:** TypeScript, JavaScript, Python, SQL, HTML/CSS, Next.js, React, Node.js, Express.  
**Automation:** Playwright, Camoufox, FastMCP.  
**Testing and security:** Vitest, pytest, Ruff, ESLint, Gitleaks, GitHub Actions, STRIDE threat modeling.

<details>
<summary><strong>Background and credentials</strong></summary>

My background includes Civil Engineering and full-stack software development.

- **Ada Tech / Santander Coders:** Web Full Stack Certificate — reference `18d1ae9b-a52f-4d5e-b0fd-4a50784c5d76`.
- **HackerRank:** [Angular certificate](https://www.hackerrank.com/certificates/22c1c285f2bf) · [React certificate](https://www.hackerrank.com/certificates/d912cb704846).
- **Academic publication:** *O Gerenciamento de Resíduos Sólidos na Engenharia Civil: Desafios e Possibilidades* — [DOI 10.35265/2236-6717-207-9174](https://doi.org/10.35265/2236-6717-207-9174).

</details>

## Contact

For professional contact, use [LinkedIn](https://www.linkedin.com/in/antonioccjr/). For security findings, follow the affected repository's security policy.
