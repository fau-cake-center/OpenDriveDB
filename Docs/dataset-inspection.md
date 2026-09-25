# Dataset inspection plan — W1

Updated: 2026-09-25. **Not yet performed: no representative files are available.** This document is a checklist and reporting template, not dataset findings.

## Request and prerequisites

- [ ] Confirm whether a sample request has already been sent; record date, recipient, and response in the work log. This task did not send one.
- [ ] Request an authorized representative ASF clip with corresponding GPS and OBD, any field definitions/manifests, and known association rules.
- [ ] Request missing-GPS, missing-OBD, and video-only examples if available; otherwise mark those cases synthetic.
- [ ] Include differing codecs, durations, file sizes, and telemetry layouts if known. One sample cannot establish full-dataset consistency.
- [ ] Confirm permitted storage/inspection environment and whether personal-machine copies or extracts are allowed.
- [x] Check the original proposal for scope (2026-09-25). This does not substitute for sample inspection.

## Non-destructive inspection

- [ ] Work from authorized locations with read-only access where available. Do not rename, overwrite, repair, transcode in place, or add files to the official dataset.
- [ ] Record source identifiers and provenance in an approved private location. Keep identifying filenames, GPS coordinates, and private paths out of public notes.
- [ ] Store inspection outputs separately. If copies or derived media are needed, resolve permissions and destinations first.
- [ ] Select an integrity check, such as existing checksums or agreed before/after hashes for samples; record what was actually checked. No checksum procedure has been run yet.

## Video

- [ ] Inspect actual container and codec(s), including audio if present; ASF is a container, not a confirmed codec.
- [ ] Record bytes, duration, dimensions, frame-rate/time-base information, and whether frame timing varies.
- [ ] Determine available timestamps and their meaning, start offsets, seeking behavior, and partial/unreadable-file behavior.
- [ ] Record tool and version used (for example, an approved metadata probe); tool selection is pending.

## GPS and OBD

- [ ] Identify whether each source is embedded or external, its format/encoding, delimiters, header/schema, row counts, and missing-value conventions.
- [ ] Record observed fields, units, valid-value documentation, and timestamp representation without inventing unknown meanings.
- [ ] For GPS, determine coordinate system, precision, and sampling pattern.
- [ ] For OBD, determine parameter identifiers, units, sampling patterns, and gaps.
- [ ] Identify duplicates, malformed rows, irregular sampling, and absent sources separately.

## Association and synchronization

- [ ] Inspect naming conventions, manifests, shared IDs, and video/telemetry cardinality.
- [ ] Determine clock sources, time zones if applicable, offsets, drift, overlaps, and gaps.
- [ ] Record whether alignment is documented, inferred, or unavailable. Do not silently interpolate or assume matching start times.
- [ ] Identify road-environment metrics if actually present; do not infer that every proposal concept has supplied fields.

## Four-case checklist

| Case | Required combination | Available now | Evidence needed |
| --- | --- | --- | --- |
| A | Video + GPS + OBD | No | Valid associations and observed schemas |
| B | Video + GPS | No | Explicit OBD absence |
| C | Video + OBD | No | Explicit GPS absence |
| D | Video only | No | Both telemetry sources absent |

All cases are planned. Clearly label future synthetic fixtures, document their invented format, and keep them separate from official data. Tiny non-sensitive text fixtures may later live under `tests/fixtures/`; no fixture format is approved yet. The provisional `.gitignore` excludes ASF files by default; any future synthetic media exception should be narrow and reviewed.

## Observation template

| Item | Observation |
| --- | --- |
| Inspector / date / tool version | Not recorded |
| Authorized source reference (private where needed) | Not available |
| Real or synthetic; selection rationale | Not available |
| Video metadata | Not inspected |
| GPS/OBD fields, units, sampling | Not inspected |
| Association evidence and time basis | Not inspected |
| Missing/unreadable/ambiguous elements | Not inspected |
| Integrity verification and output location | Not performed |
| Representativeness limits | Unknown |
| Design implications / questions raised | Pending inspection |

After inspection, populate actual observations, update requirements and questions, and propose the first schema and technical stack with evidence. Keep sensitive raw reports outside the public repository.
