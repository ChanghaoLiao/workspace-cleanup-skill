# workspace-cleanup / 工作区清理规则

## 简介 / Overview

`workspace-cleanup` 是一个可复用的 Codex skill，用来让 Codex 在完成任务后主动整理工作区：保留有价值的材料，清理明确无用的临时文件，让项目目录长期保持干净。

`workspace-cleanup` is a reusable Codex skill that helps Codex tidy up a project workspace after meaningful tasks: keep useful materials, remove clearly unnecessary temporary files, and maintain a cleaner project folder over time.

## 它能做什么 / What It Does

这个 skill 会提醒 Codex 在每次完成任务后检查本次产生的文件，并按照“保守、安全、可追溯”的标准决定哪些应该保留，哪些可以清理。

This skill tells Codex to review files created or modified during a task and decide what to keep or clean up using a conservative, safe, and traceable standard.

- 检查任务过程中创建或修改的文件
- Review files created or modified during the task
- 保留源材料、最终成果、有效笔记和可复用资产
- Keep source materials, final outputs, active notes, and reusable artifacts
- 删除明确不再需要的派生文件或临时文件
- Delete derived or temporary files that are clearly no longer needed
- 减少项目里的杂乱文件，让工作区更容易维护
- Reduce workspace clutter and make the project easier to maintain

## 它会保留什么 / What It Keeps

它默认优先保留可能还有价值的文件，而不是激进删除。

By default, it prefers keeping files that may still be valuable instead of deleting aggressively.

- 用户提供的原始材料
- User-provided source materials
- 最终交付物
- Final deliverables
- 仍然指导项目的工作笔记
- Working notes that still guide the project
- 可复用的提取、整理或翻译材料
- Reusable extracted, organized, or translated materials
- 支持追溯、引用或后续编辑的文件
- Files needed for traceability, citation, or later editing

## 它会清理什么 / What It Cleans

它只清理“明确是临时的、重复的、已经被替代的、未来基本不会再用”的文件。

It only cleans files that are clearly temporary, duplicated, superseded, or very unlikely to be reused.

- 临时草稿文件
- Temporary scratch files
- 已经被更好版本替代的一次性导出文件
- One-off exports that have been replaced by better retained versions
- 只为检查或转换内容而产生的中间产物
- Intermediate artifacts created only for inspection or transformation
- 没有继续保留价值的重复副本
- Duplicate copies with no remaining purpose
- 已确认没有后续用途的派生文件
- Derived files confirmed to have no future use

## 安全规则 / Safety Rules

这个 skill 的核心原则是保守清理：不确定就保留。

The core principle of this skill is conservative cleanup: when uncertain, keep the file.

- 不会删除用户原始材料，除非用户明确要求
- Never delete original user materials unless the user explicitly asks
- 只要文件有合理复用可能，就保留
- Keep a file whenever reuse is plausible
- 不确定时保留，而不是冒险删除
- When uncertain, keep the file instead of risking data loss
- 优先安全和可追溯，而不是追求“极度干净”
- Prefer safety and traceability over extreme minimalism
- 重要清理动作需要向用户说明
- Mention meaningful cleanup actions to the user when relevant

## 安装 / Install

把 `workspace-cleanup` 文件夹复制到本地 Codex skills 目录：

Copy the `workspace-cleanup` folder into your local Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R workspace-cleanup ~/.codex/skills/
```

## 使用方式 / Usage

在 Codex 对话里，可以这样触发或设定规则：

In a Codex conversation, you can trigger or establish the rule with:

- `use workspace-cleanup`
- `follow the workspace cleanup rule`
- `clean up derived files after each task`

也可以把它作为项目级习惯：每完成一个阶段，就让 Codex 检查并清理本次产生的临时文件。

You can also use it as a project-level habit: after each meaningful phase, ask Codex to review and clean up temporary files created during that work.

## 适用场景 / Example Use Cases

这个 skill 适合长期协作项目、内容整理项目、代码改造项目，以及任何容易产生临时文件和中间产物的工作区。

This skill is useful for long-running collaboration projects, content organization work, code refactors, and any workspace that tends to generate temporary files or intermediate artifacts.

- 做完一次视频剪辑、截图整理或文档转换后，清理中间文件
- Clean up intermediate files after video editing, screenshot organization, or document conversion
- 完成一次代码修改后，保留源码和最终结果，删除无用实验文件
- After a code change, keep source files and final outputs while removing unused experiment files
- 多轮任务之后，避免工作区堆满重复副本和临时导出
- After multiple task rounds, prevent the workspace from filling with duplicate copies and temporary exports

## 文件结构 / Files

仓库里的核心文件：

Core files in this repository:

- `workspace-cleanup/SKILL.md`: 可复用的 skill 定义
- `workspace-cleanup/SKILL.md`: the reusable skill definition
