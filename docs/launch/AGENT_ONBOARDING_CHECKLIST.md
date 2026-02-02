# Agent Onboarding Checklist

**Document Version:** 1.0  
**Last Updated:** 2026-02-02  
**Status:** ✅ Active

---

## Overview

This checklist serves as the **master source of truth** for agent onboarding in the WebWaka Agentic Software Factory. All agents must complete this checklist before beginning work. The checklist is mandatory and enforced by the Chief of Staff.

**Document Location:** https://github.com/webwaka-factory/webwaka-governance/blob/main/docs/launch/AGENT_ONBOARDING_CHECKLIST.md

---

## Pre-Execution Requirements

Before any agent may execute programmatic GitHub actions, the following prerequisites must be satisfied:

### 1. GitHub Account Setup

- [ ] GitHub account created and active
- [ ] GitHub username assigned (webwakaagent1, webwakaagent2, etc.)
- [ ] Organization membership confirmed: https://github.com/orgs/webwaka-factory/people
- [ ] Team assignment confirmed (check your role assignment prompt)
- [ ] Repository access verified (can access all 7 core repositories)

**Verification:** Navigate to https://github.com/webwaka-factory and confirm you can access the organization and repositories.

### 2. Role Assignment Confirmation

- [ ] Role assignment prompt reviewed and understood
- [ ] Role responsibilities clearly understood
- [ ] Team assignments confirmed
- [ ] Governance invariants (Founder Decisions) reviewed
- [ ] Execution instructions read and acknowledged

**Verification:** Confirm you have read your role-specific prompt:
- Founder: ROLE_ASSIGNMENT_FOUNDER.md
- Chief of Staff: ROLE_ASSIGNMENT_CHIEF_OF_STAFF.md
- Execution Agent: ROLE_ASSIGNMENT_EXECUTION_AGENT.md
- QA Agent: ROLE_ASSIGNMENT_QA_AGENT.md
- Security Agent: ROLE_ASSIGNMENT_SECURITY_AGENT.md

### 3. Founder Decisions Review

- [ ] All Founder Decisions (FD-2026-001 through FD-2026-014) reviewed
- [ ] Founder Decision Index understood: https://github.com/webwaka-factory/webwaka-governance/blob/main/docs/decisions/FOUNDERS_DECISION_INDEX.md
- [ ] Role-specific FDs identified and understood
- [ ] Governance compliance requirements acknowledged

**Verification:** You can explain the key Founder Decisions relevant to your role.

---

## GitHub Personal Access Token (PAT) Setup

**Status:** ✅ MANDATORY  
**Enforcement:** Chief of Staff blocks execution until complete

### When a PAT Is Required

A GitHub Personal Access Token is required for the following activities:

- **GitHub API Access:** Programmatic interactions with GitHub (creating issues, managing PRs, etc.)
- **Programmatic Issue/PR Creation:** Automation that creates or modifies GitHub issues and pull requests
- **Automation & CI Interaction:** Scripts and workflows that interact with GitHub Actions or CI/CD systems
- **Repository Cloning:** Cloning private repositories programmatically
- **Organization Resource Access:** Accessing organization-level resources and settings

### Approved PAT Type

**Fine-Grained Personal Access Tokens ONLY**

| Requirement | Detail |
|:---|:---|
| **Type** | Fine-grained PAT (not classic) |
| **Expiration** | Set expiration date (recommended: 90 days) |
| **Scope** | Limited to specific repositories (if possible) |
| **Regeneration** | Regenerate before expiration |

**Why Fine-Grained?** Fine-grained PATs offer granular permission control, reducing the blast radius if a token is exposed.

### Required Permissions

Your fine-grained PAT must have the following permissions:

| Permission | Access | Justification |
|:---|:---|:---|
| **Contents** | Read/Write | Clone, commit, and push code changes |
| **Pull Requests** | Read/Write | Create, review, and merge pull requests |
| **Issues** | Read/Write | Create, update, and manage GitHub issues |
| **Actions** | Read | View CI/CD workflow status and results |
| **Metadata** | Read | Access repository metadata and information |

### Explicit Prohibitions

The following are **strictly prohibited**:

| Prohibition | Reason |
|:---|:---|
| ❌ **Classic PATs** | Use fine-grained PATs only; classic PATs are deprecated |
| ❌ **Hardcoded Tokens** | Never hardcode PATs in code, scripts, or configuration files |
| ❌ **Committed to GitHub** | Never commit PATs to any repository (violates FD-2026-012) |
| ❌ **Shared Tokens** | Each agent must have their own PAT; never share tokens |
| ❌ **Overly Broad Permissions** | Request only the minimum permissions needed for your role |

### Storage Requirements

Your PAT must be stored securely:

| Storage Method | Status | Details |
|:---|:---|:---|
| **Environment Variables** | ✅ Approved | Store as `GITHUB_PAT` or `GITHUB_TOKEN` in your environment |
| **Local Secrets Store** | ✅ Approved | Use OS-level secrets management (macOS Keychain, Windows Credential Manager, etc.) |
| **CI/CD Secrets** | ✅ Approved | Store in GitHub Actions secrets or CI/CD platform secrets |
| **Hardcoded in Files** | ❌ Prohibited | Never store in code, config files, or scripts |
| **Shared Credentials** | ❌ Prohibited | Never share PATs with other agents or team members |

