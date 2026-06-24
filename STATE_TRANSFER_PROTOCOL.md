# MindGrid Lite Agent Workspace — State Transfer Protocol

## 1. Purpose

Този протокол дефинира как проверено project state се движи между implementation repos, `mindgrid-lite-agent-workspace`, PM Assistant, ChatGPT strategic review и Project Lead decisions.

Целта е да се намали manual copy/paste и да се предотврати ситуация, в която Project Lead действа като ръчен messenger между agents, tools, repos и project memory.

State transfer трябва да става чрез кратки, структурирани packets, не чрез разхвърляни logs, chat fragments или устни предположения.

## 2. Core Principle

Implementation repos produce technical facts.

Workspace stores project memory and status.

PM Assistant reviews project/commercial implications.

ChatGPT strategic review coordinates and critiques.

Project Lead makes final decisions.

Agent analysis is not a decision.

Implementation status is not commercial approval.

Demo/RC status is not production approval.

## 3. Repositories and Information Flow

Preferred flow:

```text
Implementation repo
-> Project State Transfer Packet
-> mindgrid-lite-agent-workspace
-> Workspace Sync Packet
-> PM Review Packet
-> PM Assistant
-> PM Feedback Integration Packet
-> mindgrid-lite-agent-workspace
-> Decision Packet
-> Project Lead
```

Brief explanation:

- Implementation repo: източник на technical facts от code, Git, tags, QA и реални files.
- Project State Transfer Packet: структурира technical state за пренасяне към control workspace.
- `mindgrid-lite-agent-workspace`: пази project memory, scope, risks, tasks, handoffs и accepted outputs.
- Workspace Sync Packet: дефинира как project memory трябва да се обнови след проверен state.
- PM Review Packet: подготвя кратък review материал за PM Assistant.
- PM Assistant: оценява commercial, project management и client expectation implications.
- PM Feedback Integration Packet: структурира PM feedback обратно към workspace.
- Decision Packet: подготвя ясно решение за Project Lead.
- Project Lead: приема или отказва final business decision.

## 4. Source Information Categories

### Hard Technical Facts

Examples:

- repo name;
- absolute path;
- branch;
- commit hash;
- tag;
- working tree status;
- changed files;
- implemented features;
- tested functionality;
- QA results;
- known technical limitations.

Hard technical facts трябва да идват от repo, Git, files, staging, logs, tests или друг проверим artifact.

### Project Lead Reported Context

Examples:

- client saw demo;
- client liked direction;
- client requested offer;
- client asked about calendar or payment;
- client gave informal feedback.

Това е useful context, но не е hard fact, освен ако не е подкрепено от artifact, written approval или explicit decision.

### PM Assistant Interpretation

Examples:

- commercial risk;
- offer scope risk;
- client expectation risk;
- Phase 1 / Phase 2 boundary;
- pricing readiness;
- production readiness concerns.

PM Assistant interpretation е review input. То не е final approval, освен ако Project Lead explicit го приеме.

### Final Decisions

Examples:

- final scope approved;
- price approved;
- offer sent;
- client accepted;
- production approved;
- feature postponed;
- project paused.

Final decisions трябва да бъдат explicit, attributable и записани в правилното project memory място.

## 5. Packet Types

### 1. Project State Transfer Packet

Purpose: пренася проверен technical state от implementation repo към control workspace.

Source: implementation repo.

Target: `mindgrid-lite-agent-workspace` project folder or output.

Required inputs: repo path, branch, commit/tag, working tree status, changed files, implemented behavior, QA results, limitations, risks.

Expected output: concise state packet ready for workspace review or sync.

What it must not decide: pricing, offer approval, production approval, client acceptance, scope expansion.

Stop conditions: wrong repo, dirty tree not understood, missing branch/commit, production impact not approved, unclear target project.

### 2. Workspace Sync Packet

Purpose: дефинира как accepted state се записва в project memory.

Source: accepted state output or transfer packet.

Target: project memory files inside `mindgrid-lite-agent-workspace`.

Required inputs: source packet, target project folder, memory files to update, status/task/risk/next-action changes, decisions not made.

Expected output: approved memory update plan or completed memory sync.

What it must not decide: new business decisions, pricing, client approval, production approval.

Stop conditions: source output not accepted, unclear memory files, decision required, forbidden file needed.

### 3. PM Review Packet

Purpose: да даде concise review material на PM Assistant.

Source: workspace state, accepted outputs, implementation facts, risks.

Target: PM Assistant.

Required inputs: what has been done, what is confirmed, what is not confirmed, demo/RC status, production status, offer readiness, risks, questions.

Expected output: PM review, commercial risks, scope concerns, suggested corrections, next recommendation.

What it must not decide: final approval, final price, final offer, production execution.

Stop conditions: raw unfiltered logs, missing production boundary, unclear scope, unclear approval status.

### 4. PM Feedback Integration Packet

Purpose: структурира PM feedback обратно към workspace.

Source: PM Assistant review.

Target: `mindgrid-lite-agent-workspace`.

Required inputs: PM verdict, requested corrections, new risks, scope suggestions, commercial boundary notes, production boundary notes, client questions.

Expected output: integration summary and recommended memory/action updates.

What it must not decide: final acceptance of PM recommendation, client approval, price approval, production approval.

Stop conditions: PM feedback is ambiguous, Project Lead decision required, suggested change conflicts with approved scope.

### 5. Decision Packet

Purpose: подготвя explicit decision за Project Lead.

Source: workspace memory, PM feedback, QA, implementation facts, strategy analysis.

Target: Project Lead.

