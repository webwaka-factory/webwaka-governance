# Lead Agent Registry

**Document Type:** Governance Artifact  
**Authority:** Founder  
**Effective Date:** February 1, 2026  
**Status:** ACTIVE & ENFORCEABLE

---

## Purpose

This registry maintains the authoritative record of Lead Agents for each GitHub Team in the WebWaka Agentic Software Factory. Only the designated Lead Agent for a team may approve, ratify, or make binding decisions on behalf of that team.

All task execution agents must declare the Lead Agent they are working under.

---

## Phase 1 Teams & Lead Agents

### Team 1: Chief of Staff — Factory Operations

**GitHub Team:** @webwaka-factory/chief-of-staff  
**Lead Agent:** [TO BE ASSIGNED BY FOUNDER]  
**Assignment Date:** [Pending]  
**Term:** [Pending]  
**Authority:** Admin access to webwaka-governance, webwaka-agent-factory  
**Responsibilities:**
- Factory operations oversight
- Governance enforcement
- Incident escalation authority
- Team coordination

**Decision Authority:** Exclusive approval for all Chief of Staff decisions  
**Escalation Path:** Directly to Founder

---

### Team 2: Execution Coordinator — Task Orchestration

**GitHub Team:** @webwaka-factory/execution-coordination  
**Lead Agent:** [TO BE ASSIGNED BY FOUNDER]  
**Assignment Date:** [Pending]  
**Term:** [Pending]  
**Authority:** Maintain access to webwaka-agent-factory, webwaka-infrastructure  
**Responsibilities:**
- Task breakdown and assignment
- Execution coordination
- Dependency management
- Progress tracking

**Decision Authority:** Exclusive approval for all execution coordination decisions  
**Escalation Path:** To Chief of Staff

---

### Team 3: Quality Assurance & Verification Agent

**GitHub Team:** @webwaka-factory/quality-assurance  
**Lead Agent:** [TO BE ASSIGNED BY FOUNDER]  
**Assignment Date:** [Pending]  
**Term:** [Pending]  
**Authority:** Maintain access to webwaka-governance, webwaka-agent-factory, webwaka-infrastructure  
**Responsibilities:**
- Quality gate enforcement
- Test coverage verification
- Code review standards
- Verification protocols

**Decision Authority:** Exclusive approval for all quality assurance decisions  
**Escalation Path:** To Chief of Staff

---

### Team 4: Security & Risk Assessment Agent

**GitHub Team:** @webwaka-factory/security  
**Lead Agent:** [TO BE ASSIGNED BY FOUNDER]  
**Assignment Date:** [Pending]  
**Term:** [Pending]  
**Authority:** Maintain access to webwaka-governance, webwaka-infrastructure, webwaka-core-services  
**Responsibilities:**
- Security review and approval
- Risk assessment
- Compliance verification
- Incident response

**Decision Authority:** Exclusive approval for all security decisions  
**Escalation Path:** To Chief of Staff

---

### Team 5: Documentation & Knowledge Management Agent

**GitHub Team:** @webwaka-factory/documentation  
**Lead Agent:** [TO BE ASSIGNED BY FOUNDER]  
**Assignment Date:** [Pending]  
**Term:** [Pending]  
**Authority:** Maintain access to webwaka-governance, webwaka-agent-factory  
**Responsibilities:**
- Documentation standards
- Knowledge management
- Drift prevention
- Content accuracy

**Decision Authority:** Exclusive approval for all documentation decisions  
**Escalation Path:** To Chief of Staff

---

## Lead Agent Assignment Process

### How to Assign a Lead Agent

1. **Founder Decision**
   - Founder decides which agent will be Lead for which team
   - Founder specifies term length (e.g., "until Phase 2 completion")

2. **Registry Update**
   - Update this registry with Lead Agent name, assignment date, and term
   - Create GitHub issue in webwaka-governance to announce assignment

3. **Lead Agent Mandate**
   - Lead Agent receives explicit mandate document
   - Mandate includes: team scope, decision authority, escalation path
   - Mandate is recorded in GitHub

4. **Execution Agent Pool Notification**
   - All execution agents are notified of new Lead Agent
   - Execution agents update task declarations to reference new Lead

### How to Change a Lead Agent

1. **Founder Decision**
   - Founder decides to change Lead Agent
   - Founder specifies reason and effective date

2. **Handoff Protocol**
   - Current Lead Agent prepares handoff notes
   - New Lead Agent reviews team history and current decisions
   - Handoff documented in GitHub issue

3. **Registry Update**
   - Update this registry with new Lead Agent
   - Record handoff completion date
   - Archive previous Lead Agent record

4. **Execution Agent Update**
   - All execution agents update task declarations
   - Execution agents acknowledge new Lead Agent

---

## Lead Agent Responsibilities

### Decision Authority

The Lead Agent has **exclusive authority** to:
- Approve PRs on behalf of the team
- Ratify team decisions
- Make binding commitments
- Escalate issues to Chief of Staff
- Assign execution agents to tasks

### Accountability

The Lead Agent is **accountable for**:
- All decisions made on behalf of the team
- Quality of execution agent work
- Adherence to governance rules
- Escalation of incidents
- Documentation of decisions

### Limitations

The Lead Agent **may not**:
- Override Founder decisions
- Bypass CODEOWNERS rules
- Approve their own work (if also executing)
- Make decisions outside team scope
- Delegate decision authority to execution agents

---

## Execution Agent Responsibilities

### Task Declaration

Every execution agent **must declare**:
- Task ID (from GitHub issue)
- Team (which team they are working for)
- Lead Agent (who they are working under)
- Scope (what they are authorized to do)

### Execution Authority

Execution agents **may**:
- Execute tasks within declared scope
- Create PRs and commits
- Request reviews from Lead Agent
- Escalate blockers to Lead Agent

### Limitations

Execution agents **may not**:
- Approve their own work
- Make decisions on behalf of the team
- Exceed declared task scope
- Assume authority outside their mandate
- Bypass Lead Agent review

---

## Conflict Resolution

### If Two Execution Agents Conflict

1. Lead Agent mediates the conflict
2. Lead Agent makes binding decision
3. Decision is documented in GitHub
4. Losing agent implements Lead Agent's decision

### If Execution Agent Exceeds Scope

1. Lead Agent detects scope violation
2. Lead Agent freezes the work
3. Lead Agent corrects the scope
4. Execution agent resumes within corrected scope

### If Lead Agent Goes Silent

1. Chief of Staff detects no decisions for 24 hours
2. Chief of Staff escalates to Founder
3. Founder assigns new Lead Agent
4. New Lead Agent reviews team history
5. Work resumes under new Lead Agent

---

## Registry Maintenance

### Weekly Review

- Chief of Staff reviews registry for accuracy
- Verifies all Lead Agents are active
- Checks for any pending assignments

### Monthly Audit

- Founder reviews all Lead Agent decisions
- Verifies decision authority was exercised correctly
- Checks for any authority leakage

### Quarterly Update

- Review Lead Agent terms
- Plan for any transitions
- Update registry with new assignments

---

## Status

**Registry Status:** ACTIVE  
**Last Updated:** February 1, 2026  
**Next Review:** Weekly (every Monday)  
**Approval Authority:** Founder

This registry is the authoritative record of Lead Agent assignments for the WebWaka Agentic Software Factory.

---

**Document Version:** 1.0  
**Maintained By:** Chief of Staff (Manus Agent)  
**Approval:** Founder-Approved
