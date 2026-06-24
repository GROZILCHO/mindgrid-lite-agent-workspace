# MindGrid Lite Agent Workspace — Repository Safety Protocol

## 1. Purpose

This protocol prevents work from being performed in the wrong repository, branch, folder, or project.

MindGrid Lite often coordinates several related repositories with similar names. Before any task starts, the agent must confirm the target repository identity, absolute path, branch, allowed files, forbidden files, and stop conditions.

## 2. Current Repository Map

### mindgrid-lite-agent-workspace

- Path: `C:\Users\A.Atanasov\Desktop\MindGrid Studio\mindgrid-lite-agent-workspace`
- Purpose: control layer, project memory, decision-support system, operating model, project dashboards, risks, handoffs, and accepted outputs.
- Must not contain full implementation code for all projects.

### mindgrid-request-system

- Path: `C:\Users\A.Atanasov\Desktop\MindGrid Studio\mindgrid-request-system`
- Purpose: WordPress plugin implementation for the Mestimvsichko Smart Request Flow.
- Must not be used for general workspace governance or project memory.

### Other implementation repositories

Examples:

- `mall-agro-redesign`
- `dorostol_trade_website`
- future project-specific repos

These repositories may be referenced by the workspace, but they should not be copied into it.

## 3. Mandatory Repo Header

Every future task must begin with:

- Target repository
- Absolute path
- Repository purpose
- Task type
- Allowed files
- Forbidden files
- Stop conditions

Example for `mindgrid-lite-agent-workspace`:

```text
Target repository: mindgrid-lite-agent-workspace
Absolute path: C:\Users\A.Atanasov\Desktop\MindGrid Studio\mindgrid-lite-agent-workspace
Repository purpose: control layer / project memory / decision-support system
Task type: governance documentation update
Allowed files: REPOSITORY_SAFETY.md, OPERATING_MODEL.md
Forbidden files: projects/*, agents/*, skills/*, workflows/*, templates/*, implementation repos
Stop conditions: wrong repo root, unexpected branch, dirty tree not explained, required file outside allowed list
```

Example for `mindgrid-request-system`:

```text
Target repository: mindgrid-request-system
Absolute path: C:\Users\A.Atanasov\Desktop\MindGrid Studio\mindgrid-request-system
Repository purpose: WordPress plugin implementation for Mestimvsichko Smart Request Flow
Task type: scoped implementation or technical QA
Allowed files: explicitly named plugin files for the task
Forbidden files: mindgrid-lite-agent-workspace project memory, governance files, unrelated repos
Stop conditions: wrong repo root, unexpected branch, production/deployment impact, user data risk, missing approval
```

## 4. Mandatory Preflight Check

Before file work, run:

```bash
git rev-parse --show-toplevel
git remote -v
git branch --show-current
git status --short
```

What each command confirms:

- `git rev-parse --show-toplevel` confirms the actual repository root.
- `git remote -v` confirms the connected remote repository.
- `git branch --show-current` confirms the active branch.
- `git status --short` confirms whether the working tree is clean or already modified.

The current working directory should also be reported before file work.

## 5. Stop Conditions

The agent must stop if:

- repo root does not match the target path;
- branch is unexpected;
- working tree is unexpectedly dirty;
- task requires files outside allowed files;
- task touches a forbidden repository;
- task requires destructive commands;
- task requires commercial, pricing, production, or client approval decisions;
- task is ambiguous about which repository is the target.

## 6. Dangerous Commands

Do not use these commands without explicit human confirmation:

```bash
git clean -fd
git reset --hard
git checkout .
del /s
rmdir /s
rd /s /q
Remove-Item -Recurse
rm -rf
```

These commands are dangerous because they can delete files, remove untracked work, overwrite local changes, or recursively affect folders outside the intended task scope.

## 7. Allowed Safe Cleanup

Only specific, named, non-recursive cleanup may be allowed.

Example:

```bash
del .\-files
```

This is allowed only when:

- the exact file is known;
- it is confirmed untracked;
- it is not a directory;
- there are no wildcards;
- the command is non-recursive.

## 8. Allowed Files / Forbidden Files Rule

Every task must include explicit allowed files and forbidden files.

If a needed file is not listed as allowed, the agent must stop and ask for scope clarification instead of editing it.

## 9. Final Report Requirement

Every agent/Codex task must return:

- Repository
- Path
- Branch
- Remote
- Files changed
- Files intentionally not modified
- Final `git status --short`

## 10. Cross-Repository Rule

- Control repo tasks must not edit implementation repos.
- Implementation repo tasks must not edit control repo memory.
- Project code stays in implementation repos.
- Project memory stays in `mindgrid-lite-agent-workspace`.

## 11. Naming Risk

There is a specific risk from similar names:

- MindGrid Studio
- `mindgrid-lite-agent-workspace`
- `mindgrid-request-system`

Task prompts must use absolute paths to reduce this risk.

## 12. Core Rule

No task starts without repository identity, absolute path, branch check, allowed files, forbidden files, and stop conditions.
