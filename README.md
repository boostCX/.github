# .github

Organization-wide default community health files, issue templates, and label standards for the **boostCX** organization.

Repositories in the `boostCX` org inherit these defaults automatically unless they provide their own overrides.

> **Internal governance docs** (operating model, gate matrix, workflow playbook) are maintained in the private `boostCX/bcx-handbook` repository.

## Issue templates

| Template | Type label | Use when… |
| --- | --- | --- |
| [User story](/.github/ISSUE_TEMPLATE/user_story.yml) | `enhancement` | Describing a user-facing deliverable with acceptance criteria |
| [Feature request](/.github/ISSUE_TEMPLATE/feature_request.yml) | `enhancement` | Proposing a new capability or improvement |
| [Bug — functional](/.github/ISSUE_TEMPLATE/bug_functional.yml) | `bug` | Reporting incorrect behavior |
| [Bug — performance](/.github/ISSUE_TEMPLATE/bug_performance.yml) | `bug` | Reporting a measurable performance problem |
| [Investigation](/.github/ISSUE_TEMPLATE/investigation_broad_symptom.yml) | `investigation` | Scoping a broad symptom into actionable child issues |
| [Task](/.github/ISSUE_TEMPLATE/task.yml) | `task` | Internal engineering, test, or sub-task work |

Template chooser config: [config.yml](/.github/ISSUE_TEMPLATE/config.yml)

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

> **Note:** Priority (`P0`–`P3`), Blocked, Iteration, and Status are tracked as **GitHub Projects board fields**, not as repo labels.

Labels are synced to all org repos automatically whenever `labels.yml` is updated on `main`. You can also trigger a sync manually from the Actions tab.

## For AI assistants

- **[.github/copilot-instructions.md](.github/copilot-instructions.md)** — org-wide Copilot instructions (inherited by all repos)
