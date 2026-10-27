# Monday — Developer Onboarding and CI/CD Requirements

## Developer onboarding checklist
- [ ] Obtain access to the approved GitHub repository.
- [ ] Install Git and the runtime required for the component being developed.
- [ ] Clone the repository and check out the approved development branch.
- [ ] Read the README and relevant component setup guide.
- [ ] Copy `.env.example` to a local environment file if the project provides one; never commit real secrets.
- [ ] Run the component's documented local validation commands.
- [ ] Create a focused branch using `feature/`, `fix/`, `docs/` or `ci/`.
- [ ] Commit with a clear message and open a pull request.
- [ ] Review CI results and fix failures before requesting final review.

## CI/CD requirements
The initial pipeline should validate what is actually present in the repository and clearly identify
missing or unfinished application modules rather than pretending they were tested.

### Initial CI stages
1. Checkout source.
2. Set up only the required runtime(s).
3. Validate repository structure and workflow configuration.
4. Run available formatting/lint checks.
5. Run available automated tests.
6. Run build validation when supported by the current code.
7. Publish useful logs/test reports where configured.
8. Leave deployment as a future stage until environments, approvals and secrets are agreed.

### Trigger proposal
- Pull requests targeting the approved integration branch.
- Pushes to the approved integration branch.
- Manual runs for troubleshooting, if useful.

### Failure policy
A required validation failure should produce a failed workflow. Missing application components must be
reported explicitly as `not yet implemented` or `not configured`; do not label them as passed.

### Dependencies to confirm
- Frontend: Node.js version, package manager, lint/test/build commands — owner: Team 2.
- Backend: Python version, dependency file, lint/test/start commands — owner: Team 1.
- Recognition service: runtime/model requirements and test approach — owner: AI/ML.
- Database: migration and test-database approach — backend owner.
- CI permissions and repository settings — project lead / repository admin.
