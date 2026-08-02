## Company Brief — GenomeBridge Clinical Systems Ltd

### Project Helix: Clinical Genomics Quality Engineering Programme

---

## 1. Who GenomeBridge Is

GenomeBridge Clinical Systems Ltd is a fictional UK HealthTech company. It builds clinical
referral, patient-record and genomic-testing workflow technology used by NHS-facing laboratory
and diagnostic partners.

GenomeBridge does not process real patient data in any environment used by this programme. All
records used in Project Helix are public demonstration data or synthetically generated data.

---

## 2. The Ten-Step Workflow Under Review

Project Helix exists to test and evidence the reliability of the digital workflow used to:

1. Locate or register a patient.
2. Review patient demographic information.
3. Create a clinical referral.
4. Record consent.
5. Create a genomic test request.
6. Associate a specimen with the request.
7. Track the processing status.
8. Make a diagnostic report available.
9. Control access to clinical information.
10. Retain a traceable history of material activity.

---

## 3. Why Now — The Current Metric

GenomeBridge's support desk (James Wright, Service Support Lead) has logged a sharp rise in
complaints over the last quarter tied to steps 1, 6 and 7 above — patients being hard to locate,
specimens not always linking correctly to the service request that should track them, and users
reporting session interruptions mid-workflow.

**Headline figure (reported, not yet verified):** James's team estimates that specimen-to-request
linkage problems are now a "common" cause of delayed genomic test turnaround, but no one has
quantified this against actual workflow data. Daniel Brooks (Engineering Manager) has said openly
in standup that engineering "does not trust the current numbers enough to act on them."

**This is the candidate's first job: turn an anecdote into evidence.**

---

## 4. The Target

GenomeBridge's internal release-readiness bar for Project Helix, set by Daniel Brooks and agreed
with Dr Maya Patel (Product Manager), is:

- No more than a small, explicitly-justified residual rate of specimen-to-request linkage defects
  at release, with every instance traced to a root cause and a documented mitigation.
- Zero unresolved P1 (critical) defects at the Go/No-Go review.
- A consolidated body of evidence — not a raw count of tests passed — supporting the release
  decision.

There is no fixed numeric target published to the candidate at programme start. Part of Phase 1
and Phase 2 is establishing what "acceptable" looks like from the data itself, and defending that
judgement later.

---

## 5. Cost of the Gap

Dr Maya Patel's business case for Project Helix estimates that unresolved workflow reliability
problems — rework, delayed diagnostic turnaround, and support overhead — are costing GenomeBridge
in the region of **£340,000 per year** if left unaddressed going into the next release cycle. This
figure is cited to partners and is part of why the release date is fixed rather than negotiable.

---

## 6. The Deadline

Project Helix runs over **eight weeks**, following a one-off workplace setup period before Phase 1
begins.

| Milestone | Date |
|---|---|
| Workplace Setup Gate (not a scored phase) | Before Monday 4 August 2026 |
| Phase 1 — Product Discovery, Risk and Test Strategy | Week 1: Mon 4 Aug – Fri 8 Aug 2026 |
| Phase 2 — Exploratory Testing, Test Design and Defect Triage | Week 2: Mon 11 Aug – Fri 15 Aug 2026 |
| Phase 3 — FHIR API Quality Engineering | Week 3: Mon 18 Aug – Fri 22 Aug 2026 |
| Phase 4 — Health Data Quality, SQL and Test-Data Management | Week 4: Mon 25 Aug – Fri 29 Aug 2026 |
| Phase 5 — Cypress Regression Engineering | Week 5: Mon 1 Sep – Fri 5 Sep 2026 |
| Phase 6 — Playwright Cross-Browser Quality Engineering | Week 6: Mon 8 Sep – Fri 12 Sep 2026 |
| Phase 7 — CI/CD, Performance and Quality Signals | Week 7: Mon 15 Sep – Fri 19 Sep 2026 |
| Phase 8 — Release Readiness and Quality Leadership | Week 8: Mon 22 Sep – Fri 26 Sep 2026 |
| **Release Review Date (Go/No-Go)** | **Friday 26 September 2026** |

The Release Review Date is a fixed board commitment. It does not move.

---

## 7. The Project Team

### Daniel Brooks — Engineering Manager *(candidate's manager — purple)*

Wants faster automated feedback and fewer unreliable tests. Directly owns the candidate's
day-to-day priorities. Under pressure from the board to bring a defensible release decision to the
26 September review, not just a green dashboard. Skeptical of automation that "passes on retry."

### Mark Evans — QA Engineer, outgoing *(candidate's predecessor — teal)*

Built the original Cypress approach but never established consistent standards — flaky selectors,
shared test state, hardcoded waits. Leaving GenomeBridge partway through the programme. His
handover is incomplete by design: he documents stages 1–3 of the workflow and leaves explicit gaps
elsewhere. Candidates should treat his notes as a starting point, not a finished map.

### Aisha Rahman — Software Engineer *(operational/data stakeholder — amber)*

