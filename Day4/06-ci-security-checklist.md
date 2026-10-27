# Thursday — CI Security Checklist

Mark each item `Pass`, `Fail`, or `Pending`; add evidence or owner.

- [ ] Workflow uses least-privilege `permissions`.
- [ ] Pull-request workflow does not expose deployment or production secrets to untrusted code.
- [ ] No passwords, API tokens, private keys or production credentials are committed.
- [ ] `.env` and local secret files are excluded from Git; `.env.example` uses placeholders only.
- [ ] Third-party actions and dependencies are reviewed and kept updated under team policy.
- [ ] Workflow triggers are limited to intended branches/events.
- [ ] Fork PR and other untrusted contribution behavior is considered.
- [ ] Logs do not print secrets, face images, biometric templates or other sensitive data.
- [ ] Failed required checks prevent normal merge, subject to approved repository policy.
- [ ] Dependency vulnerability findings have a documented triage process.
- [ ] Artifacts do not contain credentials or sensitive user data.
- [ ] Exceptions include an owner, reason and review date.

## Finding policy proposal
- Critical/high findings: block merge/release until fixed or formally accepted by the authorized owner.
- Medium/low findings: record, prioritize and assign a due date according to project policy.
- Do not claim compliance or a clean scan until a scan has actually run.

Review date: [date]
Reviewed by: [names]
Outstanding risks: [list]
