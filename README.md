# MindGrid Lite Agent Workspace

MindGrid Lite is a low-cost, IDE-first workspace for managing AI-assisted work without building a custom app.

The workspace uses:

- Markdown files as shared memory and operational state.
- ChatGPT Project as the command center for planning, requests, and coordination.
- VS Code, Codex, or another IDE agent as the file execution environment.
- Git as the change history and review trail.
- The human user as the approval gatekeeper.

## How To Use

1. Start with a project folder copied from `projects/_project-template/`.
2. Fill in `PROJECT_BRIEF.md`, `CURRENT_STATUS.md`, and `NEXT_ACTIONS.md`.
3. Use ChatGPT Project to decide the next request and route it to an agent role.
4. Let the IDE agent edit files, update memory, and prepare outputs.
5. Review changes before approving any external action, publication, or commit.

## Operating Model

ChatGPT Project is the command center, but it is not the source of truth. The source of truth is the Markdown memory in this repository.

Agents are role definitions. Skills are reusable Markdown procedures. Workflows define repeatable sequences. Templates create consistent project memory.

## Core Rule

If important context, decisions, tasks, risks, or next actions are not written into Markdown files, they are not considered durable workspace memory.