Required inputs: decision needed, options, recommendation, risks, affected files/repos, approval line.

Expected output: accepted, rejected, deferred, or revised decision.

What it must not decide: anything on behalf of Project Lead.

Stop conditions: unclear decision owner, missing options, missing risks, decision affects commercial/production/legal/client commitment without explicit approval.

### 6. Project Rehydration Packet

Purpose: възстановява project context след пауза.

Source: project memory and linked implementation repo status.

Target: active agent or Project Lead.

Required inputs: current status, tasks, issues, next actions, handoff, linked repo status, last known commit/tag, stale assumptions.

Expected output: current safe state, unresolved risks, stale assumptions, next safe action.

What it must not decide: new scope, production approval, pricing, client acceptance.

Stop conditions: memory and repo state conflict, linked repo unavailable, unclear next action, unresolved approval gate.

## 6. Project State Transfer Packet

This packet is generated after work or inspection in an implementation repo.

Required fields:

- Source implementation repo
- Source absolute path
- Target control repo
- Target project folder
- Branch
- Latest commit
- Latest tag, if any
- Working tree status
- Files changed
- What changed
- Current demonstrable capability
- QA performed
- Known limitations
- New risks
- Production readiness status
- Commercial / PM implications
- Workspace files that may need sync
- Items that must not be updated without human decision

This packet must not approve pricing, final offer, production, client acceptance, or scope expansion.

## 7. Workspace Sync Packet

This packet is used to update project memory inside `mindgrid-lite-agent-workspace`.

Required fields:

- Source packet reviewed
- Workspace project folder
- Memory files to update
- Status changes
- Task changes
- Risk changes
- Next action changes
- Handoff changes
- Decisions not made
- Files intentionally not modified

`DECISIONS_LOG.md` must only be updated if there is an explicit human / Project Lead decision.

## 8. PM Review Packet

This packet is sent to PM Assistant.

Required fields:

- What has been done
- What is confirmed
- What is not confirmed
- Current demo/RC status
- Production/live status
- Offer readiness status
- Main risks
- Specific questions for PM Assistant
- What PM Assistant should not do yet

PM Assistant should receive concise review packets, not raw repo logs or scattered chat history.

## 9. PM Feedback Integration Packet

This packet is used after PM Assistant gives review.

Required fields:

- PM verdict
- Corrections requested
- New risks identified
- Scope changes suggested
- Commercial boundary changes
- Production boundary changes
- Questions for client
- Recommended next action
- Whether offer draft is allowed or still blocked

PM feedback is not final approval unless Project Lead accepts it.

## 10. Decision Packet

This packet is used when Project Lead must make a decision.

Required fields:

- Decision needed
- Options
- Recommendation
- Risks
- Files or repos affected
- What changes after approval
- What remains blocked
- Explicit approval line

Examples:

- approve Phase 1 scope;
- approve price;
- approve sending offer;
- approve production work;
- postpone calendar;
- keep payment as Phase 2.

## 11. Project Rehydration Packet

This packet is used when returning to a project after a pause.

Required checks:

- read `CURRENT_STATUS.md`;
- read `TASKS.md`;
- read `ISSUES_LOG.md`;
- read `NEXT_ACTIONS.md`;
- read `AGENT_HANDOFF.md`;
- inspect linked implementation repo status;
- compare last known commit/tag against current repo state;
- identify stale assumptions;
- identify next safe action.

No project should resume from chat memory alone after a long pause.

## 12. Two-Repo Workflow

Codex may work across both an implementation repo and `mindgrid-lite-agent-workspace` only when a two-repo workflow is explicitly requested.

Rules:

- two-repo workflow must be explicitly requested;
- both repos require preflight checks;
- allowed files must be listed separately for each repo;
- forbidden files must be listed separately for each repo;
- final report must include status of both repos;
- if either repo is unexpectedly dirty, stop;
- if target repo is ambiguous, stop.

Default should remain one-repo work unless a two-repo workflow is explicitly authorized.

## 13. Minimal Copy/Paste Rule

Project Lead should not have to copy raw logs, long terminal output, or full chat history between systems.

Preferred transfer unit:

- concise packet;
- structured summary;
- clear next action;
- open risks;
- files affected;
- decision needed.

## 14. What Must Never Be Transferred as Fact Without Verification

Do not transfer these as facts without explicit verification:

- client approval;
- price approval;
- production approval;
- legal/privacy approval;
- payment model approval;
- calendar booking logic approval;
- AI/Maps/API approval;
- final offer approval.

These must remain pending unless Project Lead explicitly confirms.

## 15. Example: mindgrid-request-system to workspace

Source:

- `mindgrid-request-system`
- branch `develop`
- tag `v0.6.0-rc.1`

Target:

- `mindgrid-lite-agent-workspace`
- `projects/mestimvsichko-smart-request-flow/`

Example packet summary:

- demo/RC implementation exists;
- production/live remains HOLD;
- estimate is indicative/demo unless approved otherwise;
- calendar, payment, Maps, and AI remain out of base scope unless separately scoped;
- workspace memory may need update;
- final offer and pricing are not approved.

This example is a state transfer example, not new Mestimvsichko project work.

## 16. Relationship to Operating Model and Repository Safety

- `OPERATING_MODEL.md` defines how the system works.
- `REPOSITORY_SAFETY.md` defines how to avoid wrong-repo work.
- `STATE_TRANSFER_PROTOCOL.md` defines how information moves between systems.

## 17. Core Rule

No project state should move between repos, PM Assistant, ChatGPT, or Project Lead as loose unstructured text when it can be moved as a packet.
