# Monday — Repository Assessment and Branching Strategy

## 1. Purpose
Establish how the team will store, review and validate project changes.

## 2. Repository assessment
- Repository: `shamanthnb36/facial-recognition-cicd` [confirm this is the approved project repository]
- Default branch: [confirm in GitHub Settings → Branches]
- Current source components present: [inspect repository; list actual folders]
- Existing workflows: [inspect `.github/workflows/`]
- Collaborators and permissions: [confirm with project lead]
- Repository model recommendation: **Use the currently approved repository structure.** Do not split or
  reorganize repositories without project-lead approval.
- Assessment date: [date]
- Open questions: [list items awaiting confirmation]

## 3. Proposed branching strategy
- `main`: stable, reviewed baseline; direct pushes should be restricted if branch protection is available.
- `feature/<short-name>`: new application features.
- `fix/<short-name>`: bug fixes.
- `docs/<short-name>`: documentation-only changes.
- `ci/<short-name>`: CI/CD and workflow changes.
- Work is proposed through pull requests; reviewers and required checks must be agreed by the team.
- Keep branches focused and avoid committing secrets, generated files, virtual environments or local `.env` files.

## 4. Commit convention
Use clear, imperative messages:
- `docs: add repository onboarding guide`
- `ci: add initial GitHub Actions validation`
- `fix: correct workflow validation step`

## 5. Proposed minimum pull-request checks
1. Workflow YAML parses and runs.
2. Repository structure/required files are validated.
3. Lint, tests and build checks run when the relevant application code and commands are available.
4. Review completed by an approved teammate.
5. Failed required checks are resolved before merge, unless an explicit exception is approved and recorded.

## 6. Acceptance criteria
- [ ] Default branch and permissions verified.
- [ ] Actual repository contents recorded.
- [ ] Branch naming and PR expectations reviewed with team.
- [ ] Repository structure changes approved before implementation.
