<!-- markdownlint-disable -->

# Hardening Report: martincostello--benchmarkdotnet-results-publisher/v2.1.0

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **martincostello--benchmarkdotnet-results-publisher/v2.1.0** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### broad-permissions (severity: medium)

The workflow file has a top-level `permissions: read-all` setting, which grants overly broad read access to all GitHub Actions scopes. This should be replaced with specific minimal permissions required by each job. Note: the file contains a `# zizmor: ignore[excessive-permissions]` comment, but per security policy this must still be flagged.

Locations:

- `.github/workflows/ossf-scorecard.yml:13`

## Iteration Notes

### Iteration 1

**Fixes applied:** broad-permissions

**Notes:**

Replaced top-level `permissions: read-all` with `permissions: contents: read` in `.github/workflows/ossf-scorecard.yml`. The job already had its own specific permissions block (`id-token: write`, `security-events: write`) which overrides the top-level for the analysis job. The `# zizmor: ignore[excessive-permissions]` comment was removed as it's no longer needed.

