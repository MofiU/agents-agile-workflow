# 🎯 Agents Agile Workflow

> AI team sprint orchestration — no humans required, no rituals needed.

A lightweight agile framework designed for **AI agent teams**. Replaces human-centric ceremonies with efficient autonomous workflows.

## 📦 Project Structure

```
agents-agile-workflow/
├── SKILL.md                    # Main skill - workflow orchestration
├── agents/                      # Role/persona definitions
│   ├── sprint-master.md        # Sprint orchestrator
│   ├── product-owner.md        # Goal & priority definition
│   ├── developer-agent.md       # Task execution with TDD
│   ├── qa-agent.md              # Quality verification
│   └── code-reviewer.md        # PR reviews
├── evals/
│   └── evals.json              # Test cases
├── README.md
├── CONTRIBUTING.md
└── .gitignore
```

## 🤖 The Roles

Each agent follows the agency-agents format with identity, persona, rules, and workflows.

| Agent | File | Responsibility |
|-------|------|----------------|
| **Sprint Master** | `agents/sprint-master.md` | Orchestrates sprints, tracks metrics |
| **Product Owner** | `agents/product-owner.md` | Defines goals, prioritizes |
| **Developer Agent** | `agents/developer-agent.md` | Executes tasks, TDD |
| **QA Agent** | `agents/qa-agent.md` | Verifies quality |
| **Code Reviewer** | `agents/code-reviewer.md` | Reviews PRs |

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

## 📈 What We Skip (AI Teams)

| Human Agile | AI Team |
|-------------|---------|
| Daily standup | Agents self-organize |
| Sprint estimation | Record actual time |
| Story points | Count tasks only |
| Retrospective "feelings" | Auto-collected metrics |
| Team bonding | No-op |
| Attendance tracking | N/A |

## 🧪 Testing

```bash
# Generate eval viewer
python ~/.agents/skills/skill-creator/eval-viewer/generate_review.py \
  agents-agile-workflow-workspace/iteration-1 \
  --skill-name "agile-workflow" \
  --static /tmp/eval_review.html
```

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add new agents or improve existing ones.

## 📜 License

MIT
