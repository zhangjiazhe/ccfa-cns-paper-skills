---
name: ai-conference-track
description: Plan, draft, revise, compress, rebut, and camera-ready AI top-conference papers. Use for CCF-A or AI conference targets such as NeurIPS, ICML, ICLR, CVPR, ICCV, ECCV, ACL, EMNLP, KDD, WWW, SIGIR, AAAI, IJCAI, COLM, and related conference-first manuscripts with method, benchmark, dataset, model, theory, or experiment-heavy contributions.
---

# AI Conference Track

## Operating Principle

Build a conference paper around a defensible contribution and an evaluation that proves exactly that contribution. Do not polish prose before the method/evidence/story triangle is stable.

## Workflow

1. Frame the paper.
   - Name the problem, failure mode in existing work, core contribution, and target venue.
   - If the idea is vague, use `references/brainstorming-and-introduction-twice.md`.
2. Write a disposable Draft 0 introduction.
   - Use it to constrain experiments and evaluation, not as final prose.
3. Lock the evaluation contract.
   - Datasets, baselines, metrics, ablations, robustness tests, and limitations must map to claims.
4. Draft in evidence-first order.
   - Method/design and experiments before final introduction and abstract.
   - Final introduction must be rewritten after evaluation is stable.
5. Compress for page limits.
   - Use `references/conference-compression.md` before final submission.
6. Verify.
   - Run `verification-track` before submission and after major revisions.
7. Prepare rebuttal and camera-ready.
   - Keep response actions tied to concrete manuscript changes.

## Section Defaults

For AI top conferences, prefer this sequence unless the venue template demands otherwise:

1. Abstract
2. Introduction with claim-first contribution summary
3. Related work or positioning
4. Method / framework / theory
5. Experiments
6. Ablations and analysis
7. Limitations, ethics, broader impact, or reproducibility statements as required

## Evaluation Checklist

Before writing final intro claims, confirm:
- each headline claim has one primary figure/table
- baselines are credible and not straw targets
- ablations isolate the contribution rather than merely decorating it
- implementation details, compute, seeds, hyperparameters, and data splits are reproducible enough for the venue
- limitations are honest and do not sabotage the contribution

## Rebuttal Defaults

For reviewer comments:
- classify each comment as misunderstanding, evidence gap, methodological concern, novelty concern, clarity issue, or scope mismatch
- answer with the action first
- cite exact changed sections, equations, figures, or appendix locations
- respectfully push back only when the premise is false or the request is outside the paper scope

## Integration

Use:
- `verified-source-corpus` before literature-heavy writing
- `figure-evidence-planner` when figures or tables carry the argument
- `verification-track` before submission, rebuttal, and camera-ready

Detailed patterns live in:
- `references/brainstorming-and-introduction-twice.md`
- `references/conference-compression.md`
