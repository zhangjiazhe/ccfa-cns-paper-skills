---
name: paper-router
description: Route academic manuscript work for CCF-A/AI top conferences and CNS-family journals. Use when the user asks where a project should go, whether to target an AI conference or Nature/Science/Cell journal, how to sequence writing/revision/verification, or asks for a unified paper workflow across NeurIPS/ICML/ICLR/CVPR/ACL/KDD/AAAI/IJCAI and Nature/Science/Cell main journals or subjournals.
---

# Paper Router

## Role

Use this skill as the first stop for high-stakes paper work. It does not write the manuscript. It chooses the correct track, names required gates, and hands off to the specialized skills.

## Route Decision

Route to `ai-conference-track` when the target is CCF-A or AI-conference-first work:
- NeurIPS, ICML, ICLR, CVPR, ICCV, ECCV
- ACL, EMNLP, NAACL, COLING
- KDD, WWW, SIGIR, WSDM
- AAAI, IJCAI, COLM or similar conference tracks

Route to `cns-journal-track` when the target is broad journal-first work:
- Nature, Science, Cell
- Nature Methods, Nature Biotechnology, Nature Machine Intelligence, Nature Medicine, Nature Communications, Communications Biology
- Science Advances, Science Robotics, Science Translational Medicine
- Cell Systems, Cell Reports, Cell Genomics, Molecular Cell, Neuron or related Cell-family journals

Route to `verification-track` when the main request is:
- citation or source verification
- claim-to-source checking
- figure/table/data consistency
- final pre-submission evidence audit

Route to `verified-source-corpus` before writing literature-heavy sections when the source base is not yet verified.

Route to `figure-evidence-planner` when the bottleneck is figure logic, panel roles, or claim-to-figure mapping.

## Ambiguous Venue Protocol

When venue is uncertain, decide from evidence package rather than style preference:

1. Identify contribution type: method, model, benchmark, resource, biological finding, tool, theory, dataset, translational result, or mixed.
2. Ask whether the central claim is best judged by expert reviewers in a compact conference paper or by broad editors/readers in a full journal story.
3. Check whether the paper needs extended biological validation, data/resource availability, or source-data packaging. If yes, journal track becomes more likely.
4. Check whether the novelty is mainly algorithmic, benchmark-driven, or ablation-heavy under page limits. If yes, conference track becomes more likely.
5. If both are plausible, produce a two-path plan: conference-first and journal-first, with evidence gaps for each.

## Required Gates

Before drafting formal text, ensure:
- target family is chosen or explicitly left as dual-track
- core claim and contribution type are named
- evidence map exists or is planned
- unverified citations are kept out of final prose

Before submission, require:
- `verification-track`
- `figure-evidence-planner` for figure-heavy papers
- `cns-journal-track` submission audit for CNS-family journals
- conference compression and rebuttal readiness for AI conferences

## Source Notes

This integrated router distills patterns from:
- `Nature-Paper-Skills` for CNS-style journal writing
- `paper-writing-skill` for AI/CS conference writing workflow
- `citation-check-skill` for two-pass claim verification
- `academic-research-skills` for verified-source-corpus and workflow-state ideas

See `references/source-repositories.md` for original GitHub links.
