# .github

Organization-wide default community health files, issue templates, and label standards for the **boostCX** organization.

Repositories in the `boostCX` org inherit these defaults automatically unless they provide their own overrides.

> **Internal governance docs** (operating model, gate matrix, workflow playbook) are maintained in the private `boostCX/bcx-handbook` repository.

---

## ⚠ This repository is public

This repository **must** be public for GitHub to inherit default issue templates, PR templates, and community health files across all `boostCX` organization repositories. This is a [platform requirement documented by GitHub](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file).

### What belongs here

- Issue and PR templates
- Community health files (CONTRIBUTING, SECURITY, SUPPORT, CODEOWNERS)
- Label definitions
- Generic Copilot instructions

### What does NOT belong here — ever

- **No proprietary business logic, architecture, or implementation details**
- **No client names, tenant identifiers, or customer data**
- **No internal team structures, org charts, or personnel details beyond CODEOWNERS**
- **No credentials, tokens, API keys, or connection strings**
- **No internal process documentation** (operating model, gate matrix, playbook — these live in the private `bcx-handbook` repo)

If in doubt, put it in `boostCX/bcx-handbook` (private), not here.

---

## `.github` vs `.template`

- **`boostCX/.github` (public):** org-default issue templates, PR template, community health files, and public-safe label definitions.
- **`boostCX/.template` (private):** starter repository content for new repos created from the template.
- **Private automation repos:** org-write workflows and project automation that should not run from a public trust boundary.

## Issue templates

| Template | Use when… |
| --- | --- |
| [Epic](/.github/ISSUE_TEMPLATE/epic.yml) | Defining a platform capability or large deliverable spanning multiple stories |
| [Story](/.github/ISSUE_TEMPLATE/user_story.yml) | Describing a user-facing deliverable with acceptance criteria |
| [Task](/.github/ISSUE_TEMPLATE/task.yml) | Internal engineering, tech debt, QA/ops work, or sub-task work |
| [Bug — functional](/.github/ISSUE_TEMPLATE/bug_functional.yml) | Reporting incorrect behavior with clear repro steps |
| [Bug — performance](/.github/ISSUE_TEMPLATE/bug_performance.yml) | Reporting a measurable performance problem with evidence |
| [Investigation (Spike)](/.github/ISSUE_TEMPLATE/investigation_spike.yml) | Scoping a broad symptom into actionable child issues |

Template chooser config: [config.yml](/.github/ISSUE_TEMPLATE/config.yml)

### Capacity planning

All sprintable work (Story, Task, Bug, Investigation) requires the **Estimate (hours)** org-level issue field.
Estimates are tracked as hours, not story points.

### Project board fields

Project 3 carries only workflow state:

- `Status`
- `Iteration`

All other metadata (Priority, Blocked, Severity, Workstream, Requires QA Task, Estimate (hours), etc.)
lives on the issue as **org-level issue fields** (not as labels and not as project fields).

## Community health files

| File | Purpose |
| --- | --- |
| [PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md) | Default PR checklist |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Contribution expectations |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Community standards |
| [SECURITY.md](SECURITY.md) | Vulnerability reporting process |
| [SUPPORT.md](SUPPORT.md) | Support routing |
| [CODEOWNERS](CODEOWNERS) | Default ownership (`@boostCX/platform-code-reviewers`) |

## Labels

**[labels.yml](labels.yml)** defines a minimal label set. Labels must not duplicate org-level issue fields.

> **Note:** Priority, Blocked, Severity, Workstream, Requires QA Task, and Estimate (hours) are **org-level issue fields**. Project 3 tracks only `Status` and `Iteration`.

Label synchronization and project automation are intentionally run from a **private internal automation repository**, not from this public repo.

## For AI assistants

- **[.github/copilot-instructions.md](.github/copilot-instructions.md)** — org-wide Copilot instructions (inherited by all repos)
