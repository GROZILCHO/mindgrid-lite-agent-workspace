# MindGrid Lite Agent Workspace — Project Intake Packet Template

## 1. Purpose

Този template се използва за onboarding на проект в `mindgrid-lite-agent-workspace` като control folder / project memory entry.

Intake packet трябва да изясни:

- какъв е проектът;
- къде живее реалната работа;
- какво е известно;
- какво е неизвестно;
- какво трябва да се verify-не;
- коя е следващата безопасна стъпка.

Този template не създава implementation code.

Този template не одобрява scope, цена, production или client commitments.

Този template е intake input, не final project decision.

## 2. When to Use This Template

Use this template when:

- adding a new project to `projects/`;
- returning to an old project after a pause;
- consolidating a project currently spread across chats;
- preparing a project for PM Assistant review;
- preparing a project for Codex implementation work;
- creating a dashboard entry based on verified information.

Do not use it as:

- a final offer;
- a technical specification;
- a production approval;
- a pricing document;
- a replacement for PM Assistant or Project Lead decisions.

## 3. Required Source Types

### Hard Facts

Examples:

- repo URL;
- local path;
- branch;
- latest commit/tag;
- live/staging URL;
- existing files;
- plugin/theme/app status;
- verified QA result.

### Project Lead Reported Context

Examples:

- client liked a direction;
- client requested a quote;
- client gave informal feedback;
- boss/client requested changes;
- project priority changed.

### Agent / PM Analysis

Examples:

- Strategy Agent recommendation;
- PM Assistant review;
- QA Agent finding;
- Content/UX/Technical Agent output.

### Final Decisions

Examples:

- approved scope;
- approved price;
- approved production deployment;
- sent offer;
- accepted offer;
- paused project.

Do not mix these categories.

Do not record analysis as decision.

Do not record client interest as approval.

## 4. Intake Packet Fields

Copy and complete this section when preparing a project intake.

### Project Identity

- Project name:
- Short internal name / slug:
- Related client / brand:
- Project Lead:
- Primary language:
- Current priority:
- Current phase:

### Project Type

Choose or describe:

- Website
- WordPress plugin
- Next.js app
- Marketing campaign
- SEO project
- Design system
- Content project
- AI agent / automation system
- Other

### Business Purpose

- What problem does this project solve?
- Who is it for?
- Why does it matter now?
- What would count as success?

### Current Known Status

- What is already done?
- What is currently active?
- What is paused?
- What is blocked?
- What is unknown?

### Control Workspace Status

- Does a control folder already exist?
- Existing control folder path, if any:
- Required control folder path:
- Existing project memory files:
- Missing project memory files:

### Implementation Repository / Work Location

- Implementation repo name:
- GitHub URL:
- Local absolute path:
- Current branch:
- Latest known commit:
- Latest known tag:
- Working tree status:
- Live URL:
- Staging URL:
- Admin/backend URL, if relevant:
- Main technology stack:

If any of these are unknown, mark `Unknown / Needs verification`.

### Existing Materials

- Relevant chats:
- Existing documents:
- Existing design files:
- Existing images/assets:
- Existing PM Assistant reviews:
- Existing client feedback:
- Existing technical reports:
- Existing QA reports:

### Current Risks

- Scope risk:
- Technical risk:
- Commercial risk:
- Client expectation risk:
- Content risk:
- Design/UX risk:
- Production/deployment risk:
- Legal/privacy risk:
- Time/budget risk:

### Open Questions

- Questions for Project Lead:
- Questions for client:
- Questions for PM Assistant:
- Questions for Technical Agent:
- Questions for Content/UX/SEO:
- Questions before implementation:
- Questions before offer/pricing:

### Required Packets Before Work

Choose which packets are required:

- Project State Transfer Packet
- PM Review Packet
- PM Feedback Integration Packet
- Decision Packet
- Project Rehydration Packet
- Implementation Packet
- QA Packet
- Memory Sync Packet

### Proposed Project Control Folder

- Proposed folder path:
- Proposed files to create:
  - `PROJECT_BRIEF.md`
  - `CURRENT_STATUS.md`
  - `TASKS.md`
  - `NEXT_ACTIONS.md`
  - `ISSUES_LOG.md`
  - `DECISIONS_LOG.md`
  - `AGENT_HANDOFF.md`
  - `outputs/`

### Proposed First Workspace Action

- Create control folder:
- Create initial project memory:
- Request PM Assistant review:
- Inspect implementation repo:
- Prepare Project State Transfer Packet:
- Prepare offer/scope review:
- Pause until more information:
- Other:

### Stop Conditions

The intake must stop if:

- target repo is unclear;
- implementation repo path is unknown and required;
- project scope is unclear;
- client approval is assumed but not verified;
- production status is unclear;
- pricing/offer is being requested without PM/Project Lead review;
- work would touch implementation code before control folder exists;
- work would require destructive commands;
- work would mix control repo and implementation repo changes without explicit two-repo workflow approval.

## 5. Minimal Intake Version

Use this short form for fast onboarding when full intake is too heavy.

- Project:
- Client / brand:
- Control folder exists?
- Implementation repo:
- Local path:
- Current phase:
- Last known status:
- Next safe action:
- Blocked by:
- Top 3 risks:
- Human decision needed:
- Packet needed before work:

## 6. Example Intake: Mall Agro Redesign

- Project name: Mall Agro Redesign
- Status: Needs intake
- Control folder: missing / not yet created
- Implementation repo: known from broader project context but must be verified before recording hard facts
- Next safe action: create Project Intake Packet and verify implementation repo status
- Risks: context spread across chats, active implementation not centralized in workspace memory

Do not invent commit hashes, branches, URLs, current tasks, or QA results.

## 7. Example Intake: Dorostol Trade Website

- Project name: Dorostol Trade Website
- Status: Needs intake
- Control folder: missing / not yet created
- Implementation repo: Unknown / Needs verification
- Next safe action: create Project Intake Packet
- Risks: multilingual/content/design drift, context spread across chats

Do not invent commit hashes, branches, URLs, current tasks, or QA results.

## 8. Relationship to Existing System Documents

- `OPERATING_MODEL.md` defines how the system works.
- `REPOSITORY_SAFETY.md` defines repo safety.
- `STATE_TRANSFER_PROTOCOL.md` defines how information moves.
- `PROJECTS_DASHBOARD.md` summarizes project status.
- `PROJECT_INTAKE_PACKET_TEMPLATE.md` defines how new projects enter the workspace.

## 9. Core Rule

No project should be added to the dashboard as active unless it has either a control folder or a completed Project Intake Packet with clearly marked unknowns.
