# CCFA/CNS Paper Skills

Integrated Codex skills for writing CCF-A / AI top-conference papers and Nature / Science / Cell family manuscripts.

## Included Skills

| Skill | Purpose |
|---|---|
| `paper-router` | Main entry point for routing manuscript tasks |
| `ai-conference-track` | CCF-A / AI top-conference writing workflow |
| `cns-journal-track` | Nature / Science / Cell journal workflow |
| `verification-track` | Claim, citation, figure, table, data, and source verification |
| `verified-source-corpus` | Verified literature/source corpus boundary |
| `figure-evidence-planner` | Claim-to-figure and panel-evidence planning |

## Installation

Copy the skill folders into your Codex skills directory:

```bash
cp -R skills/* ~/.codex/skills/
```

Then restart Codex.

## Recommended Entry Point

Use `paper-router` first for most manuscript work:

```text
Use $paper-router to plan this ICLR submission.
```

```text
Use $paper-router to decide whether this work fits Nature Methods, Nature Biotechnology, Science Advances, or Cell Systems.
```

Use `verification-track` directly when the task is only source or claim verification:

```text
Use $verification-track to verify every factual claim in this draft against the supplied PDF and bibliography.
```

## Documentation

- English integration record: [`docs/ccfa-cns-skills-integration.md`](docs/ccfa-cns-skills-integration.md)
- Chinese integration record: [`docs/ccfa-cns-skills-integration.zh-CN.md`](docs/ccfa-cns-skills-integration.zh-CN.md)

## Source Repositories

This integration draws design ideas from:

- https://github.com/Boom5426/Nature-Paper-Skills
- https://github.com/SNL-UCSB/paper-writing-skill
- https://github.com/serenakeyitan/citation-check-skill
- https://github.com/zhangjiazhe/academic-research-skills

## License And Attribution

This repository is released under the MIT License. See [`LICENSE`](LICENSE).

Upstream attribution, third-party license notes, and trademark/affiliation disclaimers are recorded in [`NOTICE.md`](NOTICE.md).

This repository is an integration and rewrite for a CCFA/CNS workflow. It is not a verbatim mirror of the upstream repositories.