Supports API and browser workflow clarification. Delivers data files to the candidate during the
programme with a pattern buried in them that isn't called out explicitly — she expects the
candidate to find it, not be told it.

### Laura Okafor — Information Governance Lead *(compliance/risk stakeholder — coral)*

Challenges access control, synthetic-data handling, and auditability. Laura is the source of the
one hard regulatory constraint every candidate must satisfy by Phase 4: **synthetic data only,
correctly protected, with a documented handling policy** (see Section 9 below). She also frames
the clinical-safety context referenced in Phase 1 and revisited in Phase 8.

### Dr Maya Patel — Product Manager *(referenced, not a direct inbox contact)*

Owns Project Helix requirements and partner commitments. Sets the release-readiness bar jointly
with Daniel Brooks. Her requirements documents contain the gaps the candidate must surface in
Phase 1's requirement-gap analysis.

### Sofia Chen — Platform Engineer *(referenced, not a direct inbox contact)*

Reviews the candidate's GitHub Actions and environment configuration from Phase 7 onward. Her
standards for pipeline hygiene (secrets handling, artefact retention, no excessive traffic against
public systems) are the implicit bar for Phase 7 deliverables.

### James Wright — Service Support Lead *(referenced, not a direct inbox contact)*

Source of the original complaint themes in Section 3. His support-ticket framing is what Phase 2's
exploratory testing charters are designed to investigate and either confirm or correct.

---

## 8. Clinical Safety Context — Awareness Level Only

GenomeBridge's workflow is health IT, and UK health IT has two companion clinical safety
standards. The candidate is not expected to become a Clinical Safety Officer or produce a Clinical
Safety Case. The candidate is expected to understand, at awareness level, how their quality
evidence relates to this framework — because Laura Okafor will ask about it directly in Phase 8.

- **DCB0129** covers clinical safety activities carried out by *organisations that develop* health
  IT systems — this is GenomeBridge's obligation as the system builder.
- **DCB0160** covers clinical safety activities carried out by *healthcare organisations that
  deploy and use* health IT systems — this would sit with any NHS trust or lab partner adopting
  Project Helix.
- **Software quality evidence supports clinical safety assurance — it does not replace it.** A
  passing test suite is not a clinical safety case, and a QA Engineer does not independently
  approve clinical safety. The candidate's job is to produce evidence a Clinical Safety Officer
  could use — not to act as one.

This distinction is referenced in Phase 1 (system context and risk framing) and returns as a
direct stakeholder challenge from Laura Okafor in Phase 8.

---

## 9. Regulatory / Data-Handling Constraint

Laura Okafor's non-negotiable requirement, which must be visible in Phase 4's test-data policy and
referenced again at Phase 8:

- All test data must be public demonstration data (OpenMRS, HAPI FHIR public server) or
  synthetically generated (Synthea or candidate-generated synthetic records).
- No real patient information, under any circumstances, in any file, screenshot, log, or commit.
- Credentials and connection strings must never be committed to GitHub — environment variables
  only.
- Synthetic records must be clearly identifiable as synthetic (naming convention, tagging) so they
  can never be mistaken for real data downstream.

---

## 10. Internal Shorthand Glossary

GenomeBridge's operational queue report (used from Phase 3 onward) uses internal shorthand. These
terms are explained here so the candidate does not need to guess:

| Code | Meaning |
|---|---|
| **REF-INC** | Referral Incomplete — referral record missing one or more mandatory fields |
| **SPEC-UNLINK** | Specimen Unlinked — specimen record exists but is not associated with its service request |
| **CONS-MISS** | Consent Missing — no consent record found for a referral requiring one |
| **DUP-PAT** | Duplicate Patient Candidate — two or more patient records flagged as possible duplicates |
| **WF-STALL** | Workflow Stalled — no status update recorded against a Task for longer than the expected interval |
| **TAT** | Turnaround Time — elapsed time from referral creation to diagnostic report availability |
| **QGATE** | Quality Gate — an internal release checkpoint requiring evidence before progression |
| **TBC** | To Be Confirmed — used by the operations team when a weekly figure was not finalised at time of reporting |

These codes will appear directly in the Phase 3/4 operational data. Candidates who skip this
glossary will misread the queue report.

---

## 11. Open Questions Going Into Phase 1

These are deliberately unresolved. Part of Phase 1 is identifying which of these can actually be
answered using OpenMRS, HAPI FHIR, and the data GenomeBridge will provide — and which cannot.

- Is the specimen-linkage problem a UI/workflow issue, a data-entry issue, or something upstream
  that hasn't been named yet?
- How much of the support-ticket volume increase is a genuine reliability problem versus normal
  growth in referral volume?
- What can be tested directly against public demonstration systems, and what can only be assessed
  through inference, given that GenomeBridge has no private, GenomeBridge-hosted environment for
  this programme?
- Where does the previous Cypress suite's instability come from — the tests, or the public
  environment itself?

---

*This brief is the starting reference point for Phase 1. It does not contain the answer key. Some
figures here are deliberately reported-but-unverified, consistent with how a real Quality Engineer
joining mid-programme would receive this information.*
