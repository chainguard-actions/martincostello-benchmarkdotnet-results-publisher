<!-- markdownlint-disable -->

# Hardening Report: martincostello--benchmarkdotnet-results-publisher/v2.1.1

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **martincostello--benchmarkdotnet-results-publisher/v2.1.1** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### broad-permissions (severity: medium)

The workflow file ossf-scorecard.yml has a top-level `permissions: read-all` which grants overly broad read access to all GitHub Actions scopes. This should be replaced with specific minimal permissions scopes. (Note: the file contains a `# zizmor: ignore[excessive-permissions]` comment acknowledging this, but it still fails the broad-permissions check.)

Locations:

- `.github/workflows/ossf-scorecard.yml:12`

## Iteration Notes

### Iteration 1

**Fixes applied:** broad-permissions

**Notes:**

Replaced `permissions: read-all` at the top level of `.github/workflows/ossf-scorecard.yml` with `permissions: contents: read`. The job-level permissions (`id-token: write`, `security-events: write`) were already correctly scoped and remain unchanged. The `# zizmor: ignore` comment was also removed since the broad permission is no longer present.

