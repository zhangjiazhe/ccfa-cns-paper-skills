# Verified Source Corpus Schema

Use a table or structured YAML with these fields.

| Field | Required | Notes |
|---|---|---|
| `source_id` | yes | Stable local ID, e.g. `S001` |
| `citation_key` | no | BibTeX key when available |
| `title` | yes | Exact verified title |
| `authors` | yes | First author + et al. acceptable in compact table |
| `year` | yes | Publication/preprint year |
| `venue_or_repository` | yes | Journal, conference, preprint server, dataset repo, code repo |
| `stable_identifier` | yes | DOI, PMID, PMCID, arXiv, accession, or repository URL |
| `source_type` | yes | paper, preprint, dataset, code, protocol, registry, guideline |
| `verification_route` | yes | PubMed, CrossRef, arXiv, publisher page, DOI resolver, official repo |
| `verified_on` | yes | Date checked |
| `supports_claims` | yes | Claims this source can support |
| `limitations` | no | Caveats, version issues, preprint status, access limits |
| `status` | yes | verified_primary, verified_secondary, verified_preprint, verified_dataset_or_code, candidate_unverified, excluded |

Do not export entries with `candidate_unverified` or `excluded` into final bibliography files.
