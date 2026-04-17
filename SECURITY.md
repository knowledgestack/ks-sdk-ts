# Security Policy

## Reporting a vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Report privately via one of:

1. **GitHub Private Vulnerability Reporting** (preferred) — [report here](https://github.com/knowledgestack/ks-sdk-ts/security/advisories/new).
2. **Email** — `security@knowledgestack.ai` (include "ks-sdk-ts" / `@knowledge-stack/ksapi` in the subject).

Include where possible:

- Affected version (`@knowledge-stack/ksapi` npm version or commit SHA)
- Reproduction steps
- Impact (credential exposure, code execution, privilege escalation, DoS)
- Proof-of-concept if you have one

## Scope

This package is **generated from the Knowledge Stack OpenAPI specification**.

In scope:
- Vulnerabilities in generated client code (auth handling, request construction, response parsing)
- Supply-chain concerns in the published npm artifact
- CI / release pipeline misconfigurations

Out of scope (report to `security@knowledgestack.ai`):
- Vulnerabilities in the hosted Knowledge Stack API — report upstream
- Issues in forks or third-party clients

## Response

- Acknowledgement within **2 business days**
- Triage within **5 business days**
- Critical fixes target **7 days**; lower severity within the next release cycle
- Default disclosure window: **90 days**, adjusted by mutual agreement

## Safe harbor

Good-faith security research welcomed under the same terms as the rest of the Knowledge Stack ecosystem.
