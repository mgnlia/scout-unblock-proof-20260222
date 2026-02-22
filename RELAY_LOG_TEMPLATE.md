# Relay Log Template (relayLogId Convention)

Status: Active
Owner: Scout
Effective UTC: 2026-02-22T00:00:00Z

## 1) ID Convention
Use a unique immutable ID on every adversary relay package:

`relayLogId: RLY-<YYYYMMDD>-<HHMMSS>Z-<taskId>-<seq>`

Example:
`relayLogId: RLY-20260222-104500Z-CB5AA-01`

Rules:
- UTC only (`Z` suffix)
- Monotonic sequence per task (`01`, `02`, ...)
- One relayLogId per outbound relay event
- Must appear in: task description, GitHub receipt body, and (if sent) outbound message body

## 2) Required Fields (copy/paste)

```yaml
relayLogId: RLY-YYYYMMDD-HHMMSSZ-<taskId>-NN
sourceTaskId: <taskId>
recipient: <name/agentId>
outboundUtc: <ISO-8601 UTC>
packetA:
  parentHashes:
    - <repo>: <sha>
  inventoryUtc: <ISO-8601 UTC>
packetB:
  commitSha: <sha>
  parentSha: <sha>
  blobHash: <sha>
  packetUtc: <ISO-8601 UTC>
  pinnedUrl: <url>
  mutableUrl: <url>
gates:
  G1:
    requirement: New fingerprint (new SHA/blob)
    evidence: <text>
    result: PASS|FAIL
  G2:
    requirement: In-scope anchor evidence (contract URLs + #L + UTC)
    evidence: <text>
    result: PASS|FAIL
disposition: NIL(valid escalation packet)|VALID_ESCALATION_PACKET
suppressionTrail:
  - taskId: <id>
    updatedAtUtc: <ISO-8601 UTC>
notes: <optional>
```

## 3) Markdown Receipt Block

```md
## Relay Audit Record
- relayLogId: `RLY-YYYYMMDD-HHMMSSZ-<taskId>-NN`
- recipient: `<name/agentId>`
- outbound UTC: `<ISO-8601>`
- disposition: `NIL(valid escalation packet)`
```

## 4) Placement Checklist
- [ ] Added `relayLogId` to task description
- [ ] Added `relayLogId` to immutable GitHub receipt (issue/doc/comment)
- [ ] Added receipt URL to task `githubUrls`
- [ ] Included recipient + outbound UTC
- [ ] Included G1/G2 results
- [ ] Included disposition (`NIL(...)` or `VALID...`)

## 5) Non-Interference Rule
If parent task is in active adversary review (e.g., CB5AA), do not edit evidence unless reviewer requests net-new artifacts. For policy rollout, publish template in separate doc/repo artifact and apply on next relay event.
