# Security — W1 draft

No application release exists and no supported-version policy, security response commitment, or dedicated reporting contact has been established. The official repository is not yet available. This document must be completed before a public release.

## Reporting a concern now

Do not post credentials, exploitable details, research videos, telemetry, or identifying dataset information in public issues or discussions. Use an existing private project communication channel to ask Carlos or the research lead for the appropriate security contact before sending sensitive details. No email address or GitHub private-reporting feature is claimed to be configured.

Once a private channel is confirmed, provide a minimal description, affected component/version if any, impact, and safe reproduction steps using synthetic data. Do not include live credentials or restricted files.

## Data and access boundaries

- Keep original data unchanged and in FAU-designated storage. Confirm permissions before making copies, especially on personal computers.
- Keep official data, private inspection reports, local credentials, and access links out of Git. Review staged changes even when ignore rules are present.
- Open-source code distribution does not grant dataset access or redistribution rights.
- Temporary authorization is intended. Existing requirements assign the authentication layer to FAU; the actual mechanism, expiry, revocation, resume behavior, and audit policy remain unresolved. Do not treat placeholder access logic as production security.
- If a secret is exposed, notify the responsible owner privately and arrange revocation/rotation; removing a file in a later commit alone does not remove exposure.

## Items to settle before release

Confirm a private reporting contact/process, responsible responders, supported versions, institutional data-handling requirements, authorization behavior and validation, and any logging/retention rules. These are pending decisions, not assurances that controls have been implemented.
