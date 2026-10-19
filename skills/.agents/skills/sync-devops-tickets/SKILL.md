---
name: sync-devops-tickets
description: Sync open Azure DevOps work items into docs/tickets.md and keep project context so a new session can continue after /clear. Use when refreshing the ticket list, starting work after a clear, or when the agent needs to know which DevOps project this repo maps to.
disable-model-invocation: true
---

# Sync DevOps tickets

Keep a local, agent-readable snapshot of the current Azure DevOps backlog and the project context.

## Files

- `docs/tickets.md` — current open tickets (agent-facing)
- `docs/agents/issue-tracker.md` — DevOps project/org/team context (create or update if missing)

## Process

1. **Ensure context exists**  
   If `docs/agents/issue-tracker.md` is missing or incomplete, ask the user for:
   - Azure DevOps organization
   - Project name
   - Team or area path (if used)  
   Write it in a short, stable format so later sessions can read it.

2. **Get the current tickets**  
   Prefer, in order:
   - Azure CLI (`az boards work-item list` or equivalent) if available and authenticated
   - A list the user pastes
   - An existing `docs/tickets.md` only if the user says it is already up to date  

   Include only work that still needs to be done (exclude closed/removed unless the user asks).

3. **Write `docs/tickets.md`**  
   Overwrite the file with a clean list. For each ticket use:

   ```markdown
   ## [ID] — [Title]
   - Status: [status]
   - Summary: [one or two sentences]
   - Notes: [acceptance criteria or key constraints, if any]
