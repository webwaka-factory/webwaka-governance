# 📘 Founder Decision Index

**Last Updated:** February 2, 2026  
**Status:** Active and Enforced  
**Total Decisions:** 13 (All Ratified)

---

## Decision Registry

### FD-2026-001: Offline-First Is Non-Negotiable Invariant

| Field | Value |
| :--- | :--- |
| **Issue** | #7 |
| **Title** | Offline-First Is Non-Negotiable Invariant |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Invariant |
| **Scope** | Platform Architecture |

**Decision Statement**
The WebWaka platform operates under an **offline-first invariant**. This is non-negotiable and fundamental to the platform architecture.

**Rationale**
- Users must be able to work offline without losing data
- The platform must survive app restarts with zero data loss
- Offline capability is a core competitive advantage

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_OFFLINE_FIRST`
- Related PRs: #62, #63, #64, #65, #66, #67, #68, #69, #70, #71, #72, #73

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-002: Transaction Queue Persistence Required

| Field | Value |
| :--- | :--- |
| **Issue** | #8 |
| **Title** | Transaction Queue Persistence Required |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Invariant |
| **Scope** | Data Durability |

**Decision Statement**
All offline transactions must persist across app restarts. No transaction may be silently lost.

**Rationale**
- Users trust the platform with their data
- Silent data loss is unacceptable
- Transactions are the unit of work

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_TRANSACTION_DURABILITY`
- Related Issues: #30, #37, #38, #39

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-003: Sync-On-Reconnect Is Mandatory

| Field | Value |
| :--- | :--- |
| **Issue** | #9 |
| **Title** | Sync-On-Reconnect Is Mandatory |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Invariant |
| **Scope** | Network Synchronization |

**Decision Statement**
When the app reconnects to the network, automatic sync is mandatory. Users must not manually trigger sync.

**Rationale**
- Seamless user experience
- Automatic recovery from network disruptions
- Zero manual intervention required

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_AUTO_SYNC`
- Related Issues: #43, #44, #45, #46

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-004: Multi-Repository Topology Is Authoritative

| Field | Value |
| :--- | :--- |
| **Issue** | #10 |
| **Title** | Multi-Repository Topology Is Authoritative |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Architecture |
| **Scope** | System Structure |

**Decision Statement**
The WebWaka platform architecture uses a multi-repository topology. This topology is authoritative and defines the system structure.

**Rationale**
- Clear separation of concerns
- Scalable team organization
- Governance at repository level

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_REPO_TOPOLOGY`
- Repositories: 12 total (7 active, 5 archived)

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-005: GitHub Is The Sole System of Record

| Field | Value |
| :--- | :--- |
| **Issue** | #11 |
| **Title** | GitHub Is The Sole System of Record |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Governance |
| **Scope** | System of Record |

**Decision Statement**
GitHub is the authoritative system of record for all WebWaka work. No parallel tracking systems are permitted.

**Rationale**
- Single source of truth
- Full auditability
- Immutable history
- Integrated governance

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_GITHUB_SOR`
- Policy: No external tracking systems

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-006: Role-Based Agent Execution (Not Account-Based)

| Field | Value |
| :--- | :--- |
| **Issue** | #12 |
| **Title** | Role-Based Agent Execution (Not Account-Based) |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Governance |
| **Scope** | Agent Execution Model |

**Decision Statement**
Agent execution is role-based, not account-based. A single Manus account may execute multiple roles via team membership.

**Rationale**
- Flexible agent allocation
- Clear role attribution
- Scalable team organization
- Governance at role level

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_ROLE_BASED_EXECUTION`
- Teams: 5 Phase 1 teams defined

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-007: Founder Is Sole Decision Authority

| Field | Value |
| :--- | :--- |
| **Issue** | #13 |
| **Title** | Founder Is Sole Decision Authority |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Governance |
| **Scope** | Decision Authority |

**Decision Statement**
The Founder is the sole decision authority. No decision authority may be delegated.

**Rationale**
- Clear accountability
- Unified vision
- No conflicting decisions
- Founder retains control

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_FOUNDER_AUTHORITY`
- Policy: All decisions require Founder approval

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-008: Decisions Are Immutable Once Approved

| Field | Value |
| :--- | :--- |
| **Issue** | #14 |
| **Title** | Decisions Are Immutable Once Approved |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Governance |
| **Scope** | Decision Immutability |

**Decision Statement**
Once a decision is approved (FD-YYYY-NNN), it is immutable. Changes require a new decision.

**Rationale**
- Stability and predictability
- Clear audit trail
- No retroactive changes
- Governance integrity

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_DECISION_IMMUTABILITY`
- Policy: All decisions versioned

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-009: CI Enforcement Is Non-Negotiable

