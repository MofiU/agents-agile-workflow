---
name: agile-workflow
description: Sprint execution for AI agent teams - use when running sprints, managing backlogs, tracking tasks, or handling blockers. AI agents work autonomously on tasks. Use whenever sprints, agile, ceremonies, backlog, or task states are mentioned. Activates for: sprint planning, daily status, sprint review, retrospective, blocker escalation, backlog prioritization.
---

# Agile Workflow for AI Teams

## Core Principle

**Task-driven autonomous execution.** AI agents own their responsibilities and act without waiting for commands.

**No human rituals.** AI teams skip estimation, daily standups, attendance, and psychological safety. Just tasks flowing through states.

## Project Structure

```
This skill includes:
├── SKILL.md            # This file - workflow orchestration
└── agents/
    ├── sprint-master.md      # Coordinates the sprint
    ├── product-owner.md      # Defines goals and priorities
    ├── developer-agent.md    # Executes tasks with TDD
    ├── qa-agent.md          # Verifies quality
    └── code-reviewer.md      # Reviews PRs
```

## Sprint Rhythm (2 weeks / 10 days)

```
Day 1:    Sprint Planning → Tasks distributed to agents
Day 2-9:  Agents work autonomously → blockers escalate as needed
Day 10:   Sprint Review → Retro → Next Sprint Planning
```

## Task States

```
Backlog → Ready → In Progress → In Review → Accepted
                 ↓
             Rejected → (fix) → In Review
```

## Quick Commands

```
sprint:start          → Create sprint backlog, assign tasks
sprint:status         → Show sprint progress, burndown
sprint:review         → Demo completed, report metrics
sprint:retro          → Generate improvement actions
task:add <desc>        → Add to backlog
task:claim <id>       → Start working
task:done <id>         → Move to Accepted
blocker:add <id>       → Log blocker, escalate
```

## Daily Autonomy Loop

Each AI agent runs continuously:

```
1. Check Ready queue → claim task
2. Execute TDD → submit PR
3. Review others' PRs
4. Update task state
5. Blocked > 15min → escalate to SM
```

## Blocker Escalation

| Priority | Issue | SLA | Action |
|----------|-------|-----|--------|
| P0 | Service down | 1h | Escalate immediately |
| P1 | API unavailable | 4h | SM coordinates |
| P2 | Build broken | 24h | Fix or work around |
| P3 | Unclear spec | 1w | PO clarifies |

## Sprint Planning Output

```markdown
## Sprint N Backlog

**Goal**: [1 sentence from PO]

**Capacity**: [X] tasks

| ID | Task | Type | Assigned To | State |
|----|------|------|-------------|-------|
| 1 | feature X | frontend | [agent] | Ready |
| 2 | API Y | backend | [agent] | Ready |

**Definition of Done**:
- Unit tests pass
- 2 approvals
- CI green
```

## Sprint Review Output

```markdown
## Sprint N Review

**Goal**: [met | partially met | not met]
**Completed**: [X] / [Y] tasks

**What Shipped**:
- Task 1 → [link]
- Task 2 → [link]

**Carry-over**:
- Task 3: [reason]

**Metrics**:
- Velocity: [X] tasks
- Blocker count: [N]
```

## Role Reference

### Sprint Master (agents/sprint-master.md)
Coordinates sprints, tracks metrics, removes blockers.

### Product Owner (agents/product-owner.md)
Defines sprint goal, prioritizes backlog, clarifies scope.

### Developer Agent (agents/developer-agent.md)
Executes tasks autonomously using TDD.

### QA Agent (agents/qa-agent.md)
Verifies PRs, ensures test coverage ≥80%.

### Code Reviewer (agents/code-reviewer.md)
Second approval gate, reviews for correctness/security.
