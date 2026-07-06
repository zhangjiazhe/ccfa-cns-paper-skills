# CCFA/CNS 论文写作 Skills 整合记录

## 已安装的本地 Skills

以下 skills 已安装在 `/Users/zjz/.codex/skills/`：

| Skill | 作用 |
|---|---|
| `paper-router` | 论文任务总入口，用于在 AI 顶会、CNS 期刊、文献核验和图表规划之间路由 |
| `ai-conference-track` | 面向 CCF-A / AI 顶会的选题定位、写作规划、压缩、rebuttal 和 camera-ready 工作流 |
| `cns-journal-track` | 面向 Nature / Science / Cell 正刊及子刊的选刊、论证、图表和投稿前检查工作流 |
| `verification-track` | 对 claim、citation、figure、table、data 和 source 做两轮核验 |
| `verified-source-corpus` | 建立可核验的文献与资料语料库，限定正式写作中可引用的来源边界 |
| `figure-evidence-planner` | 将中心 claim 映射到 figure、panel role、legend 和 Results 叙事结构 |

## 原始来源仓库

| 仓库 | GitHub 链接 | 在本次整合中的角色 |
|---|---|---|
| Nature-Paper-Skills | https://github.com/Boom5426/Nature-Paper-Skills | CNS 期刊写作主线来源，包括 claim-evidence 修订、figure planning、submission audit、data availability、rebuttal response |
| paper-writing-skill | https://github.com/SNL-UCSB/paper-writing-skill | AI/CS 顶会写作来源，包括 brainstorming、introduction-twice、evaluation-first writing、compression、rebuttal habits |
| citation-check-skill | https://github.com/serenakeyitan/citation-check-skill | 事实与引用核验来源，包括两轮 claim extraction、状态分类、数值精度和基于文档的 verification |
| academic-research-skills | https://github.com/zhangjiazhe/academic-research-skills | Verified Source Corpus、academic search routing、manifest/run-state 和 integrity gate 等概念来源 |

## 整合决策

这次没有把几个原始仓库直接合并成一个巨大的 skill，而是采用模块化设计：

- `paper-router` 作为主入口，负责判断当前任务应该调用哪条写作或核验路线。
- `ai-conference-track` 专门服务 NeurIPS、ICML、ICLR、CVPR、ACL、KDD、AAAI、IJCAI、COLM 等 AI 顶会。
- `cns-journal-track` 专门服务 Nature、Science、Cell 以及 Nature Portfolio、Science 系列、Cell Press 子刊。
- `verification-track` 独立承担投稿前的事实、引用、图表、数据与来源核验。
- `verified-source-corpus` 先建立可靠来源边界，避免正式论文里混入未核验文献。
- `figure-evidence-planner` 负责把论文主张转化为 figure/panel 证据链，适合 AI 顶会和 CNS 期刊共同使用。

这样做的好处是：

- 避免多个大 skill 互相抢触发。
- 日常写作时上下文更小、更稳定。
- AI 顶会与 CNS 期刊的写作逻辑可以分开优化。
- 核验能力作为独立 gate，可以在任何投稿路径里复用。

## 推荐使用方式

AI 顶会论文：

```text
Use $paper-router to plan this ICLR submission.
```

预期路线：

```text
paper-router -> ai-conference-track -> verified-source-corpus -> figure-evidence-planner -> verification-track
```

CNS 正刊或子刊论文：

```text
Use $paper-router to decide whether this work fits Nature Methods, Nature Biotechnology, Science Advances, or Cell Systems.
```

预期路线：

```text
paper-router -> cns-journal-track -> verified-source-corpus -> figure-evidence-planner -> verification-track
```

只做事实与引用核验：

```text
Use $verification-track to verify every factual claim in this draft against the supplied PDF and bibliography.
```

## 重要边界

- 原始仓库没有被盲目整合。
- `paper-writing-skill` 没有作为独立大入口安装，因为它与 `paper-router` 的触发范围重叠较大。
- `academic-research-skills` 没有作为主 orchestrator 使用，因为它对当前 CCFA/CNS 写作场景来说偏重。
- `Nature-Paper-Skills` 仍然是 CNS 写作思路的重要来源，但本地推荐入口是 `cns-journal-track`。
- 正式论文中的引用和事实陈述，应该只来自 `verified-source-corpus` 或用户提供且已核验的材料。

## 校验记录

校验日期：2026-07-06。

- 6 个整合后的 skills 均通过官方 `quick_validate.py` 校验。
- 因基础 Python 环境缺少 `PyYAML`，校验时使用了临时本地 validation environment。
- 已检查 skill 文件中没有模板残留，例如 `TODO`、`[TODO]`、`Replace with`、`Structuring This Skill`。

## 许可与归因

- 本仓库使用 MIT License 发布。
- 上游来源、第三方许可说明和归因信息记录在 `NOTICE.md`。
- Nature、Science、Cell 以及各会议/出版方名称仅用于描述投稿场景和写作流程；本仓库不代表这些期刊、会议、出版方或组织，也未获得其背书或赞助。

## 重启说明

安装或更新 skills 后，需要重启 Codex，新的 skills 才会被当前会话识别。
