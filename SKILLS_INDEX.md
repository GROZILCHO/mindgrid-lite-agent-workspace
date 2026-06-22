# Skills Index

MindGrid Lite uses Markdown-based skills instead of official OpenAI Skills.

A skill is a reusable procedure stored as a `.skill.md` file. It tells an agent when to use the procedure, what inputs are required, what steps to follow, what output to produce, and what risks to watch.

## Available Skills

- `client-brief-analysis.skill.md`: analyze a client brief and extract project direction.
- `seo-content-audit.skill.md`: review content for SEO, clarity, and conversion.
- `website-page-structure.skill.md`: define the structure for a website page.
- `wordpress-implementation-brief.skill.md`: prepare practical WordPress implementation instructions.
- `codex-task-prep.skill.md`: convert project intent into an IDE-agent-ready task.
- `qa-review.skill.md`: review work for quality, gaps, and risks.

## Usage Rules

- Use skills as plain Markdown procedures.
- Do not assume any paid skill runtime or automation platform.
- Copy outputs into project memory when they affect status, decisions, tasks, or risks.
- Adapt a skill only when the project context requires it.
