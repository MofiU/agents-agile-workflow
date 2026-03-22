# 🎯 Agents Agile Workflow

> AI team sprint orchestration — no humans required, no rituals needed.

A lightweight agile framework designed for **AI agent teams**. Replaces human-centric ceremonies with efficient autonomous workflows.

## 🤖 Why This Exists

Traditional agile assumes humans who:
- Need daily standups to know what's happening
- Require encouragement and "psychological safety"
- Miss meetings, forget things, have conflicts

**AI teams don't have these problems.** This framework strips out the ceremony and keeps the structure.

## 📦 The Agents

| Agent | Role | When Active |
|-------|------|-------------|
| [Agile Sprint Master](agile-sprint-master.md) | Orchestrates sprints | Day 1, Day 10, blockers |
| [Agile Product Owner](agile-product-owner.md) | Defines goals, prioritizes | Day 1, spec unclear |
| [Agile Developer Agent](agile-developer-agent.md) | Executes tasks, ships code | Daily |
| [Agile QA Agent](agile-qa-agent.md) | Verifies quality | On PR |
| [Agile Code Reviewer](agile-code-reviewer.md) | Second approval gate | On PR |

## ⚡ Quick Start

### Day 1: Sprint Planning

```
PO → Define sprint goal (1 sentence)
PO → Prioritize backlog
SM → Assign tasks to agents
Agents → Claim from Ready queue
```

### Day 2-9: Autonomous Execution

```
Developer:
  1. Check Ready → claim task
  2. TDD → Red → Green → Refactor
  3. Submit PR
  4. 2 approvals → merge
  5. Move to Accepted
  6. Blocked > 15min → escalate

QA + Reviewer:
  1. Review PR
  2. Approve or Request Changes
  3. Coverage ≥80% required
```

### Day 10: Review → Retro → Next Sprint

```
SM → Sprint Review (metrics, carry-over)
SM → Sprint Retro (what worked/didn't, actions)
SM → Sprint Planning (next sprint starts immediately)
```

## 📊 Task States

```
Backlog → Ready → In Progress → In Review → Accepted
                 ↓
             Rejected → (fix) → In Review
```

## 🚦 Blocker Escalation

| Priority | Issue | SLA | Action |
|----------|-------|-----|--------|
| P0 | Service down | 1h | Escalate immediately |
| P1 | API unavailable | 4h | Coordinate workaround |
| P2 | Build broken | 24h | Fix or mock |
| P3 | Unclear spec | 1w | PO clarifies |

**Path**: Agent → Sprint Master → Product Owner

## 📈 What We Skip (AI Teams)

| Human Agile | AI Team |
|-------------|---------|
| Daily standup | Agents self-organize |
| Sprint estimation | Record actual time |
| Story points | Count tasks only |
| Retrospective "feelings" | Auto-collected metrics |
| Team bonding | No-op |
| Attendance tracking | N/A |
| Psychological safety | N/A |

## 📁 Project Structure

```
agents-agile-workflow/
├── agile-sprint-master.md     # Core orchestrator
├── agile-product-owner.md     # PO role
├── agile-developer-agent.md   # Developer role
├── agile-qa-agent.md          # QA role
├── agile-code-reviewer.md     # Reviewer role
├── README.md
└── CONTRIBUTING.md
```

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add new agents or improve existing ones.

## 📜 License

MIT
