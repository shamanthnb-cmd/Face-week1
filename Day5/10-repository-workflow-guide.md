# Repository Workflow Guide

## Typical contribution
1. Update local `main` from the remote approved branch.
2. Create a task branch, for example `docs/add-onboarding-guide`.
3. Make a focused change.
4. Run applicable checks locally.
5. Commit with a descriptive message.
6. Push the branch and open a pull request.
7. Review the CI checks and address failures.
8. Request review and merge only according to the approved team policy.

Example commands (replace branch names as needed):
```bash
git switch main
git pull
git switch -c docs/add-onboarding-guide
git status
git add docs/
git commit -m "docs: add onboarding guide"
git push -u origin docs/add-onboarding-guide
```

## Safe Git habits
- Check `git status` before adding files.
- Do not commit `.env`, credentials, personal data, face images or generated model files.
- Avoid force-pushing shared branches.
- Ask for review before repository-wide or branch-protection changes.
- Read the Actions logs before changing a workflow blindly.
