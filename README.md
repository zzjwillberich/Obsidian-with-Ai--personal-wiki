# Obsidian with AI - Personal Wiki Framework

> 中文：这是一个可复用的 Obsidian + AI 个人知识库框架包。它只包含提示词、skills、模板、Schema、Obsidian 配置和空目录架构。
>
> English: This is a reusable Obsidian + AI personal wiki framework package. It includes prompts, skills, templates, schemas, Obsidian configuration, and an empty vault structure. 
## What This Is / 这是什么

中文：这个仓库把一个「LLM Wiki 模式」知识库的运行规则抽离出来，让你可以快速搭建一个由 AI 协助维护的 Obsidian Vault。AI 的职责不是一次性回答问题，而是像程序员维护代码库一样，持续增量维护你的知识库。

English: This repository extracts the operating rules of an "LLM Wiki" knowledge base so you can quickly set up an AI-assisted Obsidian vault. The AI is not meant to answer once and disappear; it maintains the wiki incrementally, like an engineer maintaining a codebase.

## Core Idea / 核心理念

中文：Obsidian 是 IDE，AI 是程序员，Wiki 是代码库。

English: Obsidian is the IDE, AI is the programmer, and the wiki is the codebase.

## Included / 包含内容

| Path / 路径 | 中文说明 | English Description |
|---|---|---|
| `AGENTS.md` | Agent 总入口规则，定义身份、模式、行为规范和 daily 自动日志机制。 | Main agent instruction file. Defines identity, modes, behavior rules, and automatic daily logging. |
| `CLAUDE.md` | Claude/Claudian 环境可读的同等规则文件。 | Equivalent instruction file for Claude/Claudian-style environments. |
| `system/llm-wiki.yaml` | LLM Wiki 的页面 Schema、字段规范、类型规范和标签约定。 | Page schema, field rules, type rules, and tag conventions for the LLM Wiki. |
| `system/prompts/` | 核心工作流提示词：摄入、查询、检查、链接和颜色规范。 | Core workflow prompts: ingest, query, lint, link rules, and color rules. |
| `system/skills/` | 知识库专用 skill，例如逐步教学 tutor。 | Knowledge-base-specific skills, such as step-by-step tutoring. |
| `system/templates/` | 概念页和主题页模板，用于保持页面结构一致。 | Templates for concept and topic pages to keep page structure consistent. |
| `.codex/skills/` | Codex 本地 skills，用于规划、调试、验证、写 skill、并行 agent 等工作流。 | Local Codex skills for planning, debugging, verification, skill writing, parallel agents, and related workflows. |
| `.obsidian/` | Obsidian 基础配置、图谱颜色配置、插件列表和 CSS 片段。 | Obsidian base configuration, graph color groups, plugin lists, and CSS snippets. |
| `wiki/` | 空的知识库目录骨架，后续知识笔记会放在这里。 | Empty wiki directory skeleton where future notes will live. |
| `raw/` | 空的原始资料目录，后续 ingest 的资料会放在这里。 | Empty source-material directory for future ingest inputs. |
| `USAGE.md` | 使用说明：如何安装、复制、启动、维护。 | Usage guide: installation, copying, startup, and maintenance. |

## Not Included / 不包含内容

中文：本仓库不包含原 Vault 的具体知识笔记、daily 日志、raw 原始资料、Git 历史、构建产物、会话记录、主题源码或插件源码。

English: This repository does not include the original vault's knowledge notes, daily logs, raw source materials, Git history, build artifacts, session records, theme source files, or plugin source files.

## Recommended Workflow / 推荐工作流

| Mode / 模式 | Trigger / 触发方式 | What It Does / 作用 |
|---|---|---|
| Ingest / 摄入 | Say `ingest`, `摄入`, `学习`, or place files in `raw/`. | Reads source material, extracts concepts, creates or updates wiki pages, and links them. |
| Query / 查询 | Ask a question about the knowledge base. | Searches the wiki, synthesizes an answer, and marks knowledge gaps. |
| Lint / 检查 | Say `lint`, `检查`, or `诊断`. | Scans the vault for broken links, schema issues, weak structure, and stale pages. |
| Tutor / 教学 | Say `/tutor`, `逐步教学`, `step by step`, etc. | Teaches step by step with no skipped reasoning. |
| Daily Log / 日志 | Automatic after meaningful knowledge work. | Appends a short record under `wiki/daily/`. |

## Quick Start / 快速开始

中文：把这个仓库复制成一个新的 Obsidian Vault，打开后把你的资料放进 `raw/`，然后对 AI 说：`请 ingest raw/文件名`。

English: Copy this repository as a new Obsidian vault, open it in Obsidian, place source materials into `raw/`, then tell the AI: `Please ingest raw/filename`.

More details are in [`USAGE.md`](USAGE.md).

## Design Principles / 设计原则

- 中文：强相关才链接，不为了图谱好看乱链。
- English: Link only strongly related pages; do not over-link for graph aesthetics.
- 中文：概念页保持原子性，一个页面只讲一件事。
- English: Keep concept pages atomic; one page should explain one idea.
- 中文：所有知识都应可追溯到 raw 来源。
- English: Knowledge should be traceable to raw source material.
- 中文：不确定就标注，不编造。
- English: Mark uncertainty clearly; do not invent facts.
- 中文：保留矛盾，用争议块记录冲突观点。
- English: Preserve contradictions and record conflicting views in warning blocks.
- 中文：渐进式维护，允许 draft 页面逐步完善。
- English: Maintain incrementally; draft pages are expected to evolve.

## License / 许可

中文：如果你要公开复用，建议根据自己的需要补充许可证文件。

English: If you plan to reuse this publicly, add a license file that matches your needs.
