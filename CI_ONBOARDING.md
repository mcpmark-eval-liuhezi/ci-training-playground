# CI Onboarding Notes for Trainees

Welcome to the sandbox! Nothing here is precious — break things freely, then fix them.

## What CI is (in one paragraph)
Continuous Integration means every push and pull request is automatically built and tested.
If a test fails, you find out in minutes instead of days.

## Where CI lives in this repo
- Workflow files live in `.github/workflows/` (YAML).
- Each file defines `on:` (triggers) and `jobs:` (what runs).
- The **Actions** tab in the GitHub UI shows every run and its logs.

## Key vocabulary
| Term | Meaning |
|------|---------|
| **Workflow** | A YAML file in `.github/workflows/` describing automated work |
| **Job** | A set of steps that runs on one runner (VM) |
| **Step** | A single command or action |
| **Runner** | The VM that executes a job |
| **Artifact** | Files a job uploads for later inspection |

## Hands-on exercises for the session
1. Add a trivial workflow that runs on every push printing "hello".
2. Break it on purpose (bad YAML syntax) and read the error message.
3. Fix it, then add a failing `exit 1` step and watch the run turn red.
4. Re-run the failed job from the UI until it passes.

## Useful links
- GitHub Actions docs: https://docs.github.com/en/actions
- Workflow syntax reference: https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax
