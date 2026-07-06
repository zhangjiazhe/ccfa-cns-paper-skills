---
name: cns-journal-track
description: Plan, evaluate fit, revise, audit, and respond for Nature, Science, Cell, and CNS-family main-journal or subjournal manuscripts. Use for Nature/Science/Cell main titles and subjournals when the task involves venue fit, article type, claim-evidence structure, figure-led Results, Data Availability, code/material availability, editorial preflight, submission audit, or reviewer response.
---

# CNS Journal Track

## Operating Principle

Build the manuscript around a broad, evidence-bounded story. Venue fit and article type are structural decisions, not late-stage styling.

## Venue Family Routing

Use `references/cns-venue-routing.md` when choosing among:
- Nature main journal and Nature Portfolio subjournals
- Science main journal and Science family journals
- Cell main journal and Cell Press journals

Default distinction:
- Main Nature/Science/Cell requires broad conceptual significance beyond a narrow specialty.
- Methods/resource subjournals require enabling power, validation, reproducibility, reuse, and a clear user community.
- Specialized subjournals tolerate more field density but still require strong claim-evidence alignment.

## Workflow

1. Choose venue family and article type.
   - Article, Resource, Analysis, Method, Brief Communication, Report, or field-specific type.
2. Build a claim-evidence map.
   - Every abstract/introduction/discussion claim must map to a result, figure, table, supplement, or source.
3. Plan figures before polishing prose.
   - Use `figure-evidence-planner` for one-claim-per-figure and panel-role mapping.
4. Rewrite Results around claims, not panel chronology.
5. Prepare data, code, materials, methods, ethics, AI-use, image-integrity, and reporting disclosures early.
6. Run `verification-track` and journal preflight before submission.
7. For reviewer comments, revise the manuscript before finalizing the response letter.

## Required Checks

Before calling a CNS-family manuscript submission-ready:
- venue promise matches evidence package
- article type is explicit
- title, abstract, introduction, figures, and discussion tell the same story
- main figures carry the paper's central claims
- source data, raw data, code, materials, protocol, accession IDs, and repository plans are explicit
- no claim is stronger than its evidence
- official journal guidance has been checked for current policy-sensitive requirements

## Integration

Use:
- `verified-source-corpus` for literature base and reference verification
- `figure-evidence-planner` for figure and panel design
- `verification-track` for claim, citation, figure, table, and data checking

Distilled from `Nature-Paper-Skills`, extended to cover Science and Cell family routing. See `references/cns-venue-routing.md` and `paper-router/references/source-repositories.md`.
