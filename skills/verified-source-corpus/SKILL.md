---
name: verified-source-corpus
description: Build and maintain a verified literature/source corpus for AI conference and CNS journal manuscripts. Use before drafting literature-heavy sections, adding citations, repairing references, building a bibliography, checking DOI/PMID/arXiv validity, deciding whether sources are verified enough to cite, or separating verified sources from unverified candidates.
---

# Verified Source Corpus

## Rule

Formal manuscript text may cite only verified sources. Candidate sources can guide exploration but must not enter the paper body, in-text citations, `.bib`, final reference list, or rebuttal claims until verified.

## Corpus Workflow

1. Collect candidate sources from user materials, search results, existing `.bib`, PDFs, notes, and prior drafts.
2. Deduplicate by DOI, PMID, arXiv ID, title, and first-author/year.
3. Verify existence and metadata.
   - DOI or publisher page for published work
   - PubMed/PMID/PMCID for biomedical work
   - arXiv for preprints
   - CrossRef/Semantic Scholar as cross-checks
4. Classify each source:
   - `verified_primary`
   - `verified_secondary`
   - `verified_preprint`
   - `verified_dataset_or_code`
   - `candidate_unverified`
   - `excluded`
5. Record what each source can safely support.
6. Export or update bibliography only from verified entries.

## Preferred Search Backends

Use available tools in this order:
- PubMed for biomedical and clinical papers
- CrossRef for DOI and publisher metadata
- arXiv for AI/CS/math/physics preprints
- Semantic Scholar for citation graph and related work
- official dataset/code/protocol repositories for non-paper sources

If a dedicated academic search MCP is installed, use it. Otherwise use web search with primary sources.

## Corpus Record

For each source, capture:
- stable ID: DOI, PMID, PMCID, arXiv ID, accession, repository URL
- title, authors, year, venue
- source type
- verification route and date
- claims it supports
- limitations or context caveats
- citation key if exported

## Handoff

Pass the corpus to:
- `ai-conference-track` for related work and positioning
- `cns-journal-track` for introduction, discussion, and policy-sensitive statements
- `verification-track` for final claim checks

See `references/corpus-schema.md` for a compact table schema.
