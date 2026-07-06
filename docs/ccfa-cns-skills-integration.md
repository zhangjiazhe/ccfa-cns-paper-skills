# CCFA/CNS Paper Skills Integration Record

## Installed Local Skills

Installed under `/Users/zjz/.codex/skills/`:

| Skill | Purpose |
|---|---|
| `paper-router` | Main entry point for routing AI conference, CNS journal, and verification tasks |
| `ai-conference-track` | CCF-A / AI top-conference planning, drafting, compression, rebuttal, and camera-ready workflow |
| `cns-journal-track` | Nature / Science / Cell main-journal and subjournal manuscript workflow |
| `verification-track` | Two-pass claim, citation, figure, table, data, and source verification gate |
| `verified-source-corpus` | Verified literature/source corpus construction and bibliography boundary |
| `figure-evidence-planner` | Claim-to-figure, panel-role, legend, and Results alignment planning |

## Original Source Repositories

| Repository | GitHub Link | Role In Integration |
|---|---|---|
| Nature-Paper-Skills | https://github.com/Boom5426/Nature-Paper-Skills | Main source for CNS-style journal workflow, claim-evidence revision, figure planning, submission audit, data availability, rebuttal response |
| paper-writing-skill | https://github.com/SNL-UCSB/paper-writing-skill | Source for AI/CS conference workflow, structured brainstorming, introduction-twice, evaluation-first writing, compression, rebuttal habits |
| citation-check-skill | https://github.com/serenakeyitan/citation-check-skill | Source for two-pass claim extraction and verification, status taxonomy, numerical precision, doc-only verification |
| academic-research-skills | https://github.com/zhangjiazhe/academic-research-skills | Source for Verified Source Corpus boundary, academic search routing, manifest/run-state and integrity-gate concepts |

## Design Decision

The integration is modular rather than a single giant skill. This avoids trigger conflicts and keeps daily context small.

`paper-router` is the preferred user-facing entry point. It routes to:

- `ai-conference-track` for NeurIPS, ICML, ICLR, CVPR, ACL, KDD, AAAI, IJCAI, COLM, and similar CCF-A / AI conference workflows.
- `cns-journal-track` for Nature, Science, Cell, and their subjournals.
- `verification-track` for claim/citation/source/figure/table/data verification.
- `verified-source-corpus` before literature-heavy writing.
- `figure-evidence-planner` when figures or panels carry the argument.

## Recommended Use

For AI conference work:

```text
Use $paper-router to plan this ICLR submission.
```

Expected route:

```text
paper-router -> ai-conference-track -> verified-source-corpus -> figure-evidence-planner -> verification-track
```

For CNS journal work:

```text
Use $paper-router to decide whether this work fits Nature Methods, Nature Biotechnology, Science Advances, or Cell Systems.
```

Expected route:

```text
paper-router -> cns-journal-track -> verified-source-corpus -> figure-evidence-planner -> verification-track
```

For source checking:

```text
Use $verification-track to verify every factual claim in this draft against the supplied PDF and bibliography.
```

## Important Boundaries

- The original repositories were not blindly merged.
- `paper-writing-skill` was not installed as a competing broad trigger because its scope overlaps too much with the router.
- `academic-research-workflow` was not installed as the main orchestrator because it is heavier than needed for CCFA/CNS manuscript work.
- `Nature-Paper-Skills` remains useful as the CNS conceptual source, but the local `cns-journal-track` is the recommended entry for your mixed AI-conference and CNS-journal use case.
- Formal drafts should cite only sources in `verified-source-corpus` or user-provided materials that have been verified.

## Validation

Validation date: 2026-07-06.

- All six integrated skills passed the official `quick_validate.py` skill validator.
- A temporary local validation environment was used because the base Python environment did not include `PyYAML`.
- The installed skill files were checked for template residue such as `TODO`, `[TODO]`, `Replace with`, and `Structuring This Skill`.

## Restart

Restart Codex after installation so the new skills are picked up.
