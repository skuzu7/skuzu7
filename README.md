# Antonio Caetano

**Software engineering · Application security · Browser automation**

I build web applications and automation tools with TypeScript, Next.js and Python. My portfolio connects application code with security reviews, threat models and regression tests, with a focus on authentication, session handling and payment boundaries.

[LinkedIn](https://www.linkedin.com/in/antonioccjr/) · [Public repositories](https://github.com/skuzu7?tab=repositories)

## Selected engineering work

### 1. freeband-nextjs — authentication and session security

A Next.js and TypeScript web application with a documented defensive review of administrative authentication and session management.

- **Review:** [scope, controls, findings and retest criteria](https://github.com/skuzu7/freeband-nextjs/blob/main/SECURITY_REVIEW.md).
- **Threat model:** [STRIDE analysis and trust boundaries](https://github.com/skuzu7/freeband-nextjs/blob/main/docs/THREAT_MODEL.md).
- **Test evidence:** [session regression tests](https://github.com/skuzu7/freeband-nextjs/blob/main/src/lib/__tests__/session.test.ts) covering expiry, tampering, invalid signatures and legacy cookie rejection.
- **Build evidence:** [GitHub Actions](https://github.com/skuzu7/freeband-nextjs/actions), including [successful run #19](https://github.com/skuzu7/freeband-nextjs/actions/runs/33989576172) for commit `d3160b5` on September 5, 2026.

The August 29 review records 33 passing tests and explicitly discusses per-instance rate limiting, forwarded-address trust, legacy tokens in URLs and session revocation. Those results describe that review's baseline; the current source and CI history provide the context for subsequent changes.

### 2. Shopping-Cart-Project — payment integration boundaries

A Next.js shopping cart integrating Stripe checkout.

- [Payment architecture](https://github.com/skuzu7/Shopping-Cart-Project/blob/main/docs/SECURITY_ARCHITECTURE.md) documents the client/server boundary, server-side secret handling and checkout validation.
- [Security policy](https://github.com/skuzu7/Shopping-Cart-Project/blob/main/SECURITY.md) and [CI history](https://github.com/skuzu7/Shopping-Cart-Project/actions) provide review entry points.

### 3. CSA-Obsidian — browser automation and MCP

A Python project combining Camoufox browser automation, persistent sessions, a CLI and a 17-tool Model Context Protocol server. The documented use cases include authorized QA, accessibility, browser compatibility and agent evaluation.

- [Project overview and test instructions](https://github.com/skuzu7/CSA-Obsidian#readme).
- [Architecture](https://github.com/skuzu7/CSA-Obsidian/blob/main/docs/ARCHITECTURE.md) and [security design documentation](https://github.com/skuzu7/CSA-Obsidian/blob/main/docs/SECURITY_ARCHITECTURE.md).
- [Security policy](https://github.com/skuzu7/CSA-Obsidian/blob/main/SECURITY.md) and [CI history](https://github.com/skuzu7/CSA-Obsidian/actions).

Browser profiles, cookies and saved sessions require sensitive-data handling. The project's documented operating scope is limited to systems, accounts and profiles owned by the operator or explicitly authorized for testing.

## Defensive engineering focus

- Review authentication, authorization, input validation and secret handling.
- Connect threat models to code paths, regression tests and documented limitations.
- Validate proposed fixes in controlled test environments before deployment.
- Use AI assistance for code understanding, test design and remediation review, with human review of findings and changes.

The linked security artifacts are project documentation and maintainer reviews, not independent security certifications. A passing CI run establishes only that the configured checks passed.

## Technical toolkit

**Languages:** TypeScript, JavaScript, Python, HTML/CSS, SQL  
**Application development:** Next.js, React, Node.js, Express  
**Automation:** Playwright, Camoufox, FastMCP  
**Quality and security:** Vitest, pytest, Ruff, ESLint, Gitleaks, GitHub Actions, STRIDE threat modeling

## Background and credentials

My background includes Civil Engineering and full-stack software development.

- **Ada Tech / Santander Coders:** Web Full Stack Certificate — reference `18d1ae9b-a52f-4d5e-b0fd-4a50784c5d76`.
- **HackerRank:** [Angular certificate](https://www.hackerrank.com/certificates/22c1c285f2bf) · [React certificate](https://www.hackerrank.com/certificates/d912cb704846).
- **Academic publication:** *O Gerenciamento de Resíduos Sólidos na Engenharia Civil: Desafios e Possibilidades* — [DOI 10.35265/2236-6717-207-9174](https://doi.org/10.35265/2236-6717-207-9174).

## Contact and security reporting

For professional contact, use [LinkedIn](https://www.linkedin.com/in/antonioccjr/). For security findings, follow the affected repository's security policy and keep credentials, session exports and confidential data out of public issues.
