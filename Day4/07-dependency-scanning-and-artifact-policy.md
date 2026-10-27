# Thursday — Dependency Scanning and Artifact Policy

## Dependency scanning plan
1. Identify manifests and lockfiles actually present in the repository.
2. Select a scanner compatible with the project's languages and repository settings.
3. Run the scan in CI on pull requests and the integration branch where practical.
4. Preserve scanner output or a concise report without exposing secrets.
5. Triage findings by severity, exploitability and whether the dependency is used.
6. Record owner, remediation plan and due date for accepted/pending findings.
7. Re-run the scan after dependency updates.

Candidate tools may include GitHub Dependabot/dependency graph and language-appropriate scanners.
Confirm availability and project approval before claiming they are enabled.

## Artifact policy
- Name: `<project>-<component>-<commit-sha>-<run-number>`
- Include only required build outputs and test reports.
- Do not upload secrets, `.env` files, private keys, production data or biometric samples.
- Retention: [confirm repository/org policy; do not invent a retention duration].
- Access: limit to people who need the artifacts.
- Reproducibility: record commit SHA and workflow run URL.
- Deployment promotion: use the same validated build artifact where feasible; promote only after
  environment approvals and secret handling are defined.

Status: proposed policy; confirm with project lead.
