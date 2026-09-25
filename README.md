# OpenDriveDB

Project 1: open-source infrastructure for organizing driving video and associated telemetry, with indexing, query, and dataset access capabilities. The research proposal also calls for a streaming framework; its required behavior remains unresolved.

## Status — Week 1 foundation, September 25, 2026

This folder contains planning documentation, not a working application. No official GitHub repository exists yet; Carlos's peer is responsible for creating it. No representative ASF/GPS/OBD files have been provided. No language, database, API framework, storage backend, or authorization mechanism has been selected.

OpenDriveAnnotate is Project 2, will have a separate repository, and starts only after OpenDriveDB is completed. Annotation and Project 2 collaboration features are outside this folder's current scope.

## What is established

- Video is ASF, with variable file sizes. GPS and OBD are expected, but either or both may be missing.
- Official data will use FAU-designated storage. Originals must remain unchanged.
- Development may use clearly separated placeholders and synthetic/test data.
- Source code will be open source and distributed through GitHub. That does not make the research dataset public.
- Temporary authorization for dataset retrieval is intended. Its duration, expiry trigger, and interrupted-download behavior remain undecided.
- Carlos's high-level completion goal is a functioning system through which authorized users can download the full dataset and work with it. Detailed acceptance criteria remain pending.

The research proposal reports more than 10,000 existing clips and describes spatial telemetry, GPS, and road-environment metrics. This is a proposal-reported collection size, not a count independently measured in this task. See [requirements](Docs/requirements.md) for sources and scope.

## Documentation

| File | Purpose |
| --- | --- |
| [Requirements](Docs/requirements.md) | Evidence, confirmed requirements, decisions, assumptions, and proposed acceptance checks |
| [Data model](Docs/data-model.md) | Conceptual relationships; not a database schema |
| [Dataset inspection](Docs/dataset-inspection.md) | Read-only inspection checklist and four development cases |
| [Questions](notes/questions.md) | Unresolved decisions and W2 dependencies |
| [Work log](notes/work-log.md) | Verified work, handoff status, and unrecorded hours |
| [Milestones](ROADMAP.md) | Provisional milestones and current dependencies |
| [Contributing](CONTRIBUTING.md) | Lightweight draft contribution workflow |
| [Security](SECURITY.md) | Draft handling/reporting guidance; contact still pending |

## Connecting to the official repository later

This is a portable documentation folder; Git has not been initialized and no remote has been configured here. When the peer supplies the official URL and access:

1. Clone the official repository into a separate development location and inspect its existing files, branch, and history.
2. Merge these documents into that clone, preserving any existing work. No `.gitignore` was found in the supplied RA folder. If Carlos's previously created copy is located elsewhere, merge its useful rules with the new file rather than overwriting blindly.
3. Review the changes and staged file list before committing. Keep research data, local configuration, credentials, and this mirror's `sources/` and `AGENTS.md` out of the transfer.
4. Commit and push using the team's agreed review process. Do not force-push or replace existing remote history.
5. Clone the same official repository on the FAU computer. Pull before starting, then review, commit, and push before changing machines. Keep machine-specific paths/configuration local.

Personal-machine permission for official data remains unknown. Documentation and synthetic-data work can proceed independently of that decision.

## W2 readiness

Start with the [prioritized questions](notes/questions.md#w2-priorities) and [inspection checklist](Docs/dataset-inspection.md). Synthetic cases can support provisional design, but cannot validate real codecs, telemetry parsers, synchronization, scale, or FAU access. The repository and representative samples remain external dependencies. The original proposal has now been checked. Reconciliation with Carlos's previously mentioned `.gitignore` remains pending if that file is found elsewhere.

## Installation and license

There is no application to install yet. Setup, dependency, usage, and API instructions will be added with working software. Python is a candidate, not a selected stack.

Open-source distribution is intended; license and copyright decisions are pending. No `LICENSE` has been fabricated, and these drafts do not establish licensing terms.