| Field | Value |
| :--- | :--- |
| **Issue** | #15 |
| **Title** | CI Enforcement Is Non-Negotiable |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Governance |
| **Scope** | Enforcement Mechanism |

**Decision Statement**
All governance rules are enforced via CI/CD. No manual enforcement is permitted.

**Rationale**
- Consistent enforcement
- No human error
- Scalable governance
- Automated compliance

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_CI_ENFORCEMENT`
- Workflow: Deployed to 6 active repositories

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-010: Platform Crypto Only (No Custom Crypto)

| Field | Value |
| :--- | :--- |
| **Issue** | #16 |
| **Title** | Platform Crypto Only (No Custom Crypto) |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Security |
| **Scope** | Cryptography |

**Decision Statement**
The platform uses only platform-provided cryptographic libraries. No custom crypto implementations are permitted.

**Rationale**
- Security best practices
- Auditable implementations
- No crypto vulnerabilities
- Standards compliance

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_PLATFORM_CRYPTO_ONLY`
- Related Issue: #35 (OFF-002)

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-011: Data Encryption At Rest Is Mandatory

| Field | Value |
| :--- | :--- |
| **Issue** | #17 |
| **Title** | Data Encryption At Rest Is Mandatory |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Security |
| **Scope** | Data Protection |

**Decision Statement**
All offline data must be encrypted at rest using AES-256-GCM.

**Rationale**
- Data protection
- Privacy compliance
- Security best practices
- User trust

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_ENCRYPTION_AT_REST`
- Related Issue: #35 (OFF-002)

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-012: No Hardcoded Secrets or Keys

| Field | Value |
| :--- | :--- |
| **Issue** | #18 |
| **Title** | No Hardcoded Secrets or Keys |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Security |
| **Scope** | Secret Management |

**Decision Statement**
No hardcoded secrets, API keys, or cryptographic keys are permitted in code.

**Rationale**
- Security best practices
- Prevent accidental exposure
- Key rotation capability
- Compliance requirements

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_NO_HARDCODED_SECRETS`
- Related Issue: #35 (OFF-002)

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

### FD-2026-013: All Context and State Lives in GitHub

| Field | Value |
| :--- | :--- |
| **Issue** | #19 |
| **Title** | All Context and State Lives in GitHub |
| **Date Ratified** | February 2, 2026 |
| **Ratified By** | Chief of Staff on behalf of Founder |
| **Category** | Governance |
| **Scope** | Context Management |

**Decision Statement**
All task context, decisions, and state must live in GitHub. No agent may assume context outside documented artifacts.

**Rationale**
- Auditability
- Context preservation
- Handoff safety
- Governance enforcement

**Enforced By**
- CI check: `governance-enforcement.yml`
- Invariant: `INVARIANT_GITHUB_CONTEXT`
- Policy: No out-of-band communication

**Immutability Status**
- ✅ Locked (cannot be changed without new FD)
- ✅ Registered in governance index
- ✅ Enforced by CI/CD

---

## Summary Statistics

| Metric | Value |
| :--- | :--- |
| **Total Decisions** | 13 |
| **Ratified** | 13 (100%) |
| **With FD IDs** | 13 (100%) |
| **Invariants Defined** | 13 |
| **Enforced by CI** | 13 (100%) |
| **Immutable** | 13 (100%) |

## Governance Status

🟢 **FULLY ACTIVE AND ENFORCED**

- ✅ All decisions ratified
- ✅ All decisions indexed
- ✅ All invariants enforced by CI/CD
- ✅ All decisions immutable
- ✅ No decision gaps or ambiguities

## Next Steps

1. **Deployment** — Governance CI enforced on all active repositories
2. **Monitoring** — Watch for governance violations
3. **Escalation** — Any conflicts escalate to Founder
4. **Maintenance** — Index updated as new decisions are made

---

**Index Status:** ✅ COMPLETE AND ACTIVE  
**Last Updated:** February 2, 2026  
**Maintained By:** Chief of Staff (Manus)  
**Authority:** Founder
