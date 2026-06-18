# Usage Guide / 使用说明

## 1. Create a New Vault / 创建新知识库

中文：推荐把这个仓库复制到一个新的文件夹，然后用 Obsidian 打开这个文件夹作为 Vault。

English: Copy this repository into a new folder, then open that folder as an Obsidian vault.

```powershell
git clone git@github.com:zzjwillberich/Obsidian-with-Ai--personal-wiki.git My-AI-Wiki
```

## 2. Folder Guide / 文件夹说明

| Folder / 文件夹 | 中文说明 | English Description |
|---|---|---|
| `raw/` | 原始资料入口。文章、代码片段、PDF 摘录、灵感草稿都可以先放这里。AI 摄入时应引用这里作为来源。 | Source-material inbox. Articles, code snippets, PDF excerpts, and drafts can be placed here first. AI should cite this folder as source material during ingest. |
| `wiki/` | 知识库主体目录。这里保存被整理后的概念页、主题页、课程页、创作页和日常日志。 | Main knowledge-base directory. Stores organized concept pages, topic pages, lessons, creator notes, and daily logs. |
| `wiki/concepts/` | 原子概念页。一个页面只解释一个概念。 | Atomic concept pages. Each page explains one concept. |
| `wiki/topics/` | 主题整合页。用于把多个概念组织成体系、路线或专题。 | Topic synthesis pages. Used to organize multiple concepts into systems, roadmaps, or themes. |
| `wiki/lessons/` | 教学路径和课程拆解。适合 tutor 模式生成的分步学习材料。 | Learning paths and lesson breakdowns. Good for step-by-step tutoring material. |
| `wiki/creator/` | 创作、选题、内容系统和素材管理。 | Creator workflow, content ideas, content systems, and material management. |
| `wiki/daily/` | 自动 daily 学习记录。每次重要知识操作结束后追加记录。 | Automatic daily learning logs. Appended after meaningful knowledge work. |
| `system/` | 知识库运行系统。包含 schema、prompt、skill 和模板。 | Operating system for the wiki. Contains schemas, prompts, skills, and templates. |
| `system/prompts/` | Ingest、Query、Lint、链接颜色规范等核心提示词。 | Core prompts for ingest, query, lint, and link/color rules. |
| `system/skills/` | 知识库专用技能，例如 tutor。 | Wiki-specific skills, such as tutor. |
| `system/templates/` | 新建页面时使用的模板。 | Templates used when creating new pages. |
| `system/lint-reports/` | Lint 报告输出目录，默认留空。 | Output folder for lint reports, empty by default. |
| `.codex/skills/` | Codex 工作流技能，用于开发式协作、调试、计划、验证等。 | Codex workflow skills for development-style collaboration, debugging, planning, and verification. |
| `.obsidian/` | Obsidian 配置文件。包含图谱、外观、插件和 CSS 片段。 | Obsidian configuration files, including graph, appearance, plugins, and CSS snippets. |
| `.claude/` | Claude/Claudian 相关目录骨架，默认只保留结构。 | Claude/Claudian-related skeleton folders, kept as structure only by default. |

## 3. Important Files / 重要文件

| File / 文件 | 中文说明 | English Description |
|---|---|---|
| `AGENTS.md` | AI 助手的主规则。新环境最应该先读这个。 | Main rule file for AI assistants. This is the first file to read in a new environment. |
| `CLAUDE.md` | Claude 环境入口规则，内容与 AGENTS 规则保持一致。 | Claude entry instruction file, aligned with AGENTS rules. |
| `system/llm-wiki.yaml` | 页面类型、字段、标签和结构约定。 | Page types, fields, tags, and structure conventions. |
| `system/prompts/ingest.md` | 摄入 raw 资料并转化为 Wiki 页面的流程。 | Workflow for ingesting raw material into wiki pages. |
| `system/prompts/query.md` | 查询知识库并综合回答的流程。 | Workflow for querying the wiki and synthesizing answers. |
| `system/prompts/lint.md` | 扫描知识库健康状况的流程。 | Workflow for scanning wiki health. |
| `system/prompts/link-and-color.md` | 强相关链接、标签和颜色分组规范。 | Rules for strong links, tags, and color groups. |
| `system/skills/tutor.md` | 逐步教学模式说明。 | Step-by-step tutor mode instructions. |
| `system/templates/concept-template.md` | 概念页模板。 | Concept page template. |
| `system/templates/topic-template.md` | 主题页模板。 | Topic page template. |

## 4. How to Use with AI / 如何配合 AI 使用

中文：让 AI 每次开始时先读 `wiki/index.md` 和 `AGENTS.md`。如果是新库，先让 AI 创建或更新 `wiki/index.md`，再开始摄入资料。

English: Ask the AI to read `wiki/index.md` and `AGENTS.md` at the start of each session. For a new vault, ask it to create or update `wiki/index.md` before ingesting material.

Useful commands / 常用指令：

```text
请 ingest raw/example.md
关于某个概念，我现在知道什么？
请 lint 知识库
/tutor 带我一步一步学这个主题
帮我把这个灵感整理进 creator
```

## 5. First Setup Checklist / 首次设置清单

- 中文：用 Obsidian 打开仓库根目录。
- English: Open the repository root as an Obsidian vault.
- 中文：确认 `.obsidian/snippets/folder-colors.css` 已启用。
- English: Confirm `.obsidian/snippets/folder-colors.css` is enabled.
- 中文：把需要摄入的资料放到 `raw/`。
- English: Put source materials into `raw/`.
- 中文：让 AI 根据 `system/templates/` 创建页面。
- English: Ask the AI to create pages using `system/templates/`.
- 中文：定期运行 lint，检查断链、重复页和标签漂移。
- English: Run lint regularly to find broken links, duplicate pages, and tag drift.

## 6. Maintenance Rules / 维护规则

中文：

1. 创建页面前先搜索，避免重复。
2. 优先更新已有页面，而不是重写。
3. 只建立强相关链接。
4. 新知识必须可追溯到 `raw/` 来源。
5. 不确定的信息要明确标注。
6. 今日有知识工作时，最后更新 `wiki/daily/YYYY-MM-DD.md`。

English:

1. Search before creating pages to avoid duplicates.
2. Prefer updating existing pages over rewriting them.
3. Create only strong, meaningful links.
4. New knowledge should trace back to `raw/` sources.
5. Mark uncertain information clearly.
6. When knowledge work happens, update `wiki/daily/YYYY-MM-DD.md` at the end.

## 7. What to Add Later / 后续可以添加什么

中文：这个包默认不带知识内容。你可以后续添加：

English: This package intentionally ships without knowledge content. You can later add:

- `wiki/index.md` as the vault homepage / 作为知识库首页
- Your own concept pages / 你自己的概念页
- Your own topic maps / 你自己的主题地图
- Real raw source files / 真实 raw 原始资料
- Lint reports / Lint 检查报告
- Additional Obsidian themes or plugins / 额外 Obsidian 主题或插件
