---
name: figure-evidence-planner
description: Map manuscript claims to figures, tables, panels, legends, and supporting evidence for AI conference and CNS journal papers. Use when designing main figures, deciding main versus supplement, auditing figure-panel roles, aligning Results text with legends, checking table/figure numerical consistency, or planning figure-led manuscript revisions.
---

# Figure Evidence Planner

## Principle

Each main figure should earn its place by carrying a clear claim. Panels exist to support the claim, define the method, validate robustness, show a failure mode, or move secondary evidence to the supplement.

## Planning Workflow

1. Write the manuscript claim in one sentence.
2. Choose the figure or table that carries that claim.
3. Assign each panel one primary role:
   - core evidence
   - method bridge
   - benchmark comparison
   - ablation
   - robustness/generalization
   - resource overview
   - case illustration
   - failure mode or limitation
4. Decide main versus supplement.
5. Align Results paragraph, legend, axis labels, metrics, datasets, and statistics.
6. Flag any text claim that the figure does not directly support.

## Conference Defaults

For AI conference papers:
- keep figures compact and page-budget aware
- prioritize method overview, main result, ablations, and analysis
- move dense robustness and extra baselines to appendix
- ensure every headline plot has enough setup for reproducibility

## CNS Journal Defaults

For Nature/Science/Cell-family manuscripts:
- organize Results around figure claims, not analysis chronology
- legends should preserve panel roles and essential quantitative anchors
- source data and raw data readiness matter
- main figures should collectively carry the paper's full story arc

## Output

Return:
- claim-to-figure map
- panel role table
- main versus supplement decision
- legend and Results alignment notes
- numerical or labeling mismatches
- minimum safe fixes before submission

Use `verification-track` after figure text stabilizes.
