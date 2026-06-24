# MindGrid Lite Agent Workspace — Projects Dashboard

## 1. Purpose

Този файл е top-level overview на активни и планирани проекти в MindGrid Lite Agent Workspace.

Целта му е Project Lead бързо да вижда:

- къде стои всеки проект;
- къде има project memory;
- кое implementation repo е свързано;
- коя е следващата безопасна стъпка;
- какво е blocked;
- къде е нужен PM Assistant или human decision.

Dashboard-ът е index / overview / control surface. Той не заменя detailed project memory.

## 2. Dashboard Rules

- Този dashboard summarizes; той не заменя project memory.
- Detailed truth остава в project folder-а.
- Implementation facts трябва да идват от implementation repos или state transfer packets.
- Client/project context трябва да се маркира като Project Lead reported context, освен ако не е verified.
- PM Assistant interpretation е review input, не final decision.
- Final decisions изискват explicit Project Lead / human approval.
- Unknown details трябва да се маркират като `Unknown / Needs intake`, не да се guess-ват.
- Dashboard updates трябва да намаляват context recovery time, не да създават още manual reporting.

## 3. Current System Layer Status

Project: MindGrid Lite Agent Workspace

Current status: System foundation active.

Existing system files:

- `OPERATING_MODEL.md`
- `REPOSITORY_SAFETY.md`
- `STATE_TRANSFER_PROTOCOL.md`
- `PROJECTS_DASHBOARD.md`

Current purpose:

Control layer, project memory, decision-support system, repo safety, state transfer, project overview.

Next safe action:

Use dashboard to onboard projects through Project Intake Packets.

Top risks:

- Too much documentation without operational reduction.
- Project Lead becoming a messenger again.
- Stale dashboards if not updated through packets.
- Mixing control repo and implementation repo work.

## 4. Projects Overview Table

| Project | Control folder | Implementation repo | Current phase | Last known status | Next safe action | Blocked by | Top risks | PM review needed? | Human decision needed? |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Mestimvsichko Smart Request Flow | `projects/mestimvsichko-smart-request-flow/` | `mindgrid-request-system` | Offer preparation review | Demo/RC implementation exists; demo/client discussion GO; production/live HOLD; PM Assistant review reported as Needs Correction in current task context | PM review feedback integration / scope correction plan | Final scope, price, client approval, technical corrections, upload/staff workflow/privacy/version clarifications | Estimate expectation, calendar/payment scope creep, uploads gap, staff workflow, version mismatch, production readiness | Yes | Yes |
| Mall Agro Redesign | Missing / Needs intake | Unknown / not onboarded in workspace | Needs intake | Control folder missing; implementation repo not verified in workspace | Create Project Intake Packet | Missing control folder and verified repo state | Context spread across chats; active implementation not centralized in workspace memory | Unknown / after intake | Yes, for intake approval |
| Dorostol Trade Website | Missing / Needs intake | Unknown / not onboarded in workspace | Needs intake | Control folder missing; implementation repo not verified in workspace | Create Project Intake Packet | Missing control folder and verified repo state | Multilingual/content/design drift; project context spread across chats | Unknown / after intake | Yes, for intake approval |
| Trend Address / Call For All Marketing Work | Missing / Needs intake | Unknown / not onboarded in workspace | Planned / Needs intake | No control folder verified | Defer until active need or create lightweight intake | Project not yet onboarded | Marketing scope scattered across chats and tools | Unknown / after intake | Yes, if activated |

## 5. Active Project Details

### Mestimvsichko Smart Request Flow

- Control folder: `projects/mestimvsichko-smart-request-flow/`
- Implementation repo: `mindgrid-request-system`
- Current phase: Offer preparation review
- Last accepted output: `outputs/offer-scope-mapping.md`
- Last known technical status: Existing WordPress plugin demo / release-candidate implementation exists in the external plugin repo; branch `develop`; latest relevant commit `77c64a1 merge: sprint 6 demo estimate preview into develop`; latest relevant tag `v0.6.0-rc.1`.
- Client / external status: Project Lead reported demo/client discussion GO; client reportedly saw direction and asked for an offer; current task context reports PM Assistant review returned Needs Correction.
- Production status: HOLD. Production execution is not approved.
- Next safe action: Prepare PM review feedback integration / scope correction plan before final offer, pricing, or production work.
- Blocked by: final scope, price, client approval, technical corrections, privacy path, upload decision, staff workflow, exact viewed version, meaning of "right direction", version mismatch.
- Top risks: estimate expectation, request vs booking confusion, calendar/payment scope creep, upload gap, staff workflow gap, privacy/legal wording, plugin version mismatch, production readiness.
- Required packet before next work: PM Feedback Integration Packet or Decision Packet, depending on whether Project Lead has accepted PM recommendations.
- Recommended next agent / reviewer: Strategy Agent for scope correction framing, then QA Audit Agent; Project Lead / PM Assistant review before commercial decision.

