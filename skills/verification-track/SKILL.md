---
name: verification-track
description: Verify manuscript claims, citations, figures, tables, data statements, and source support before conference or journal submission. Use for citation checking, hallucination detection, claim-to-source verification, doc-only verification, numerical consistency, final pre-submission gates, rebuttal evidence checks, or any task where unverified claims must be blocked.
---

# Verification Track

## Principle

No unsupported factual claim should enter a submission-ready paper, rebuttal, cover letter, slide deck, or response document.

## Two-Pass Protocol

Always separate extraction from verification.

Pass 1: extract claims only.
- List every factual, numerical, comparative, causal, ranking, source-attributed, or time-bound claim.
- Include location: section, paragraph, figure, table, slide, or line when available.
- Do not verify during this pass.

Pass 2: verify fixed claims.
- Work only from the Pass 1 claim list.
- For each claim, identify the supporting source, figure, table, data artifact, or result.
- Assign one status:
  - `verified`
  - `numerical_error`
  - `unverified`
  - `hallucination`
  - `misleading`
  - `not_in_source`
  - `needs_author_input`

## Verification Sources

Prefer:
1. user-provided source documents and project data
2. `verified-source-corpus`
3. official DOI/publisher/PubMed/CrossRef/arXiv/Semantic Scholar records
4. official dataset, code, protocol, and registry pages

For current policies, deadlines, journal instructions, or changing rules, verify live with official sources.

## Blocking Rules

Block finalization when:
- any citation is fabricated or cannot be found
- a cited source does not support the claim
- numerical values differ without explicit approximation support
- a figure/table value conflicts with text or legend
- Data Availability, code availability, ethics, or AI disclosure contains placeholders
- a central claim is only partially supported but stated as established fact

Do not block for stylistic preferences. Record those separately.

## Output

Return:
- summary counts by status
- high-risk findings first
- claim ID, claim text, location, source/evidence, status, and minimum safe fix
- remaining author-input questions
- final readiness label: `ready`, `fix_before_submission`, `needs_author_input`, or `blocked`

Use `references/claim-status-taxonomy.md` for detailed status definitions.
