# Agent Identification System

**Version:** 1.0  
**Date:** January 31, 2026  
**Status:** Implemented

---

## Overview

The Agent Identification System assigns unique identifiers to each agent working in the factory. This enables better tracking, prevents duplicate claims, and improves observability.

---

## Agent ID Format

Each agent is assigned a unique identifier in the format: `agent-<number>`

**Examples:**
- `agent-1`
- `agent-2`
- `agent-3`

---

## How It Works

### 1. Agent Registration

When deploying a new agent, assign it a unique agent ID:

**In the agent prompt:**
```
AGENT IDENTIFICATION:
- Your unique agent ID is: agent-1
- Include this ID in all comments and commits
- Use this format: "[agent-1] Your message here"
```

### 2. Agent Comments

All agent comments on issues should include the agent ID:

**Format:**
```
[agent-1] I am claiming this task.
[agent-1] Implementation complete. PR created: #27
[agent-1] Blocked on dependency. Need help with X.
```

### 3. Git Commits

All commits by agents should include the agent ID in the commit message:

**Format:**
```
[agent-1] feat: Implement CS-3 IAM test suite

- Added comprehensive test coverage
- Implemented all acceptance criteria
```

### 4. Activity Logging

The activity logging system automatically captures agent IDs from comments and commits, enabling:
- Per-agent activity tracking
- Workload distribution analysis
- Performance metrics

---

## Benefits

### Prevents Duplicate Claims

**Before Agent IDs:**
- Multiple agents could claim the same task
- No way to distinguish between agents
- Race conditions were common

**With Agent IDs:**
- Each agent has a unique identifier
- Activity log shows which agent claimed what
- Duplicate claims are easily detected

### Improves Observability

**Tracking:**
- See which agent is working on which task
- Identify high-performing agents
- Detect inactive agents

**Analytics:**
- Tasks completed per agent
- Average time per task per agent
- Success rate per agent

### Better Debugging

**When issues occur:**
- Identify which agent caused the issue
- Review that agent's activity history
- Understand agent behavior patterns

---

## Agent Registry

| Agent ID | Status | Deployed | Last Activity |
|----------|--------|----------|---------------|
| agent-1 | Active | 2026-01-31 | 2026-01-31 |
| agent-2 | Active | 2026-01-31 | 2026-01-31 |
| agent-3 | Active | 2026-01-31 | 2026-01-31 |

---

## Implementation

### For New Agents

When deploying a new development agent:

1. **Assign the next available agent ID** (e.g., `agent-4`)
2. **Update the agent prompt** to include the agent ID
3. **Register the agent** in this document
4. **Deploy the agent** with the updated prompt

### For Existing Agents

To update existing agents:

1. **Stop the agent** (let it complete current task)
2. **Update the prompt** with an agent ID
3. **Redeploy the agent**

---

## Agent Prompt Template

Add this section to all autonomous agent prompts:

```markdown
## AGENT IDENTIFICATION

**Your unique agent ID is: agent-X**

You MUST include your agent ID in all interactions:

1. **In all comments:** Start with `[agent-X]`
   - Example: `[agent-X] I am claiming this task.`

2. **In all commits:** Include `[agent-X]` in commit messages
   - Example: `[agent-X] feat: Implement feature`

3. **When logging activity:** Always provide your agent ID
   - The logging system will track your activities

This identification system:
- Prevents duplicate work
- Enables performance tracking
- Improves debugging
- Provides accountability
```

---

## Monitoring Agent Activity

### View Activity for a Specific Agent

```bash
python3 scripts/log_agent_activity.py --agent agent-1
```

### View All Agent Activity

```bash
cat logs/activity_log.jsonl | grep agent-1
```

### Generate Agent Performance Report

```bash
python3 scripts/generate_agent_report.py agent-1
```

---

## Best Practices

**Do:**
- Assign sequential agent IDs (agent-1, agent-2, agent-3...)
- Include agent ID in all comments and commits
- Register new agents in this document
- Monitor agent activity regularly

**Don't:**
- Reuse agent IDs for different agents
- Deploy agents without agent IDs
- Skip agent ID in comments or commits
- Deploy too many agents without monitoring

---

## Troubleshooting

**Issue: Agent not including ID in comments**
- Check the agent prompt includes the identification section
- Verify the agent is using the updated prompt
- Redeploy the agent if needed

**Issue: Duplicate agent IDs**
- Check the agent registry for conflicts
- Assign a new unique ID to the duplicate agent
- Update the agent prompt and redeploy

---

**Agent identification is critical for factory operations. Always use agent IDs.**
