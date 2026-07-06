# Claim Status Taxonomy

Use these labels consistently in verification reports.

| Status | Meaning | Action |
|---|---|---|
| `verified` | Source, data, figure, or table directly supports the claim | Keep, cite exact support |
| `numerical_error` | Number, unit, direction, denominator, or rounding differs from support | Correct value or rewrite |
| `unverified` | No adequate authoritative support found | Remove, source, or mark as author input |
| `hallucination` | Claim contradicts available source or cites fabricated/nonexistent support | Remove or replace |
| `misleading` | Claim is technically sourced but omits important context or cherry-picks | Qualify or add context |
| `not_in_source` | In doc-only mode, the claim is absent from supplied materials | Remove or request source |
| `needs_author_input` | Verification depends on private data, unpublished experiment, or author decision | Ask targeted question |

Central claims marked anything except `verified` block final submission unless explicitly downgraded or removed.
