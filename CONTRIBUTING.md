# Contributing to Project Helix

## Branch and PR process

1. Create your phase branch from `develop`.
2. Make meaningful, atomic commits with descriptive messages.
3. Open a pull request using the PR template.
4. Link all relevant Jira issues (HELIX-XXX) in the PR description.
5. Include execution evidence (screenshots, reports, logs) in the PR.
6. Respond to any review comments before merging.
7. Merge only after all required checks pass.

## Commit message format

```
feat(phase-N): short description of what was added

- Detail 1
- Detail 2

HELIX-XXX
```

## Secrets and credentials

- Never commit credentials, tokens, or connection strings.
- Use `.env` files locally — these are gitignored.
- Reference `.env.example` for required environment variables.
- Use GitHub Secrets for CI/CD.
