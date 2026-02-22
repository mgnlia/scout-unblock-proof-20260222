# d6A9 Canonical Owner-Auth Packet (Template)

Status: TEMPLATE_READY (not a final publish)

Supersession note:
This packet supersedes all prior conflicting/non-canonical d6A9 deployment-identity claims. Adversary must evaluate ONLY the SHA-pinned links declared in this packet.

## 1) Owner-auth dashboard proof (REQUIRED)
- `DASHBOARD_PROOF_URL` (immutable): `<PASTE_IMMUTABLE_URL_SHOWING_DEPLOYMENT_ID_AND_CREATED_AT>`
- Must visibly include both fields:
  - `deploymentId`
  - `createdAt` (UTC or explicitly timezone-qualified)

## 2) Canonical SHA declaration (single source of truth)
- `CANONICAL_SHA`: `<40-char-commit-sha>`
- Rule: every packet link below MUST use exactly this same SHA.

## 3) SHA-consistent direct links (immutable only)
- `PACKET_SELF_URL`:
  - `https://github.com/<org>/<repo>/blob/<CANONICAL_SHA>/deliverables/d6a9-owner-auth-packet/FINAL_CANONICAL_OWNER_AUTH_PACKET.md`
- `PACKET_SELF_RAW_URL`:
  - `https://raw.githubusercontent.com/<org>/<repo>/<CANONICAL_SHA>/deliverables/d6a9-owner-auth-packet/FINAL_CANONICAL_OWNER_AUTH_PACKET.md`
- `DASHBOARD_PROOF_REF_URL` (if repo-hosted export/screenshot JSON/MD):
  - `https://raw.githubusercontent.com/<org>/<repo>/<CANONICAL_SHA>/deliverables/d6a9-owner-auth-packet/<proof-file>`

## 4) Contradiction controls (must be explicit)
- Mutable-link usage disposition: REJECT
- Scope/target mismatch disposition: REJECT
- SHA inconsistency disposition: REJECT
- Supersession-chain gaps disposition: REJECT

## 5) One-shot publish checklist (must all be true)
- [ ] Dashboard proof URL is immutable and shows deploymentId + createdAt
- [ ] Exactly one canonical SHA declared
- [ ] All links are SHA-pinned and match canonical SHA
- [ ] Supersession note included
- [ ] Packet published in one update (no partial fragments)

## 6) Same-cycle adversary re-check request text
"Run same-cycle adversary re-check on d6A9 using ONLY this one-shot immutable owner-auth packet: <IMMUTABLE_PACKET_URL>. Validate: (1) dashboard proof includes deploymentId + createdAt, (2) single canonical SHA declaration, (3) SHA-consistent immutable links only, (4) explicit supersession note, (5) explicit contradiction disposition for mutable-link usage, scope/target mismatch, SHA inconsistency, and supersession-chain gaps. Return ACCEPT/REJECT."
