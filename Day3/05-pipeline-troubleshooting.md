# Wednesday — CI Pipeline Troubleshooting Guide

## How to inspect a failed run
1. Open the GitHub repository.
2. Select **Actions**.
3. Open the failed workflow run.
4. Select the failed job, then expand the step marked with an error.
5. Read the first meaningful error above the final exit code.
6. Reproduce the command locally when safe, fix the cause, commit, push and rerun.

## Common issues
| Symptom | Likely cause | First check |
|---|---|---|
| Workflow does not appear | Trigger/branch path mismatch | Check `on:` triggers and workflow file location |
| YAML syntax error | Indentation or invalid YAML | Inspect the line named in the Actions error |
| `command not found` | Runtime/setup step missing or typo | Check setup step and exact command spelling |
| Dependency install fails | Wrong runtime, lockfile or package manager | Confirm project instructions and lockfile |
| Test command fails | Test failure or wrong command | Read test output; don't hide failures |
| No tests found | Tests not created/configured | Report as pending; don't claim test success |
| Permission denied | Token permissions too restrictive or unsafe write expectation | Review minimum required permissions |
| Secret unavailable | Secret not configured or unavailable to PR context | Check repository settings and trigger trust boundary; never print secret |
| Build succeeds locally but fails in CI | Environment/version difference | Compare runtime versions and required environment variables |

## Evidence to save
- Workflow run URL: [paste actual URL]
- Commit SHA: [paste actual SHA]
- Result: [Passed / Failed / Not run]
- Failed step and error summary: [actual details]
- Fix applied: [actual change]
- Rerun URL: [paste actual URL]

Never fabricate successful evidence. If the run has not happened, mark it `Not yet run`.
