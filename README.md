# AI-Project-Skills

Project-level Cursor skills for specific codebases.

Install these per project (into `.cursor/skills/` or equivalent). They complement the global skills in [AI-Global-Skills](https://github.com/MichaelB14/AI-Global-Skills).

## Skills

| Skill | Source | Purpose |
|-------|--------|---------|
| `setup-matt-pocock-skills` | [mattpocock/skills](https://github.com/mattpocock/skills) | One-time setup for issue tracker and docs layout |
| `grill-with-docs` | [mattpocock/skills](https://github.com/mattpocock/skills) | Interview session that produces a glossary and ADRs |
| `grilling` | [mattpocock/skills](https://github.com/mattpocock/skills) | Required by `grill-with-docs` |
| `domain-modeling` | [mattpocock/skills](https://github.com/mattpocock/skills) | Required by `grill-with-docs` |
| `to-spec` | [mattpocock/skills](https://github.com/mattpocock/skills) | Turn the current conversation into a spec |
| `to-tickets` | [mattpocock/skills](https://github.com/mattpocock/skills) | Break a spec into tracer-bullet tickets |
| `prototype` | [mattpocock/skills](https://github.com/mattpocock/skills) | Build a throwaway prototype to explore an idea |
| `handoff` | [mattpocock/skills](https://github.com/mattpocock/skills) | Capture context for another session or agent |
| `improve-codebase-architecture` | [mattpocock/skills](https://github.com/mattpocock/skills) | Find deepening opportunities and grill through them |
| `spec-driven-development` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | Turn decisions into a clear spec |
| `planning-and-task-breakdown` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | Break a spec into implementable tasks |
| `test-driven-development` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | Drive implementation with tests |
| `blast-radius` | [pstack](https://github.com/cursor/plugins) | Check what a change might break outside the diff |
| `triage` | [mattpocock/skills](https://github.com/mattpocock/skills) | Move issues and external PRs through a state machine of triage roles, categorise, verify, grill if needed, and write agent-ready briefs. |

## Typical workflow

1. **Setup** — Run `/setup-matt-pocock-skills` once so skills know where docs and the issue tracker live.
2. **Clarify** — Start the next change with `/grill-with-docs`. It writes or updates `GLOSSARY.md` and ADRs.
3. **Explore** (optional) — Use `/prototype` to try an idea before locking it in.
4. **Specify** — Run `/to-spec`, then `/to-tickets`. Or use Addy’s `/spec-driven-development` → `/planning-and-task-breakdown`.
5. **Implement** — Build with `/test-driven-development` (or Matt’s implement flow).
6. **Check** — Run `/blast-radius` on changes you’re unsure about before merging.
7. **Hand off** — Use `/handoff` when another session needs to continue.

## Install

From the project root:

```bash
npx skills add https://github.com/MichaelB14/AI-Project-Skills
