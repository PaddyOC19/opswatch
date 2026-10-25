# OpsWatch Troubleshooting Log

A record of actual technical problems, investigations,
root causes and solutions encountered during development.

## 001 — GitHub CLI Authentication

**Date:** 24 October 2026
**Status:** Resolved
**Category:** Development environment

### Problem

The GitHub CLI was installed but not authenticated.

### Evidence

Running `gh auth status` reported:
"You are not logged into any GitHub hosts."

### Root Cause

GitHub CLI authentication had not been configured.

### Resolution

1. Ran `gh auth login`.
2. Selected GitHub.com and HTTPS.
3. Completed browser authentication.
4. Verified the active account using `gh auth status`.

### Verification

Successfully authenticated as PaddyOC19.

### Lesson Learned

Installing a CLI tool does not automatically authenticate
it with an external service.
