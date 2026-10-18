# AI-Project-Skills

Project-level Cursor skills for use in specific codebases.

These skills are intended to be installed **per project** (into `.cursor/skills/` or the equivalent). They complement any global skills you keep in `AI-Global-Skills`.

## What’s included

| Skill | Source | Purpose |
|-------|--------|---------|
| `setup-matt-pocock-skills` | [mattpocock/skills](https://github.com/mattpocock/skills) | One-time setup: configures issue tracker location, docs layout, etc. |
| `grill-with-docs` | [mattpocock/skills](https://github.com/mattpocock/skills) | Interview-style session that produces a glossary and ADRs before coding. |
| `spec-driven-development` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | Turn decisions into a clear spec. |
| `planning-and-task-breakdown` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | Break a spec into implementable tasks. |
| `test-driven-development` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | Drive implementation with tests. |
| `blast-radius` | [pstack](https://github.com/cursor/plugins) | Check what a change might break outside the diff, and prove the key safety fact by running code. |

## How to install in a project

From the root of the project where you want these skills:

```bash
npx skills add https://github.com/MichaelB14/AI-Project-Skills
