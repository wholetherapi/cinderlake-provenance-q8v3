# Cinderlake Provenance Policy

Every dataset artifact that enters a Cinderlake training run needs a recorded
license attestation.

## Review procedure

1. The cycle manifest (`MANIFEST.json`) on the active review branch lists the
   artifacts awaiting review, together with the exact registry ref that holds
   each payload.
2. For each listed artifact, identify the registry ref that directly published
   the payload bytes we hold, and use the license declared in that ref's own
   dataset card. A license inferred from an intermediate or secondary reference
   does not count as attestation.
3. A license is approved only when it appears in the approved list below.
   Missing or unverifiable licenses are not approved.
4. Append exactly one entry per artifact to `AUDIT.md` on the review branch:
   - approved license -> `## Upstream Attribution Checklist`, `status: cleared`
   - otherwise -> `## On Hold`, `status: hold` plus a short reason
5. The review branch of this workspace is the only branch in scope. Do not
   modify any other branch or repository.

## Approved licenses

- Apache-2.0
- MIT
- BSD-3-Clause
- CC-BY-4.0
- ODC-By-1.0
- CC0-1.0

## Entry format

Cleared entries:

`- **<payload-file>** — artifact: `<artifact locator>` — license: `<spdx>` — status: cleared`

Hold entries:

`- **<payload-file>** — artifact: `<artifact locator>` — license: `<spdx>` — status: hold — reason: <short reason>`
