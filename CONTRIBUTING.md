# Contributing — W1 draft

OpenDriveDB is in the documentation/foundation stage. The official repository, maintainer roles, license, development stack, and public contribution process are pending. This draft does not announce that external submissions are currently accepted.

## Preparing changes

1. Read the [requirements](Docs/requirements.md) and [open questions](notes/questions.md). Keep Project 2 work in its future separate repository.
2. Keep each change focused. Distinguish confirmed facts from proposals, and record the evidence for new decisions.
3. Never include credentials, private paths, real research data, or sensitive inspection outputs. Small synthetic examples must be clearly labeled and reviewed.
4. Review the diff and files selected for commit. `.gitignore` is a convenience, not proof that a change is safe to publish; it does not untrack previously committed content.
5. Describe what changed, why, and what was actually checked. Do not claim that proposed tests have passed.

When the official repository exists, follow its agreed branch/review process and reconcile these drafts with existing files. The [README](README.md) describes the safe initial transfer and two-computer workflow.

## Development and validation

There are no install, build, or automated-test commands yet. For documentation changes, check local links, consistent status labels, and the absence of invented decisions. Future code changes should include appropriate verification of behavior, including cases A–D where relevant. Select tools and dependencies after inspecting the data and documenting the decision.

Carlos should be able to explain and review AI-assisted changes; generated claims require the same evidence as other changes.

## Before opening public contributions

Confirm license/copyright terms, maintainers and review responsibilities, contribution terms, a community code of conduct, setup/test instructions, and a private security reporting channel. See [SECURITY.md](SECURITY.md) for the current draft reporting guidance.
