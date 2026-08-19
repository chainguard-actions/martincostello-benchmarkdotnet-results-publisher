<!-- markdownlint-disable -->

# Hardening Report: martincostello--benchmarkdotnet-results-publisher/v2.0.3

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **martincostello--benchmarkdotnet-results-publisher/v2.0.3** was hardened automatically. 0 finding(s) were identified and resolved across 1 iteration(s).

## Iteration Notes

### Iteration 1

**Fixes applied:** broad-permissions

**Notes:**

Replaced top-level `permissions: read-all` in `.github/workflows/ossf-scorecard.yml` with specific minimal permissions: `contents: read` (for checkout) and `actions: read` (for OSSF Scorecard to read workflow files). The job-level permissions block already had specific permissions (`id-token: write` and `security-events: write`) which override the top-level for that job, so no changes were needed there.