### Mall Agro Redesign

- Control folder: Missing / Needs intake
- Implementation repo: Unknown / not onboarded in workspace
- Current phase: Needs intake
- Last accepted output: Unknown / Needs intake
- Last known technical status: Unknown / Needs intake
- Client / external status: Unknown / Needs intake
- Production status: Unknown / Needs intake
- Next safe action: Create Project Intake Packet.
- Blocked by: missing control folder, missing verified repo facts, missing current status, missing risks, missing next action.
- Top risks: context spread across chats, active implementation not centralized in workspace memory, unclear repo/status boundary.
- Required packet before next work: Project Intake Packet.
- Recommended next agent / reviewer: Project Lead Agent for intake; Documentation Agent after intake approval.

### Dorostol Trade Website

- Control folder: Missing / Needs intake
- Implementation repo: Unknown / not onboarded in workspace
- Current phase: Needs intake
- Last accepted output: Unknown / Needs intake
- Last known technical status: Unknown / Needs intake
- Client / external status: Unknown / Needs intake
- Production status: Unknown / Needs intake
- Next safe action: Create Project Intake Packet.
- Blocked by: missing control folder, missing verified repo facts, missing current status, missing risks, missing next action.
- Top risks: multilingual/content/design drift, project context spread across chats, unclear source of truth for implementation and content status.
- Required packet before next work: Project Intake Packet.
- Recommended next agent / reviewer: Project Lead Agent for intake; Strategy Agent or Documentation Agent after intake approval.

### Trend Address / Call For All Marketing Work

- Control folder: Missing / Needs intake
- Implementation repo: Unknown / not onboarded in workspace
- Current phase: Planned / Needs intake
- Last accepted output: Unknown / Needs intake
- Last known technical status: Unknown / Needs intake
- Client / external status: Unknown / Needs intake
- Production status: Not applicable / Unknown until intake
- Next safe action: Defer until active need or create lightweight intake.
- Blocked by: missing Project Lead activation, missing control folder, missing project brief.
- Top risks: marketing scope scattered across chats and tools, unclear campaign ownership, unclear approval path.
- Required packet before next work: Lightweight Project Intake Packet if activated.
- Recommended next agent / reviewer: Project Lead Agent.

## 6. Project Intake Queue

1. Mall Agro Redesign
   - Why intake is needed: project is known as planned/active work, but no control folder is verified in this workspace.
   - Minimal files to create later: `PROJECT_BRIEF.md`, `CURRENT_STATUS.md`, `TASKS.md`, `ISSUES_LOG.md`, `NEXT_ACTIONS.md`, `DECISIONS_LOG.md`, `AGENT_HANDOFF.md`, `outputs/`.
   - Required information before intake: target repo path, current branch, current status, main goals, client/business context, top risks, next safe action.

2. Dorostol Trade Website
   - Why intake is needed: project context is not centralized in this workspace.
   - Minimal files to create later: `PROJECT_BRIEF.md`, `CURRENT_STATUS.md`, `TASKS.md`, `ISSUES_LOG.md`, `NEXT_ACTIONS.md`, `DECISIONS_LOG.md`, `AGENT_HANDOFF.md`, `outputs/`.
   - Required information before intake: target repo path, language/content scope, current implementation status, design/content risks, next safe action.

3. Trend Address / Call For All Marketing Work
   - Why intake is needed: marketing work can spread across chats and tools without a control folder.
   - Minimal files to create later: lightweight project brief, current status, tasks, issues, next actions, handoff, outputs.
   - Required information before intake: active campaign need, channels, approval owner, content scope, deadlines if any, next safe action.

4. Other active projects to be added only after Project Lead confirmation
   - Why intake is needed: avoid creating project folders from vague memory.
   - Minimal files to create later: use standard project folder structure.
   - Required information before intake: explicit Project Lead confirmation and target repo/project facts.

## 7. Next Safe System Actions

1. QA review of `PROJECTS_DASHBOARD.md`.
2. Commit dashboard if QA passes.
3. Create a Project Intake Packet template.
4. Use the template to onboard Mall Agro Redesign.
5. Do not update project statuses manually unless based on project memory, state transfer packet, PM review packet, or Project Lead decision.

## 8. Update Rules

This dashboard may be updated:

- after accepted project memory sync;
- after Project State Transfer Packet;
- after PM Feedback Integration Packet;
- after explicit Project Lead decision;
- after project intake.

This dashboard must not be updated:

- from vague chat memory alone;
- from unverified assumptions;
- from Codex analysis without review;
- from implementation repo changes that have not been transferred through a packet.

## 9. Core Rule

The dashboard must reduce Project Lead context recovery time. If maintaining the dashboard creates more work than clarity, the update process must be simplified.
