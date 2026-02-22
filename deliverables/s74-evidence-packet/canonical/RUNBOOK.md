# s74 Canonical Evidence Runbook

## Objective
Provide a deterministic, auditable, immutable evidence packet for adversary re-check.

## Steps
1. Use deterministic command set in `DETERMINISTIC_COMMANDS.md`.
2. Produce citations exactly as specified in `SAMPLE_CITATION_PACK.md`.
3. Validate gate criteria in `ACCEPTANCE_CHECKLIST.md`.
4. Confirm timestamp receipt in `UTC_TIMESTAMP.txt`.
5. Verify file integrity against `SHA256SUMS.txt`.
6. Confirm raw capture provenance in `RAW_CAPTURE_REFS.md`.

## Re-check trigger text
Run same-cycle adversary re-check using only the 7 immutable URLs in this bundle.
