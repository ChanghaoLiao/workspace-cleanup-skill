# workspace-cleanup

A reusable Codex skill for keeping project workspaces clean and organized.

## What it does

This skill tells Codex to clean up after each meaningful task by:

- reviewing files created during the task
- keeping source materials, final outputs, active notes, and reusable artifacts
- deleting only derived files that are clearly no longer needed
- preserving a tidy, low-clutter workspace

## Safety rules

The skill is intentionally conservative:

- it never deletes original user materials unless explicitly asked
- it keeps files when reuse is plausible
- it prefers safe retention over aggressive cleanup

## Install

Copy the `workspace-cleanup` folder into your local Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R workspace-cleanup ~/.codex/skills/
```

## Usage

In a Codex conversation, ask for:

- `use workspace-cleanup`
- `follow the workspace cleanup rule`
- `clean up derived files after each task`

## Files

- `workspace-cleanup/SKILL.md`: the reusable skill definition
