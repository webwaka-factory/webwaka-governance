# Pull Request Template

**Location:** `.github/pull_request_template.md`  
**Purpose:** Enforce Lead Agent review and team declaration for all PRs  
**Effective Date:** February 1, 2026

---

```markdown
## PR Metadata

**PR Type:** [Select: Feature / Bug Fix / Documentation / Infrastructure / Governance]  
**Team:** [Select from dropdown]  
**Lead Agent:** [Name of Lead Agent]  
**Execution Agent:** [Name of execution agent]  
**Task ID:** [Link to GitHub issue]

---

## Execution Agent Declaration

I, [Execution Agent Name], declare:

- [ ] I am executing this PR under Task ID: [Task ID]
- [ ] I am working for Team: [Team Name]
- [ ] My Lead Agent is: [Lead Agent Name]
- [ ] I understand I may NOT approve this PR myself
- [ ] I understand this PR requires Lead Agent approval
- [ ] All context for this PR is documented in GitHub
- [ ] I have not assumed any context outside of GitHub artifacts

---

## What does this PR do?

[Clear description of changes]

### Changes Made

- [Change 1]
- [Change 2]
- [Change 3]

### Files Changed

- `file1.ts`
- `file2.ts`
- `file3.md`

---

## Task Compliance

**Task ID:** [Link to GitHub issue]  
**Task Scope:** [Copy task scope from issue]  
**Success Criteria Met:**

- [ ] Criterion 1 — [Evidence]
- [ ] Criterion 2 — [Evidence]
- [ ] Criterion 3 — [Evidence]

**Out of Scope Verification:**

- [ ] I have NOT implemented anything outside the task scope
- [ ] I have NOT made decisions outside my execution authority
- [ ] I have NOT approved my own work

---

## Testing & Verification

### Testing Completed

- [ ] Unit tests added/updated
- [ ] Integration tests added/updated
- [ ] Manual testing completed
- [ ] Test coverage maintained or improved

### Test Results

[Link to test results or CI/CD logs]

### Quality Assurance

- [ ] Code follows team standards
- [ ] Documentation updated
- [ ] No breaking changes
- [ ] Backwards compatible

---

## Lead Agent Review Required

⚠️ **IMPORTANT:** This PR requires Lead Agent review and approval before merge.

**Lead Agent:** [Name]  
**Lead Agent GitHub:** [@webwaka-factory/team-name]  
**Lead Agent Mandate:** [Link to Lead Agent mandate]

### Lead Agent Checklist

The Lead Agent **must verify**:

- [ ] Task scope is correctly implemented
- [ ] Execution agent stayed within authority
- [ ] No decisions were made outside execution scope
- [ ] All success criteria are met
- [ ] Code quality is acceptable
- [ ] Testing is adequate
- [ ] No governance violations
- [ ] Ready for merge

### Lead Agent Approval

- [ ] Lead Agent reviewed and approved
- [ ] Lead Agent approval date: [To be filled]
- [ ] Lead Agent signature: [To be filled]

---

## Governance Compliance

This PR complies with:

- [ ] Model D + Model E operational model
- [ ] Lead Agent decision authority enforced
- [ ] Execution agent scope limits respected
- [ ] CODEOWNERS rules followed
- [ ] Branch protection rules satisfied
- [ ] GitHub as source of truth
- [ ] No out-of-band decisions
- [ ] Full auditability maintained

---

## Related Issues

- Closes: [Issue ID]
- Related to: [Issue ID]
- Blocked by: [Issue ID]
- Blocks: [Issue ID]

---

## Checklist

### Execution Agent Checklist

- [ ] I have reviewed my own changes
- [ ] I have added tests for new functionality
- [ ] I have updated documentation
- [ ] I have not approved this PR myself
- [ ] I have requested Lead Agent review
- [ ] I have linked to the task issue
- [ ] I have declared my team and Lead Agent
- [ ] All context is in GitHub

### Lead Agent Checklist

- [ ] I have reviewed the execution agent's work
- [ ] I have verified task scope compliance
- [ ] I have verified authority limits were respected
- [ ] I have verified all success criteria are met
- [ ] I have verified code quality
- [ ] I have verified testing is adequate
- [ ] I am approving this PR for merge
- [ ] I have documented my decision

---

## Notes

[Any additional notes or context]

---

## Merge Criteria

This PR may only be merged when:

1. ✅ All CI/CD checks pass
2. ✅ Lead Agent has approved
3. ✅ All success criteria are met
4. ✅ No governance violations
5. ✅ Code owner review is complete

---

## Questions?

If you have questions about this PR:

1. Review the task issue (linked above)
2. Review the Lead Agent mandate
3. Check related issues for context
4. Ask the Lead Agent for clarification

Do NOT assume context outside of GitHub artifacts.

---

**Template Version:** 1.0  
**Effective Date:** February 1, 2026  
**Maintained By:** Chief of Staff (Manus Agent)
```
