# Security Policy — Project Helix

## Synthetic data requirement

All data used in this project must be synthetic or public demonstration data.
No real patient information may appear in any file, commit, log, screenshot, or artefact.

## Credential handling

- Connection strings, API keys and tokens must never be committed to this repository.
- Store secrets locally in `.env` (gitignored).
- Use GitHub Secrets for CI/CD pipelines.
- Reference `.env.example` to document required variables without exposing values.

## Reporting a concern

If you identify a credential exposure or data handling issue in this repository,
open a GitHub Issue labelled `security` immediately.
