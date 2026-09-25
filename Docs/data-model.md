# Conceptual data model — W1

Updated: 2026-09-25. Planning model only; no database schema or parser contract is selected. Evidence labels follow [requirements](requirements.md).

## Established relationships

```text
DrivingRecord (conceptual)
  ├── Video: required, ASF
  ├── GPS: optional
  └── OBD: optional
```

GPS and OBD are expected, but either or both may be absent (U). Optional here means absence must be supported; it does not mean missing data should be silently fabricated. Original files remain in FAU-designated storage and unchanged (U).

## Candidate information to capture after inspection

| Concept | Candidate information | Unresolved |
| --- | --- | --- |
| Record | Stable reference, source provenance, association status | ID source, uniqueness, trip/session boundaries |
| Video | External location/reference, container, codec, duration, resolution, frame-rate metadata | Actual codecs, timestamp semantics, valid ranges |
| GPS | Source reference, fields, time basis, coordinate representation | File format, units, coordinate system, sampling |
| OBD | Source reference, available parameters, units, time basis | Encoding, parameter meanings, sampling |
| Association | Evidence connecting sources and any alignment uncertainty | Naming rules, manifest/IDs, offsets, drift, cardinality |
| Inspection | Findings, inspection date, errors, source identity | Persistent format and validation rules |

These are candidate metadata categories (A), not mandatory columns. Telemetry may be separate, embedded, shared among videos, or split across files; no one-file-per-video rule has been established. Do not invent speed, RPM, timestamps, coordinate units, or a trip identifier as confirmed fields.

## Proposed handling semantics

- Distinguish confirmed absence from not-yet-inspected, unreadable, and ambiguous associations. Exact status names and API representations remain open.
- A video with missing telemetry should remain representable. Do not use zero coordinates or zero measurements to mean missing.
- A record with no video is outside this conceptual model; report orphan telemetry for investigation rather than discarding or attaching it arbitrarily.
- Preserve source timestamps and units when recording observations. Do not assume UTC, Unix time, common clocks, interpolation, or synchronized sampling.
- Keep authorization policy separate from descriptive record metadata; no token tables or user roles are specified yet.

## Development cases

| Case | Video | GPS | OBD | Intended check once implemented |
| --- | --- | --- | --- | --- |
| A | Present | Present | Present | Represent both associations |
| B | Present | Present | Missing | Represent missing OBD explicitly |
| C | Present | Missing | Present | Represent missing GPS explicitly |
| D | Present | Missing | Missing | Represent video-only record |

No fixtures or tests have been created or run. Synthetic metadata can exercise these relationships, but cannot validate actual ASF decoding or telemetry parsing. Additional negative cases to consider later: unreadable video, ambiguous matches, orphan telemetry, and incompatible timestamps. Agree expected behavior before writing assertions.
