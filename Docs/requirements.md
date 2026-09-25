# OpenDriveDB requirements — W1

Updated: 2026-09-25. This is lightweight requirements documentation, not a finalized architecture or formal SRS.

## Evidence and status labels

- **U — Confirmed by Carlos:** the current task and Carlos's explicit answers in [New Research Project Update](chatgpt-conversation://6a9f6894-213c-83e9-9cca-2eaff5ca3ea2).
- **P — Confirmed in the proposal:** `EPS, Open Soorce SW.doc`, IUCRC Executive Project Summary, project title "Developing Open-Source Driving Video Datasets", Center/Site Director Borko Furht. Read from the supplied RA folder on 2026-09-25; reference file left unchanged.
- **F — Existing project file:** Carlos's supplied documentation. Its note "Autentication Layer determined by FAU" is retained as an institutional decision responsibility, not as a selected mechanism.
- **G — General guidance:** `Building Open Source SW.docx` supports staged planning/coding, license selection, contribution rules, and publishing. It does not choose the project stack or license.
- **D — Current project decision:** an agreed scope/workflow choice, distinct from a proposal requirement.
- **A — Working assumption/proposal:** useful for planning, not approved technical scope.
- **Q — Open:** unresolved; tracked in [questions](../notes/questions.md).

Previous assistant examples of APIs, libraries, schemas, test tools, or schedules are not evidence of an adopted technical decision. The original proposal was checked directly; its broad streaming and real-time wording still needs operational acceptance criteria.

## Confirmed requirements

| ID | Requirement | Evidence |
| --- | --- | --- |
| R01 | Support the existing ASF video dataset; file sizes vary. | U |
| R02 | Associate video with available GPS and OBD; handle records missing either or both without treating all such records as invalid. Exact representation remains open. | U |
| R03 | Preserve the original dataset. Inspection and implementation must not require overwriting, renaming, converting in place, or adding test records to the official collection. | U |
| R04 | Use FAU-designated storage for official data; the actual storage service and access interface are unresolved. | U |
| R05 | Permit separate placeholders/test data during development. They must not be represented as official research records. | U |
| R06 | Distribute source code as open-source software through GitHub. License selection remains pending. | U |
| R07 | Provide temporary authorization for dataset retrieval. Expiry, identity, granting authority, retry, and resume behavior are unresolved. | U |
| R08 | Aim for a fully functional system allowing authorized users to download the full dataset and work with it. This is Carlos's high-level goal, not documented final faculty acceptance. | U |

## Confirmed proposal scope

| ID | Scope in the original proposal | Status |
| --- | --- | --- |
| P01 | Database/streaming framework for driving video and spatial telemetry, with standardized indexing and query APIs. | P; clarify streaming before design |
| P02 | Front-facing driving-camera data, GPS, road-environment metrics, and references to real-time telemetry. | P; available fields and live-ingestion obligations unknown |
| P03 | Existing collection of more than 10,000 clips, described as coming from an NIH project. | P; not independently counted; total bytes unknown |
| P04 | No requirement for complex LiDAR/radar pipelines. | P; do not introduce these as W1 deliverables |

Indexing/query and streaming remain intended OpenDriveDB capabilities. R08 does not replace them with a download-only scope. Query priorities and streaming acceptance need clarification.

## Current project decisions

- **D01:** OpenDriveDB is Project 1. Finish it before starting OpenDriveAnnotate (Project 2); use separate repositories.
- **D02:** Carlos's peer creates the official GitHub repository. No official repository exists yet; prepare local documentation for later integration.
- **D03:** Keep official dataset storage separate from source-code distribution. Do not publish real research samples by default; any exception needs confirmed data-sharing terms.
- **D06:** The existing requirements assign determination of the authentication layer to FAU (F). The interface, identity provider, and integration responsibilities remain open; do not select them independently.
- **D04:** Use lightweight repository documentation instead of formal SRS/SDD/STD documents.
- **D05:** Prepare conceptual development cases: video + GPS + OBD; video + GPS; video + OBD; video only. These are planned cases, not executed tests.

- **D07:** Users should be able to obtain and run the software on compatible personal, laboratory, or work computers. Installation, configuration, usage, and contribution instructions are expected as implementation develops; supported environments remain open.

## Working assumptions and deliberately unselected choices

- **A01:** Python is a plausible candidate based on Carlos's background; it is not selected. Neither FastAPI nor any database, package manager, CI, Docker setup, or protocol is selected.
- **A02:** A conceptual driving record links a video to optional telemetry. Actual file cardinality, trip segmentation, IDs, and storage schema depend on inspection.
- **A03:** Early work can use configurable placeholder locations and synthetic metadata. This cannot establish compatibility or performance with the real dataset.
- **A04:** Derived indexes/metadata can be stored separately from originals. Whether derivative media is permitted, and its retention/storage policy, must be resolved before implementation.
- **A05:** A 10-hour week is Carlos's planning budget. Earlier mid-semester/October targets are planning aspirations, not a verified delivery commitment; replan around dependencies.

## Proposed acceptance evidence — pending agreement

| Area | Evidence to agree and later demonstrate |
| --- | --- |
| Dataset compatibility | Inspect representative authorized ASF/GPS/OBD samples; document formats and associations with known limitations. |
| Index/query | Index available records and demonstrate the agreed queries, including all four telemetry-presence cases. |
| Integrity | Demonstrate originals remain unchanged during inspection, indexing, and retrieval; choose an agreed verification method. |
| Access/download | Show permitted full-dataset retrieval and denied unauthorized/expired access under the selected policy, including agreed failure/resume behavior. |
| Streaming | Define the required behavior first, then demonstrate it against agreed criteria. |
| Reproducibility | Document and test installation, configuration, and an example on agreed supported environments. |
| Scale/release | Agree dataset scale, performance thresholds, reviewer, licensing, and release evidence before claiming completion. |

No acceptance check above has been executed. W1 completes a documentation foundation, not functional delivery. See [questions](../notes/questions.md) for dependencies and [work log](../notes/work-log.md) for actual work.
