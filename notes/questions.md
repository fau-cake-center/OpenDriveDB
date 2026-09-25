# Open questions and W2 dependencies

Updated: 2026-09-25. These are unresolved questions, not unanswered versions of facts Carlos has already confirmed. Move resolved answers into the relevant document with source/date. Suggested respondents below are not assigned owners or promises.

## W2 priorities

| Priority | Needed next | Suggested respondent/source | What it blocks |
| --- | --- | --- | --- |
| 1 | Official repository URL and contributor access; reconcile existing files and Carlos's original `.gitignore` | Carlos's peer / Carlos | Shared Git workflow; local documentation can continue |
| 1 | Representative ASF/GPS/OBD files and association documentation; confirm sample-request status | Peer / dataset custodian | Real parsing, synchronization, compatibility, evidence-based schema |
| 1 | Meaning of streaming and required query examples | Research lead | Final API, delivery, and architecture scope |
| 1 | Authorized inspection location and handling rules | FAU data custodian / research lead | Use or copying of real research data |
| 2 | FAU storage interface and deployment constraints | FAU infrastructure contact | Official storage integration and deployment |
| 2 | Temporary access lifecycle and full-download acceptance | Research lead / access administrator | Authorization and delivery implementation |

No external request was sent by this documentation task. Whether Carlos already requested samples is unverified.

## Dataset

- What resolutions, codecs, frame rates, durations, and corruption patterns occur in ASF files?
- What formats/fields/units do GPS and OBD use? Are they embedded, external, shared, or split?
- What identifies corresponding files? Are there manifests, trip/session boundaries, duplicates, or orphan telemetry?
- How common is missing GPS or OBD, and how should availability and unreadable data appear to users?
- Which road-environment metrics actually exist? What are their definitions?

## Synchronization

- What time bases, timestamp units, time zones, clock sources, offsets, and drift apply?
- Is alignment already provided? What should happen when it cannot be established?
- Are resampling or interpolation needed and permitted, and what accuracy is required?

## Privacy and governance

- May official data be copied to personal computers? Which inspection locations are authorized?
- What IRB, data-use, consent, or other institutional conditions apply?
- What images, locations, identifiers, metadata, and logs must remain private?
- May any real samples or derivatives be distributed? Current practice excludes real data from the source repository until terms are confirmed.

## Storage

- Which FAU-designated service, path conventions, read permissions, and interfaces will be used?
- Where may indexes, inspection outputs, and permitted derivatives be stored?
- Is more than one backend required? Who maintains storage, availability, and backups?

## Authorization and retrieval

The existing requirements assign the authentication layer to FAU.

- Which FAU-selected identity/authentication mechanism must OpenDriveDB integrate with, and who defines the integration contract?
- Who grants access, to whom, and using what identity/approval process?
- Does access expire by elapsed time, download completion, or another event? How is completion defined across multiple files?
- What are retry, resume, reuse, revocation, and partial-transfer rules?
- Must users retrieve the full dataset only, individual files, or query-selected subsets?
- What access logging is required, and what privacy/retention limits apply?

## Queries

- Which concrete user questions must v1 answer, and which metadata may be viewed before authorization?
- Are ID, time, location, telemetry availability, OBD values, or road metrics required filters? These are candidates only.
- What API format, pagination, response limits, and error behavior are needed?

## Streaming

- Does the proposal require remote playback, synchronized video/telemetry delivery, incremental download, live ingestion, or some combination?
- Are seeking, range requests, or derived playable media required and permitted?
- What latency, throughput, and client compatibility must be demonstrated?

## Scale and deployment

- What are the measured clip count, total bytes, growth, and concurrent query/download expectations?
- What performance thresholds and test environment are acceptable?
- What client operating systems and hardware must be supported?
- Where will any server component run, who operates it, and what network restrictions apply? GitHub source distribution does not settle these questions.

## Open source and release

- Which license and copyright notice are approved, and by whom?
- Who reviews/merges contributions, and what external contribution terms apply?
- What private security contact and reporting mechanism will be published?
- What citation, release/versioning, community code of conduct, and maintenance expectations apply?

## Definition of done and planning

- Who gives final acceptance, and what evidence demonstrates successful full-dataset retrieval?
- What required query/streaming behaviors, reproducibility checks, security checks, and performance thresholds define v1?
- How should the earlier mid-semester goal be revised around samples, repository access, and agreed scope?
- Are additional work sessions or hours missing from Carlos's existing work log? Preserve its recorded history; add actual hours for new work rather than copying planned durations.

## Work that can proceed while waiting

Refine these documents; prepare explicitly synthetic versions of cases A–D; define provisional interfaces and evaluation criteria without selecting a backend; review Git, Python application structure, API, and video concepts as needed. Label conclusions based only on synthetic data. Do not claim validated parsers, synchronization, storage integration, or release readiness.
