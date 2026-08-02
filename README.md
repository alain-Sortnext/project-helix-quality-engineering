# Project Helix — Quality Engineering Programme
### GenomeBridge Clinical Systems Ltd

A structured eight-phase Quality Engineering simulation covering test strategy, exploratory testing, FHIR API validation, healthcare data quality, Cypress and Playwright automation, CI/CD, performance testing, and release readiness.

---

## Quick links

| Resource | Location |
|---|---|
| Company brief | `docs/company-brief/genomebridge_company_brief.md` |
| Quality strategy | `docs/quality-strategy/` |
| Exploratory charters | `manual-testing/exploratory-charters/` |
| Test scenarios | `manual-testing/test-scenarios/` |
| FHIR API tests | `api-testing/` |
| Database validation | `database/` |
| Cypress suite | `cypress/` |
| Playwright suite | `playwright/` |
| CI/CD workflows | `.github/workflows/` |
| Performance tests | `performance/k6/` |
| Release artefacts | `release/` |
| Phase reports | `reports/` |

## Branch strategy

| Branch | Purpose |
|---|---|
| `main` | Stable, reviewed work only |
| `develop` | Integration branch |
| `feature/phase-1-quality-discovery` | Phase 1 work |
| `feature/phase-2-exploratory-testing` | Phase 2 work |
| `feature/phase-3-fhir-api-testing` | Phase 3 work |
| `feature/phase-4-health-data-validation` | Phase 4 work |
| `feature/phase-5-cypress-regression` | Phase 5 work |
| `feature/phase-6-playwright-engineering` | Phase 6 work |
| `feature/phase-7-quality-pipeline` | Phase 7 work |
| `feature/phase-8-release-readiness` | Phase 8 work |

## Responsible testing

All test data is synthetic. No real patient information is used at any stage.
Credentials are stored in environment variables — never committed to this repository.
See `docs/decisions/synthetic-data-policy.md` for the full data-handling policy.

## Stack

TypeScript · Cypress · Playwright · Postman · PostgreSQL · k6 · axe-core · GitHub Actions · Jira Cloud

---

*GenomeBridge Clinical Systems Ltd is a fictional company created for educational purposes.*
