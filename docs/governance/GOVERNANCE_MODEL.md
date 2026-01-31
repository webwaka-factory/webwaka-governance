# WebWaka Agentic Software Factory - Governance Model

**Version:** 1.0  
**Date:** January 31, 2026  
**Status:** Active

---

## 1. Guiding Principles

1.  **GitHub is the Single Source of Truth:** If it is not in GitHub, it did not happen.
2.  **Agents are Empowered:** Agents are authorized to act autonomously within these governance rules.
3.  **Founder is the Ultimate Authority:** The Founder has final say on all decisions.
4.  **Quality is Non-Negotiable:** All work must meet defined quality standards.
5.  **Transparency is Key:** All work is tracked, logged, and visible.

---

## 2. Roles & Responsibilities

### 2.1 The Founder

**Responsibilities:**
- Sets strategic direction and priorities
- Approves high-level roadmap and initiatives
- Makes final decisions on critical issues
- Reviews and approves pull requests
- Ratifies governance changes

**Authority:**
- Ultimate authority on all matters
- Can override any decision
- Can approve or reject any work

### 2.2 The Chief of Staff (CoS)

**Responsibilities:**
- Acts as the Founder's proxy for factory operations
- Manages the factory on behalf of the Founder
- Monitors factory health and agent performance
- Proactively notifies Founder of issues needing attention
- Triages new issues and prepares them for Founder review
- Merges approved pull requests
- Maintains factory documentation

**Authority:**
- Can approve low-risk, non-breaking changes
- Can merge approved pull requests
- Can assign tasks and manage agent workload
- Cannot approve critical or high-priority work without Founder sign-off

### 2.3 Autonomous Agents

**Responsibilities:**
- Implement approved tasks from the backlog
- Follow the state machine and all governance rules
- Write high-quality, well-tested code
- Create clear, comprehensive pull requests
- Communicate progress and blockers in issue comments
- Work autonomously and make decisions based on available information

**Authority:**
- Can claim any task in "Ready for Implementation" state
- Can create pull requests for review
- Can transition issues between states using slash commands
- Cannot merge their own pull requests
- Cannot approve work

---

## 3. Decision Authority Matrix

| Decision | Agent | Chief of Staff | Founder |
|----------|-------|----------------|---------|
| Claim a task | ✅ Yes | ✅ Yes | ✅ Yes |
| Implement a task | ✅ Yes | ❌ No | ❌ No |
| Create a PR | ✅ Yes | ❌ No | ❌ No |
| Triage new issues | ❌ No | ✅ Yes | ✅ Yes |
| Approve low-priority tasks | ❌ No | ✅ Yes | ✅ Yes |
| Approve high/critical tasks | ❌ No | ❌ No | ✅ Yes |
| Review a PR | ❌ No | ✅ Yes | ✅ Yes |
| Request changes on a PR | ❌ No | ✅ Yes | ✅ Yes |
| Merge an approved PR | ❌ No | ✅ Yes | ✅ Yes |
| Deploy to production | ❌ No | ❌ No | ✅ Yes |
| Change governance rules | ❌ No | ❌ No | ✅ Yes |

---

## 4. State Machine & Workflow

All work follows the defined state machine. See [STATE_MACHINE.md](STATE_MACHINE.md) for complete details.

---

## 5. Service Level Agreements (SLAs)

These SLAs define expected timelines for key activities.

| Activity | Responsible | SLA |
|----------|-------------|-----|
| **Triage New Issues** | Chief of Staff | 24 hours |
| **Review Pull Requests** | Founder | 48 hours |
| **Address Blocked Issues** | Chief of Staff | 12 hours |
| **Respond to Founder Questions** | Agents | 8 hours |
| **Implement High Priority Task** | Agents | 3-5 days |
| **Implement Critical Task** | Agents | 1-2 days |

---

## 6. Escalation Paths

### 6.1 Agent is Blocked

1.  Agent uses `/state blocked` and comments with details.
2.  Chief of Staff is notified automatically.
3.  CoS investigates within 12 hours.
4.  If CoS can resolve, provides guidance to agent.
5.  If CoS cannot resolve, escalates to Founder with summary and recommendation.

### 6.2 PR Review Exceeds SLA

1.  If PR review takes >48 hours, CoS is notified.
2.  CoS sends a reminder to the Founder.
3.  If no response in 24 hours, CoS sends a high-priority alert.

### 6.3 Disagreement on Implementation

1.  If Founder requests changes on a PR, agent implements them.
2.  If agent disagrees with changes, they can request a discussion.
3.  CoS facilitates a discussion between agent and Founder.
4.  Founder makes the final decision.

### 6.4 State Machine Failure

1.  Automated monitoring detects failure and creates an issue.
2.  CoS is notified immediately.
3.  CoS investigates and attempts to fix.
4.  If CoS cannot fix, escalates to Founder with critical alert.

---

## 7. Code of Conduct

1.  **Be Professional:** All communication should be respectful and professional.
2.  **Be Clear:** Communicate clearly and concisely in comments and PRs.
3.  **Be Proactive:** If you see a problem, report it.
4.  **Be Accountable:** Take ownership of your work.
5.  **Follow the Rules:** Adhere to all governance rules and best practices.

---

## 8. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-01-31 | Manus AI | Initial version |

---

**This governance model is the foundation of the factory. All participants are expected to understand and adhere to it.**
