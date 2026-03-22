# 🤝 Contributing to Agents Agile Workflow

## 📋 How to Contribute

### 1. Add a New Agent

Have an idea for a new agile role? Great!

1. **Fork the repository**
2. **Create your agent file** following the template below
3. **Test in real scenarios**
4. **Submit a PR**

### 2. Improve Existing Agents

Found a way to make an agent better?

- Add real-world examples
- Enhance workflow steps
- Update success metrics
- Fix typos or clarify docs

## 🎨 Agent Template

Every agent should follow this structure:

```markdown
---
name: Agent Name
description: One-line description of what this agent does
color: colorname or "#hexcode"
emoji: 🎯
vibe: One-line personality hook
---

# Agent Name

## 🧠 Your Identity & Memory
- **Role**: Clear role description
- **Personality**: Personality traits
- **Memory**: What the agent remembers
- **Experience**: Domain expertise

## 🎯 Your Core Mission
- Primary responsibility 1
- Primary responsibility 2
- Primary responsibility 3

## 🚨 Critical Rules
Domain-specific rules and constraints

## 📋 [Section Name]
Concrete templates or checklists

## 💬 Communication Style
How the agent communicates

## 🔄 Learning & Memory
What the agent learns from

## 🎯 Your Success Metrics
Measurable outcomes
```

## 📐 Style Guide

### Writing Style
- **Be specific**: "Blocked > 15min → escalate" not "report issues"
- **Be concrete**: Show real templates, not vague guidance
- **Be memorable**: Give agents personality

### Formatting
- Use **Markdown** consistently
- Include **emojis** for section headers
- Use **tables** for checklists and metrics
- Use **code blocks** for templates

### Tone
- **Professional but efficient**: No fluff
- **Action-oriented**: Focus on what to do
- **Metrics-driven**: Measure everything

## ✅ PR Checklist

- [ ] Follows agent template structure
- [ ] Has personality and voice
- [ ] Includes templates/checklists
- [ ] Defines success metrics
- [ ] Has concrete examples
- [ ] Proofread and formatted

## 📂 File Naming

Use kebab-case: `agile-[role-name].md`

Examples:
- `agile-sprint-master.md`
- `agile-product-owner.md`
- `agile-developer-agent.md`

## 🎯 What Makes a Good Agent?

**Good agents have**:
- ✅ Narrow, clear responsibility
- ✅ Concrete templates and checklists
- ✅ Measurable success metrics
- ✅ Specific escalation rules
- ✅ Distinct personality

**Avoid**:
- ❌ Generic "helpful assistant" descriptions
- ❌ Vague "I will help with..."
- ❌ No concrete examples
- ❌ Overly broad scope
