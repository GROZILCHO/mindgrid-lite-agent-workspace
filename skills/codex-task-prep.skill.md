# Codex Task Prep Skill

## Purpose

Convert project intent into an IDE-agent-ready task.

## When To Use

Use before asking Codex or another IDE agent to inspect files, create structure, edit content, or run checks.

## Required Inputs

- Goal.
- Approved file scope.
- Constraints.
- Expected output.
- Verification requirements.

## Process

1. State the task in one clear objective.
2. List allowed files and forbidden actions.
3. Provide relevant context and source files.
4. Define acceptance criteria.
5. Specify final reporting requirements.

## Output Format

- Task objective.
- Context.
- Allowed scope.
- Constraints.
- Acceptance criteria.
- Final response requirements.

## Risks

- Giving broad write access.
- Omitting verification expectations.
- Asking the agent to infer business decisions.
