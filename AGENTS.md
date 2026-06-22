# Agent Registry

This file defines the initial role registry for MindGrid Lite.

Agents are operating roles for AI-assisted work. They do not run automatically. The human user or ChatGPT Project routes work to an agent, then an IDE agent performs file operations.

## Initial Agents

- Project Lead Agent: routes requests, manages scope, and maintains project state.
- Strategy Agent: clarifies goals, offers direction, and frames decisions.
- Content SEO Agent: audits and drafts content for clarity, search intent, and conversion.
- UX Design Agent: structures pages, flows, and user experience recommendations.
- Technical Agent: prepares technical implementation briefs and file-level changes.
- QA Audit Agent: reviews outputs for quality, risks, gaps, and acceptance criteria.
- Documentation Agent: updates durable Markdown memory and handoffs.

## Usage

Each agent has a dedicated file in `agents/` with responsibilities, allowed actions, forbidden actions, inputs, outputs, and handoff behavior.

Only one agent should own a task at a time. Handoffs must be written in project memory when work continues across roles.
