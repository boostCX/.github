---
applyTo: "**/*"
---

# .github Repository — Architecture

This repository is the **boostCX public organization profile and shared GitHub configuration**. It is a public repository.

## What This Repo Contains

- **Organization profile** (`profile/README.md`) — Public-facing org description on GitHub
- **Community health files** — CODE_OF_CONDUCT.md, CONTRIBUTING.md, SECURITY.md, SUPPORT.md
- **Shared templates** — Issue templates, PR templates used as org-wide defaults
- **Org-wide workflows** — GitHub Actions that run across the organization
- **Copilot instructions** (`copilot-instructions.md`) — Public-safe org-wide AI guidance

## What Does NOT Belong Here

- Company-specific coding standards, testing standards, or architectural patterns (these live in the private `.template` repo)
- Repository-specific instructions or architecture docs (these live in individual repos)
- Secrets, internal URLs, proprietary business logic, or anything not suitable for a public repo

## When Updating This Repo

**Before making changes, ask:**

1. **Is this public-safe?** This repo is visible to anyone on GitHub. Never add internal details.
2. **Is this org-wide?** Changes here affect all boostCX repos that don't override them.
3. **Does the handbook need updating too?** If changing process or governance, coordinate with `bcx-handbook`.

## File Conventions

- Community health files follow [GitHub's community health file spec](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions)
- Markdown must pass the org-wide markdownlint configuration
- Workflow files go in `.github/workflows/`
- Issue and PR templates go in `.github/ISSUE_TEMPLATE/` and `.github/`

## Relationship to Other Repos

| Repo | Role | Visibility |
| --- | --- | --- |
| **`.github`** (this repo) | Public org profile, community health files, shared templates | Public |
| **`.template`** | Authoritative source for org-wide standards (coding, testing, markdown) and new-repo scaffolding | Private |
| **`bcx-handbook`** | Operating model, decision log, governance playbooks | Private |
| **Individual repos** | Inherit standards from `.template`, extend with repo-specific architecture | Private |
