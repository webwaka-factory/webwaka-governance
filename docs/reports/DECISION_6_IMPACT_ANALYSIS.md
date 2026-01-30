# Founder Decision 6 Impact Analysis: Default Update & Upgrade Policy

**Version:** 1.0  
**Date:** January 30, 2026  
**Author:** Manus AI

---

## 1. Executive Summary

This document analyzes the impact of **Founder Decision 6: Default Update & Upgrade Policy for Self-Hosted / Fully Isolated Clients**. This decision establishes a clear framework for managing software updates for deployments outside of the core Shared SaaS environment, transforming updates from a forced push into a **governed lifecycle**.

The core principle is that **self-hosted does not mean uncontrolled**. Clients gain control over the timing and scope of updates, while WebWaka retains control over the integrity, security, and compatibility of the platform. This policy is critical for building trust with enterprise and partner clients who require stability and control over their own environments.

---

## 2. Canonical Decision Summary

**Decision 6 establishes the following non-negotiable principles:**

*   **Governed Lifecycle:** Updates are opt-in, policy-driven, auditable, and reversible.
*   **Update Channel Policy:** All self-hosted and partner-deployed instances must declare an update channel at deployment: `auto-update`, `manual-approval`, or `frozen`.
*   **Granular Version Pinning:** Clients can freeze updates at the platform, suite, or capability level, avoiding an all-or-nothing approach.
*   **Mandatory Security Patching:** Critical security patches can be forcibly applied across all update channels to maintain platform integrity. This process is non-feature-changing, backward-compatible, and includes advance notice and rollback support.
*   **Immutable Deployment:** All updates are applied by re-running the "Compile & Deploy" pipeline with an updated deployment manifest, leveraging immutable infrastructure principles.
*   **Client Autonomy within Guardrails:** Clients can delay non-security updates but are prohibited from modifying core code, skipping security patches, or creating forked versions of the platform.

**The canonical statement is:**

> WebWaka treats updates as a governed lifecycle, not a forced push. Self-hosted clients control timing and scope, while WebWaka guarantees security, integrity, compatibility, and rollback safety.

---

## 3. Governance & Architectural Impact

The decision has been propagated across all relevant governance and planning documents.

### 3.1. Platform Implementation Framework V3

A new "Never Break" invariant has been added to codify the update policy:

*   **INV-008: Update Policy as Governed Lifecycle.** This makes the governed update process a foundational, immutable rule of the platform architecture, ensuring all future deployment and orchestration services adhere to it.

### 3.2. Master Implementation Plan V2

Decision 6 resolves the final blockers for the infrastructure and deployment hardening phases:

*   **ID-1 & ID-2 Unblocked:** The blockers "Default update policy for new self-hosted clients" and "Default update policy for new partner-deployed clients" have been removed.
*   **Readiness Status Updated:** The readiness status for **ID-1 (Enterprise Deployment Automation)** and **ID-2 (Partner Whitelabel Deployment)** has been upgraded from `🟡 Partially specifiable` to `✅ Fully specifiable now`.
*   **Scope Expanded:** The objectives for ID-1 and ID-2 have been updated to include the implementation of Update Channel Policy enforcement, version pinning, and security patch enforcement.

### 3.3. Master Control Board

The Master Control Board now reflects the new governance state for updates:

*   **New Invariant Added:** `INV-008` has been added to the "Never Break" Invariants section.
*   **Super Admin Automation Expanded:** New automation steps for **Configure Update Channel Policy**, **Enforce Security Patches**, and **Monitor Version State** have been added to the "Compile & Deploy" pipeline.
*   **ID-1 & ID-2 Phases Updated:** The entries for the `ID-1` and `ID-2` phases have been updated to reflect their `✅ Fully specifiable` status, expanded scope, and the resolution of their previous blockers.

---

## 4. Alignment with Existing Invariants

This decision is fully aligned with and reinforces existing platform invariants.

| Invariant | How Decision 6 Aligns |
| :--- | :--- |
| **INV-004: Partner-Led Operating Model** | Partners can offer their clients different update policies, providing another layer of value and control. |
| **INV-005: Partner-Led Operating Model** | This policy gives partners and enterprise clients the control and stability they need to run their businesses on the WebWaka platform, building trust and reducing operational risk. |
| **Offline-First** | The requirement for resumable, chunked, and verifiable updates directly addresses the challenges of deploying updates in low-connectivity environments. |

---

## 5. Conclusion

Founder Decision 6 is a pivotal decision that makes the WebWaka platform viable for serious enterprise and government use cases. By providing clear, flexible, and secure rules for software updates, it addresses a major concern for any organization that cannot tolerate forced, unpredictable changes to its core systems.

This decision de-risks the `ID-1` and `ID-2` phases, provides a clear path to supporting sophisticated clients, and ensures the long-term maintainability and security of the entire platform ecosystem, preventing fragmentation while respecting client autonomy.
