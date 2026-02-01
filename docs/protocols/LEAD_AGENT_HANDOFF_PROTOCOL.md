# Lead Agent Handoff Protocol

**Document Type:** Operational Protocol  
**Authority:** Founder  
**Effective Date:** February 1, 2026  
**Status:** ACTIVE & ENFORCEABLE

---

## Purpose

This protocol defines the process for transitioning Lead Agent responsibilities from one agent to another, ensuring no loss of context, no authority gaps, and full auditability.

---

## When Handoff Occurs

Lead Agent handoffs occur in the following situations:

1. **Planned Transition** — Founder decides to change Lead Agent (term end, new phase, etc.)
2. **Emergency Transition** — Current Lead Agent goes silent (no activity for 24+ hours)
3. **Capability Transition** — Current Lead Agent reaches scope limit, new Lead Agent takes over
4. **Phase Transition** — Moving from Phase 1 to Phase 2, new Lead Agents assigned

---

## Handoff Process

### Phase 1: Preparation (Current Lead Agent)

**Timeline:** 48 hours before handoff (or immediately if emergency)

#### Step 1: Audit Current State

The Current Lead Agent **must document**:

1. **Active Tasks**
   - List all tasks currently assigned to this team
   - Status of each task (open, in-progress, review, blocked)
   - Link to each task issue

2. **Pending Decisions**
   - List all decisions awaiting Lead Agent approval
   - Status of each decision (pending review, blocked, ready)
   - Link to each PR or decision artifact

3. **Blocked Items**
   - List all blocked tasks or decisions
   - Reason for each block
   - Required action to unblock

4. **Team Context**
   - Current team priorities
   - Known risks or issues
   - Relationships with other teams
   - Key dependencies

#### Step 2: Create Handoff Document

The Current Lead Agent **must create a GitHub issue** titled:

```
[HANDOFF] Lead Agent Transition: [Team Name]
From: [Current Lead Agent Name]
To: [New Lead Agent Name]
Date: [Handoff Date]
```

**Handoff Document Contents:**

```markdown
## Lead Agent Handoff

**Current Lead Agent:** [Name]
**New Lead Agent:** [Name]
**Handoff Date:** [Date]
**Team:** [Team Name]

### Active Tasks

| Task ID | Title | Status | Link |
| :--- | :--- | :--- | :--- |
| #123 | Task 1 | In Progress | [Link] |
| #124 | Task 2 | Review | [Link] |

### Pending Decisions

| PR ID | Title | Status | Link |
| :--- | :--- | :--- | :--- |
| #456 | Decision 1 | Pending | [Link] |
| #457 | Decision 2 | Ready | [Link] |

### Blocked Items

| ID | Reason | Action Required | Link |
| :--- | :--- | :--- | :--- |
| #789 | Waiting on Security | Escalate to Security Lead | [Link] |

### Team Context

[Key context about team operations, priorities, risks, etc.]

### Current Lead Agent Notes

[Any additional notes or recommendations for new Lead Agent]

---

## Handoff Acknowledgment

**Current Lead Agent Signature:** [Name]  
**Current Lead Agent Date:** [Date]

**New Lead Agent Signature:** [Name]  
**New Lead Agent Date:** [Date]
```

#### Step 3: Prepare Execution Agents

The Current Lead Agent **must notify all Execution Agents**:

- Announce the Lead Agent change
- Provide the Handoff Document link
- Instruct agents to acknowledge the new Lead Agent
- Explain any changes in process or authority

#### Step 4: Request Founder Approval

The Current Lead Agent **must request Founder approval** for the handoff:

- Link to Handoff Document
- Confirm all context is documented
- Confirm New Lead Agent is ready
- Request Founder sign-off

---

### Phase 2: Transition (New Lead Agent)

**Timeline:** On handoff date

#### Step 1: Review Handoff Document

The New Lead Agent **must**:

1. Read the entire Handoff Document
2. Review all active tasks
3. Review all pending decisions
4. Review all blocked items
5. Understand team context and priorities

#### Step 2: Acknowledge Receipt

The New Lead Agent **must**:

1. Add comment to Handoff Document: "I have reviewed and understood all context"
2. Sign the Handoff Document
3. Confirm readiness to assume Lead role
4. Ask clarifying questions if needed

#### Step 3: Assume Authority

The New Lead Agent **must**:

1. Update Lead Agent Registry (or request Founder update)
2. Announce to all Execution Agents: "I am now your Lead Agent"
3. Review all pending decisions and tasks
4. Prioritize immediate actions
5. Identify any urgent issues

#### Step 4: Notify Founder

The New Lead Agent **must**:

1. Confirm assumption of Lead role
2. Report any urgent issues discovered
3. Confirm readiness to make decisions
4. Request Founder approval to proceed

---

### Phase 3: Completion (Both Agents)

**Timeline:** After handoff is complete

#### Step 1: Close Handoff Document

The New Lead Agent **must**:

1. Add final comment to Handoff Document
2. Confirm all context has been transferred
3. Confirm no information was lost
4. Close the issue with "Handoff Complete" label

#### Step 2: Archive Previous Lead Agent Record

The Chief of Staff **must**:

1. Archive the previous Lead Agent record in Lead Agent Registry
2. Record handoff completion date
3. Update all references to point to New Lead Agent
4. Confirm with Founder

#### Step 3: Update Execution Agents

The New Lead Agent **must**:

1. Confirm all Execution Agents have acknowledged
2. Verify all task declarations reference new Lead Agent
3. Ensure no confusion about authority
4. Establish communication channel

