---
name: "workspace-cleanup"
description: "Use when the user wants a clean workspace, asks Codex to clean up after each task, or wants a standing rule to delete temporary or derived files that are clearly no longer needed while preserving source materials and any files likely to be reused."
---

# Workspace Cleanup

Apply this skill when the user wants ongoing workspace hygiene, post-task cleanup, or a persistent rule to keep project folders tidy.

## Core rule

After each meaningful task:

1. Review files created or modified during the task.
2. Keep files that are source materials, final deliverables, active notes, or likely to be reused.
3. Delete only derived files that are clearly no longer needed.
4. Leave the workspace in a simpler, cleaner state than before.

## What to keep

- User-provided source files
- Final outputs
- Working notes that still guide the project
- Reusable extracted or translated materials
- Files needed for traceability, citation, or later editing

## What to delete

- Temporary scratch files
- One-off exports that have been superseded
- Intermediate artifacts that were only created to inspect or transform content
- Duplicate copies with no remaining purpose
- Any derived file that is confirmed to have no future use

## Safety rules

- Never delete original user materials unless the user explicitly asks.
- Never delete a file if there is a reasonable chance it will be reused.
- When uncertain, keep the file.
- Prefer conservative cleanup over aggressive cleanup.
- Do not hide cleanup: mention what was removed when it matters.

## Decision standard

Before deleting a derived file, ask:

- Is this an original source or a user-authored asset?
- Does this file support later writing, citation, or verification?
- Has it already been replaced by a better retained artifact?
- Am I highly confident it will not be needed again?

Delete the file only if the answers support safe removal.

## Typical workflow

1. Finish the task.
2. Identify newly created artifacts.
3. Separate them into `keep` and `delete`.
4. Remove the `delete` set.
5. Briefly report the cleanup if it is relevant to the user.

## Project-level standing instruction

If the user establishes cleanup as a standing rule for the workspace, treat this skill as active for the remainder of the project unless the user says otherwise.
