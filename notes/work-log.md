# OpenDriveDB — Work Log

## September 8, 2026 — Project Planning

### Completed
- Reviewed the OpenDriveDB and OpenDriveAnnotate project proposal.
- Identified the two systems as separate open-source software projects.
- Agreed with project peer to maintain two separate GitHub repositories.
- Decided to focus development on OpenDriveDB first and begin
  OpenDriveAnnotate after OpenDriveDB is completed.
- Reviewed the expected open-source repository structure and documentation.
- Established that formal SRS, SDD, and STD documents will not be used.
- Identified README, contribution instructions, security documentation,
  licensing, testing, and development documentation as repository needs.

### Pending
- Creation of the official OpenDriveDB GitHub repository by project peer.
- Initial project documentation.
- Clarification of dataset and system requirements.


## September 9, 2026 — Requirements and Documentation — 1 hour

### Completed
- Created initial local OpenDriveDB project documentation while waiting
  for the official GitHub repository.
- Drafted the initial README.
- Defined confirmed OpenDriveDB requirements.
- Separated confirmed requirements from assumptions and unresolved questions.
- Documented currently known dataset characteristics:
  - More than 10,000 driving videos.
  - Video format is ASF.
  - Videos are expected to have associated GPS and OBD data.
  - Some records may have missing GPS and/or OBD data.
  - File sizes are variable.
- Documented that official data will eventually use FAU-designated storage.
- Established that development can initially use placeholder/test data.
- Documented that the original research dataset should remain unchanged.
- Defined the preliminary temporary-access concept for dataset users.
- Established initial completion criteria for OpenDriveDB.
- Created a structured list of unresolved technical, data, privacy,
  authorization, streaming, deployment, and open-source questions.

### Pending
- Inspect representative sample data.
- Determine GPS and OBD formats.
- Clarify data synchronization.
- Clarify privacy and data-use restrictions.
- Clarify the exact definition of streaming.
- Receive official GitHub repository.


## September 10, 2026 — Data Model Planning — 1 hour

### Completed
- Reviewed the initial OpenDriveDB requirements and open questions.
- Defined a preliminary conceptual data model centered around a driving
  record containing:
  - Video
  - Optional GPS data
  - Optional OBD data
- Identified video metadata that must be inspected, including resolution,
  FPS, codec, duration, timestamps, and naming conventions.
- Identified GPS and OBD characteristics that must be determined from
  representative samples.
- Created a dataset inspection checklist for future sample data.
- Defined cases that development/test data should represent:
  - Video + GPS + OBD
  - Video + GPS without OBD
  - Video + OBD without GPS
  - Video without GPS or OBD
- Established that early development should not depend on access to the
  complete official dataset.
- Continued identifying information required before selecting the final
  OpenDriveDB architecture.

### Pending
- Receive representative ASF, GPS, and OBD samples.
- Inspect actual dataset structure.
- Determine video-to-telemetry association mechanism.
- Determine timestamp/synchronization structure.
- Determine GPS and OBD schemas.
- Clarify streaming requirements.
- Begin technical architecture evaluation.



## September 15, 2026 — Current Status

### Current Project Phase
Requirements and data-understanding phase.

### Completed So Far
- Initial project scope established.
- Repository strategy established.
- Open-source documentation strategy established.
- Initial requirements documented.
- Open questions documented.
- Preliminary data model established.
- Dataset inspection procedure established.
- Development/test-data strategy established.

### Next Major Milestone
Obtain and inspect representative video, GPS, and OBD data before making
major technical architecture or implementation decisions.

## September 25, 2026 — W1 documentation reconciliation

### Completed in this update
- Inspected the actual RA/OpenDriveDB folder, including hidden files, and read the original research proposal plus the open-source guidance document.
- Updated README, requirements, conceptual data model, inspection checklist, and open questions against the proposal, Carlos's conversation decisions, and existing files.
- Retained the existing note that FAU determines the authentication layer; no mechanism or stack was chosen.
- Preserved every earlier work-log entry and recorded hour above. Their previous Pending lists describe those historical dates; use the current status below for today's checkpoint.
- Filled the empty CONTRIBUTING.md, SECURITY.md, and ROADMAP.md with lightweight drafts.
- Created .gitignore because none was present in the supplied folder, including hidden files. Carlos previously mentioned creating one; reconcile that copy if it is found elsewhere.
- Defined the four telemetry-presence cases and non-destructive inspection evidence. These remain planned cases, not executed tests.
- Checked local documentation links, Markdown fences, file coverage, ignore-rule examples, and preservation of the historical log. No application tests were available or run.

### Time
Actual hours for this update: not recorded; Carlos should enter actual time. No earlier dates or hours were revised.

### Current W1 checkpoint and W2 dependencies
- Documentation foundation is updated; no official GitHub repository exists yet. Peer creation/access remains pending. No Git initialization, remote configuration, commit, or push was performed.
- No representative ASF/GPS/OBD files are available. Real inspection, parser validation, synchronization, and evidence-based schema selection remain blocked. Whether a sample request was previously sent is unverified; this task sent no messages.
- Original proposal verification is complete. Official data handling permissions, storage interface, streaming/query priorities, authorization lifecycle, final acceptance, and licensing still need decisions.
- Synthetic/test data work can proceed independently; no synthetic fixtures were created in this documentation update.
- The personal schedule in ../ROADMAP.txt (relative to the project root) remains unchanged. Its September 25 data-understanding target has not been achieved; October 23 release and October 26 Project 2 start are provisional, not commitments. Project 2 starts only after Project 1 completion. See ROADMAP.md at the project root.

### Next actions
1. Confirm sample-request status, request representative data through the project contacts, and confirm its permitted inspection location.
2. Obtain the official repository URL/access from the peer; merge these materials into its clone without overwriting other work.
3. Inspect authorized samples when available; otherwise prepare clearly labeled synthetic cases and keep their limitations explicit.
4. Resolve priority streaming, query, FAU storage/authentication, and acceptance questions; revise milestones based on evidence.

### Future entry template
| Date | Actual hours | Completed work / evidence | Decisions / source | Blockers / next action |
| --- | --- | --- | --- | --- |
| To enter | To enter | To enter | To enter | To enter |
