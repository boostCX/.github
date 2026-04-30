# boostCX Organization — Copilot Instructions

These instructions apply to all repositories in the `boostCX` organization unless a repository provides its own override.

## Brand and naming

- Always use `boostCX` (lowercase `boost`, uppercase `CX`).
- Never write "BoostCX", "boostcx", "Boost CX", or other variations.

## Engineering standards

- Every code change must be linked to a GitHub Issue.
- Pull requests must include: linked issue, testing evidence, risk summary, and rollout/rollback notes.
- PRs should be small and reviewable. Prefer multiple small PRs over one large one.
- No direct commits to `main`. All changes go through pull requests with required reviews.
- Required CI checks must pass before merge.

## AI-guided development

- Copilot and AI agent workflows are encouraged to improve implementation speed, test quality, security posture, and documentation.
- AI-generated output must be reviewed, validated, and owned by the engineer.
- AI is measured by outcome quality (defect escape rate, PR cycle time, rework), not generation volume.

## Issue and work tracking

- Issues use GitHub native **issue types**: PRD, Epic, Story, Task, Bug, Investigation.
- Issue metadata is stored as **org-level issue type fields** on the issue itself: Priority, Estimate (hours), Severity, Workstream, Requires QA Task, SRED Claimable.
- The project board (Project 3) carries only **Status** and **Iteration** — all other metadata lives on the issue.
- Product area is determined by **repository**, not labels. If the owning repo is unknown, the PRD starts in `bcx-product-intake` and is transferred after triage.
- Hierarchy is expressed via GitHub native **sub-issues** (parent/child links): PRD → Epic → Story/Task/Bug, or PRD → Story/Task directly.
- Labels are supplementary only: `needs-clarification`, `release`. They do not classify issue type, area, or severity.
- The authoritative operating model, gate definitions, and workflow playbook are maintained in the private [`boostCX/bcx-handbook`](https://github.com/boostCX/bcx-handbook) repository under `governance/`.

## Code quality

- Write clear, descriptive commit messages.
- Follow the language and framework conventions established in each repository.
- Include tests for new functionality and bug fixes.
- Document public APIs and non-obvious behavior.

## Security

- Never commit secrets, credentials, API keys, or connection strings.
- Report security vulnerabilities privately per the org SECURITY.md policy.
- Use environment variables or secret management for sensitive configuration.