### Rotation Policy

Your PAT must be rotated according to the following policy:

| Scenario | Action | Timeline |
|:---|:---|:---|
| **Suspected Exposure** | Revoke immediately | Immediate |
| **Accidental Commit** | Revoke immediately | Immediate |
| **Role Removal** | Revoke immediately | Upon role termination |
| **Regular Rotation** | Regenerate | Every 90 days (recommended) |
| **End of Project** | Revoke | Upon project completion |

**Revocation:** To revoke a PAT, navigate to https://github.com/settings/personal-access-tokens and delete the token.

### Verification Step

Before beginning execution, you must verify that your PAT is correctly configured:

**Verification Checklist:**

1. **PAT Created:** Fine-grained PAT has been created at https://github.com/settings/personal-access-tokens
2. **Permissions Set:** PAT has Contents (R/W), Pull Requests (R/W), Issues (R/W), Actions (R), Metadata (R)
3. **Environment Variable Set:** PAT is stored in environment variable `GITHUB_PAT` or `GITHUB_TOKEN`
4. **Not Hardcoded:** PAT is not present in any code files or repositories
5. **Test Access:** You can successfully authenticate to GitHub using the PAT

**Test Command:**
```bash
curl -H "Authorization: token $GITHUB_PAT" https://api.github.com/user
```

**Expected Response:** Returns your GitHub user information (not an authentication error)

**Confirmation:** I confirm that my GitHub PAT is correctly configured and verified.

---

## Development Environment Setup

- [ ] Local development environment configured
- [ ] Git configured with your GitHub credentials
- [ ] Required tools installed (based on your role)
- [ ] IDE/editor configured
- [ ] SSH keys configured (if using SSH for Git)

**Verification:** You can clone a repository and make commits.

### Role-Specific Tools

| Role | Required Tools |
|:---|:---|
| **Execution Agent** | Git, Node.js/Python, Docker (if needed) |
| **QA Agent** | Git, Testing frameworks, Test runners |
| **Security Agent** | Git, Security scanning tools, Cryptography libraries |
| **Chief of Staff** | Git, GitHub CLI (optional) |
| **Founder** | Git, GitHub CLI (optional) |

---

## Communication & Support Setup

- [ ] GitHub notifications configured: https://github.com/settings/notifications
- [ ] Team communication channels joined (if applicable)
- [ ] Escalation contacts identified
- [ ] Support documentation reviewed

**Verification:** You receive GitHub notifications for your assigned issues and PRs.

---

## Governance Compliance Acknowledgment

- [ ] All Founder Decisions reviewed and understood
- [ ] Governance enforcement mechanisms understood
- [ ] CI/CD compliance requirements acknowledged
- [ ] Security and privacy requirements understood
- [ ] Escalation procedures understood

**Verification:** I understand the governance framework and will comply with all Founder Decisions.

---

## Final Verification & Sign-Off

### Chief of Staff Verification

The Chief of Staff must verify the following before clearing an agent for execution:

- [ ] All pre-execution requirements completed
- [ ] GitHub PAT setup verified and tested
- [ ] Role assignment confirmed
- [ ] Founder Decisions review acknowledged
- [ ] Development environment confirmed
- [ ] Communication setup verified

### Agent Confirmation

I confirm that I have completed all items in this checklist and am ready to begin execution:

- [ ] All pre-execution requirements completed
- [ ] GitHub PAT is configured, tested, and verified
- [ ] Role responsibilities understood
- [ ] Founder Decisions reviewed
- [ ] Development environment ready
- [ ] Ready to execute assigned work

**Agent Name:** ________________  
**Date Completed:** ________________  
**Chief of Staff Approval:** ________________  

---

## Ongoing Compliance

### During Execution

- Maintain PAT security and rotation schedule
- Comply with all Founder Decisions
- Report blockers and escalations promptly
- Keep development environment updated
- Monitor GitHub notifications

### Upon Role Completion

- [ ] Revoke GitHub PAT immediately
- [ ] Remove local credentials
- [ ] Archive work and documentation
- [ ] Provide final status report
- [ ] Confirm role completion with Chief of Staff

---

## Support & Escalation

**Questions about onboarding?**
- Create an issue in the governance repository: https://github.com/webwaka-factory/webwaka-governance/issues
- Tag `@webwakaagent2` (Chief of Staff) for urgent matters
- Reference this checklist in your issue

**PAT Issues?**
- Verify PAT has correct permissions
- Check environment variable is set correctly
- Test with the verification command above
- Revoke and regenerate if needed

**Document Location:**
https://github.com/webwaka-factory/webwaka-governance/blob/main/docs/launch/AGENT_ONBOARDING_CHECKLIST.md

---

**Status:** ✅ **MANDATORY ONBOARDING CHECKLIST - COMPLETE**

All agents must complete this checklist before execution begins. The Chief of Staff enforces this requirement as a hard blocker.