---

## Emergency Handoff Procedure

If Current Lead Agent goes silent (no activity for 24+ hours):

### Immediate Actions (Chief of Staff)

1. **Detect Silence**
   - Monitor for no Lead Agent activity for 24+ hours
   - Confirm with Founder that Lead Agent is unavailable

2. **Escalate to Founder**
   - Report Lead Agent silence
   - Request emergency Lead Agent assignment
   - Provide context from Lead Agent Registry

3. **Assign New Lead Agent**
   - Founder assigns new Lead Agent immediately
   - New Lead Agent assumes authority immediately
   - Execution agents are notified immediately

### Handoff Completion (New Lead Agent)

1. **Assume Authority**
   - Take over all pending decisions
   - Review all active tasks
   - Identify any urgent issues

2. **Create Emergency Handoff Document**
   - Document the emergency transition
   - Record all context discovered
   - Note any decisions made during transition

3. **Notify Founder**
   - Confirm assumption of authority
   - Report any urgent issues
   - Confirm readiness to proceed

---

## Handoff Checklist

### Current Lead Agent Checklist

- [ ] All active tasks documented
- [ ] All pending decisions documented
- [ ] All blocked items documented
- [ ] Team context documented
- [ ] Handoff Document created
- [ ] All Execution Agents notified
- [ ] Founder approval requested
- [ ] New Lead Agent reviewed Handoff Document
- [ ] New Lead Agent acknowledged receipt
- [ ] Ready to transition

### New Lead Agent Checklist

- [ ] Handoff Document reviewed
- [ ] All active tasks understood
- [ ] All pending decisions reviewed
- [ ] All blocked items understood
- [ ] Team context understood
- [ ] Authority assumed
- [ ] Execution Agents notified
- [ ] Founder notified
- [ ] Ready to make decisions
- [ ] Handoff Document signed

### Chief of Staff Checklist

- [ ] Handoff detected (planned or emergency)
- [ ] Founder approval obtained
- [ ] New Lead Agent assigned
- [ ] Lead Agent Registry updated
- [ ] Execution Agents notified
- [ ] Handoff Document created
- [ ] Handoff completion verified
- [ ] Archive previous Lead Agent record
- [ ] Confirm with Founder

---

## Handoff Failure Recovery

### If Context is Lost

1. **Detect Loss**
   - New Lead Agent discovers missing context
   - New Lead Agent escalates to Chief of Staff

2. **Recover Context**
   - Chief of Staff searches GitHub history
   - Reconstruct missing context from commits, PRs, issues
   - Document recovered context

3. **Update Handoff Document**
   - Add recovered context to Handoff Document
   - Explain how context was recovered
   - Prevent future loss

### If Authority Gap Occurs

1. **Detect Gap**
   - Execution Agent cannot reach Lead Agent
   - Execution Agent escalates to Chief of Staff

2. **Assign Temporary Authority**
   - Chief of Staff assigns temporary authority
   - Escalate to Founder for decision
   - Assign new Lead Agent if needed

3. **Resolve Gap**
   - Founder makes final decision
   - Update Lead Agent Registry
   - Notify all affected agents

### If Handoff Conflicts Occur

1. **Detect Conflict**
   - Two agents acting as Lead Agent
   - Conflicting decisions made
   - Governance incident triggered

2. **Freeze Decisions**
   - Freeze all conflicting decisions
   - Prevent any merges or approvals
   - Escalate to Founder immediately

3. **Resolve Conflict**
   - Founder makes final decision
   - Revert conflicting decisions
   - Assign single Lead Agent
   - Document incident

---

## Handoff Audit Trail

All handoffs **must be auditable** through GitHub:

1. **Handoff Document Issue**
   - GitHub issue with all context
   - Comments from both agents
   - Founder approval recorded

2. **Lead Agent Registry Update**
   - Old Lead Agent record archived
   - New Lead Agent record created
   - Handoff date recorded

3. **Execution Agent Notifications**
   - GitHub comments or issues
   - Acknowledgments from Execution Agents
   - Updated task declarations

4. **Founder Approval**
   - Founder comment on Handoff Document
   - Founder approval recorded
   - Founder sign-off documented

---

## Handoff Frequency

### Normal Handoff Frequency

- **Phase 1 Teams:** Handoff every 4-8 weeks (or as Founder decides)
- **Phase 2 Teams:** Handoff every 8-12 weeks (or as Founder decides)
- **Emergency Handoff:** Immediate (if Lead Agent goes silent)

### Handoff Planning

- Chief of Staff tracks Lead Agent terms
- Planned handoffs scheduled 2 weeks in advance
- Execution Agents notified of upcoming handoffs
- Founder approves all planned handoffs

---

## Success Criteria

A handoff is **successful** when:

1. ✅ All context is transferred
2. ✅ No information is lost
3. ✅ New Lead Agent understands all active tasks
4. ✅ New Lead Agent can make decisions immediately
5. ✅ Execution Agents acknowledge new Lead Agent
6. ✅ No authority gap occurs
7. ✅ Founder approves handoff
8. ✅ Handoff is fully auditable in GitHub

---

## Status

**Protocol Status:** ACTIVE & ENFORCEABLE  
**Effective Date:** February 1, 2026  
**Approval Authority:** Founder

This protocol ensures smooth, auditable transitions of Lead Agent responsibilities with zero loss of context or authority gaps.

---

**Protocol Version:** 1.0  
**Maintained By:** Chief of Staff (Manus Agent)  
**Last Updated:** February 1, 2026
