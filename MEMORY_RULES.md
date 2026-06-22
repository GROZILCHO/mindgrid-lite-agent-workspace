# Memory Rules

Markdown files are the shared memory and operational state of this workspace.

ChatGPT Project may coordinate work, but durable memory belongs in repository files.

## Project Memory Files

- `PROJECT_BRIEF.md`: project purpose, goals, audience, scope, constraints, stakeholders, and success criteria.
- `CURRENT_STATUS.md`: current state, active phase, recent progress, blockers, and working assumptions.
- `DECISIONS_LOG.md`: dated decisions, rationale, approver, and impact.
- `TASKS.md`: actionable work items, owners or agent roles, status, priority, and acceptance criteria.
- `ISSUES_LOG.md`: bugs, risks, blockers, concerns, and unresolved questions.
- `NEXT_ACTIONS.md`: the immediate next steps, approval needs, and recommended sequence.
- `AGENT_HANDOFF.md`: context passed between agents, including completed work and open threads.
- `outputs/`: generated deliverables, drafts, exports, and reviewed artifacts.

## Writing Rules

- Keep entries concise, dated when useful, and operational.
- Record decisions once in the right file instead of duplicating them everywhere.
- Do not rely on chat history for important project state.
- Update memory at the end of each meaningful work session.
- Mark uncertainty clearly instead of presenting assumptions as facts.
