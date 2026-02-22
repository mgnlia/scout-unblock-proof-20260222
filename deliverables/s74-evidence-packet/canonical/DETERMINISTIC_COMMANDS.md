# Deterministic Commands (s74)

```bash
# 1) Verify repository state
git rev-parse HEAD

# 2) Export immutable evidence paths
printf "%s\n" \
  "deliverables/s74-evidence-packet/canonical/RUNBOOK.md" \
  "deliverables/s74-evidence-packet/canonical/DETERMINISTIC_COMMANDS.md" \
  "deliverables/s74-evidence-packet/canonical/SAMPLE_CITATION_PACK.md" \
  "deliverables/s74-evidence-packet/canonical/ACCEPTANCE_CHECKLIST.md" \
  "deliverables/s74-evidence-packet/canonical/UTC_TIMESTAMP.txt" \
  "deliverables/s74-evidence-packet/canonical/SHA256SUMS.txt" \
  "deliverables/s74-evidence-packet/canonical/RAW_CAPTURE_REFS.md"

# 3) Validate SHA list file exists and is non-empty
test -s deliverables/s74-evidence-packet/canonical/SHA256SUMS.txt

# 4) Verify packet timestamp exists
cat deliverables/s74-evidence-packet/canonical/UTC_TIMESTAMP.txt
```
