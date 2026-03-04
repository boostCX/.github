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
- Label definitions and sync workflows
- Generic Copilot instructions

### What does NOT belong here — ever

- **No proprietary business logic, architecture, or implementation details**
- **No client names, tenant identifiers, or customer data**
- **No internal team structures, org charts, or personnel details beyond CODEOWNERS**
- **No credentials, tokens, API keys, or connection strings**
- **No internal process documentation** (operating model, gate matrix, playbook — these live in the private `bcx-handbook` repo)

If in doubt, put it in `boostCX/bcx-handbook` (private), not here.

---

## Issue templates

| Template | Type label | Use when… |
| --- | --- | --- |
| [Epic](/.github/ISSUE_TEMPLATE/epic.yml) | `enhancement` | Defining a platform capability or large deliverable spanning multiple stories |
| [Story](/.github/ISSUE_TEMPLATE/user_story.yml) | `enhancement` | Describing a user-facing deliverable with acceptance criteria |
| [Task](/.github/ISSUE_TEMPLATE/task.yml) | `task` | Internal engineering, tech debt, or sub-task work |
| [Bug — functional](/.github/ISSUE_TEMPLATE/bug_functional.yml) | `bug` | Reporting incorrect behavior |
| [Bug — performance](/.github/ISSUE_TEMPLATE/bug_performance.yml) | `bug` | Reporting a measurable performance problem |
| [Investigation (Spike)](/.github/ISSUE_TEMPLATE/investigation_spike.yml) | `investigation` | Scoping a broad symptom into actionable child issues |

Template chooser config: [config.yml](/.github/ISSUE_TEMPLATE/config.yml)

### Capacity planning

All sprintable templates (Story, Task, Bug, Investigation) require an **Estimate (hours)** field.
Epics include an optional estimate for top-level sizing. Estimates are tracked as hours, not story points.

### Project board fields (not labels)

**Priority** (`P0`–`P3`), **Blocked**, **Iteration**, and **Status** are tracked as GitHub Projects board fields — they are not labels and do not appear in issue templates.
The `area:*` labels are the source of truth for product area. Templates include a Product area dropdown; triage applies the matching `area:*` label after submission.

## Community health files

| File | Purpose |
| --- | --- |
| [PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md) | Default PR checklist |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Contribution expectations |
| [SECURITY.md](SECURITY.md) | Vulnerability reporting process |
| [SUPPORT.md](SUPPORT.md) | Support routing |
| [CODEOWNERS](CODEOWNERS) | Default ownership |

## Label management

- **[labels.yml](labels.yml)** — canonical label definitions (type, area, severity, meta)
- **[.github/workflows/sync-labels.yml](.github/workflows/sync-labels.yml)** — auto-syncs labels to all org repos on push
- **[.github/workflows/sync-project-fields.yml](.github/workflows/sync-project-fields.yml)** — mirrors `area:*` labels to the Project board **Product Area** field

> **Note:** Priority (`P0`–`P3`), Blocked, Iteration, Status, and Estimate (hours) are tracked as **GitHub Projects board fields**, not as repo labels.

Labels are synced to all org repos automatically whenever `labels.yml` is updated on `main`. You can also trigger a sync manually from the Actions tab.

## For AI assistants

- **[.github/copilot-instructions.md](.github/copilot-instructions.md)** — org-wide Copilot instructions (inherited by all repos)
