# Thursday — Pipeline Integration Notes and Risks

## Coordination log
| Team / owner | Required information | Status / response |
|---|---|---|
| Team 1 — Backend / AI-ML | Python version, dependencies, FastAPI startup, recognition runtime/model, DB migrations | [pending/confirmed] |
| Team 2 — Frontend / QA | Node.js version, package manager, lint/test/build commands, environment variables | [pending/confirmed] |
| Chandrika | Docker Compose, environment variables, secret injection, local service dependencies | [pending/confirmed] |
| Project lead / Mehak | Approved repository structure, branch policy, environment ownership and deployment priorities | [pending/confirmed] |

## Known risks
- Application modules or tests may not yet exist.
- Pipeline checks may be incomplete until teams provide real commands.
- Model downloads or CPU-only recognition may make tests slow or hardware-dependent.
- CI secrets and production deployment permissions are not required for the initial validation workflow.
- Ports, credentials and production endpoints must not be guessed or hard-coded.

## Decisions required
| Decision | Owner | Due date | Status |
|---|---|---|---|
| Confirm default branch and required PR checks | Project lead / admin | [date] | Pending |
| Confirm frontend/backend validation commands | Team 1 and Team 2 | [date] | Pending |
| Confirm artifact retention | Project lead | [date] | Pending |
| Confirm future environment promotion process | Team 3 + project lead | [date] | Pending |
