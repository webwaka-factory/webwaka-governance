# Founder Decision 4 Impact Analysis: MLAS Revenue Share Model

**Version:** 1.0  
**Date:** January 29, 2026  
**Author:** Manus AI

---

## 1. Executive Summary

This document analyzes the impact of **Founder Decision 4: MLAS Revenue Share Model (Maximum Flexibility, Zero Lock-In)**. This decision fundamentally reframes the Multi-Level Affiliate System (MLAS) from a feature with a predefined business model to a core piece of **configurable infrastructure**.

The key takeaway is that **MLAS is now a revenue-flow engine, not a policy-maker**. This elevates flexibility to a primary architectural principle and ensures the platform does not impose a single, hardcoded business model on its partners or clients.

---

## 2. Canonical Decision Summary

**Decision 4 establishes the following non-negotiable principles:**

*   **MLAS as Infrastructure:** MLAS must provide the tools for revenue sharing (attribution, calculation, routing, auditability) but must NOT dictate the rules (who earns, how much, when, or if the platform takes a cut).
*   **Support for Multiple Models:** MLAS must simultaneously support various revenue models, including Platform-First, Partner-Owned, Client-Owned, Zero-Platform-Cut, and complex Hybrid/Conditional models.
*   **Multi-Level Revenue Trees:** The system must support deep, non-uniform commission trees, not just simple linear chains.
*   **Granular Configuration:** Revenue sharing must be configurable at all levels (per transaction, product, actor, campaign, etc.).
*   **Separation of Concerns:** The architecture must treat **Attribution**, **Commission Rules**, and **Settlement** as three distinct, independent layers.
*   **Offline-First Reality:** The system must be designed for the realities of the Nigerian market, including cash transactions, agent-reported sales, and delayed reconciliation.

**The canonical statement is:**

> MLAS is a revenue-sharing infrastructure that supports arbitrary, configurable, multi-level revenue flows across Platform, Partner, Client, Merchant/Vendor, Agent, and User contexts. It does not impose a business model. All revenue policies are declarative, contextual, auditable, and overrideable within governance constraints.

---

## 3. Governance & Architectural Impact

The decision has been propagated across all relevant governance and planning documents.

### 3.1. Platform Implementation Framework V3

A new "Never Break" invariant has been added:

*   **INV-006: MLAS as Infrastructure, Not Policy.** This codifies the core principle of Decision 4 into the platform's foundational architecture, ensuring all future development adheres to this rule.

### 3.2. Master Implementation Plan V2

Decision 4 directly resolves a critical blocker, enabling detailed planning for the MLAS capability:

*   **CB-1 (MLAS Capability) Unblocked:** The blocker "Revenue share model for MLAS" has been removed.
*   **Readiness Status Updated:** The readiness status for **CB-1** has been upgraded from `🟡 Partially specifiable` to `✅ Fully specifiable now`.
*   **Scope Expanded:** The objective for CB-1 has been updated to reflect the full scope of the decision, including support for multiple revenue models, multi-level trees, and the separation of attribution, commission, and settlement layers. The actor scope has also been expanded to include all relevant parties.

### 3.3. Master Control Board

The Master Control Board has been updated to provide real-time visibility into the new governance state:

*   **New Invariant Added:** `INV-006` has been added to the "Never Break" Invariants section.
*   **MLAS Capability Updated:** The entry for the MLAS capability has been updated to reflect its `✅ Fully specifiable` status, expanded scope, and the resolution of the previous blocker.
*   **Canonical Statement Added:** The canonical statement from Decision 4 has been embedded directly into the MLAS capability section for immediate reference.

---

## 4. Alignment with Existing Invariants

This decision does not conflict with existing platform invariants; it reinforces them.

| Invariant | How Decision 4 Aligns |
| :--- | :--- |
| **INV-001: Pricing Flexibility** | MLAS is now a direct implementation of the pricing flexibility principle, applying it to the complex domain of revenue sharing. |
| **INV-002: Strict Tenant Isolation** | Configurable revenue models can be defined on a per-tenant basis, respecting isolation boundaries. |
| **INV-004: Partner-Led Operating Model** | Partners are not locked into a single revenue model. They can define their own rules, enabling a wider range of business models. |
| **Nigeria-First** | The explicit requirement to support cash transactions, agent-reported sales, and delayed reconciliation directly addresses the realities of the target market. |
| **Offline-First** | The separation of attribution, commission, and settlement layers is critical for supporting offline transactions and eventual reconciliation. |

---

## 5. Conclusion

Founder Decision 4 is a critical step in maturing the WebWaka platform architecture. By defining MLAS as a flexible, configurable infrastructure, it avoids premature optimization and prevents the platform from being locked into a single, restrictive business model.

This decision significantly de-risks the implementation of the MLAS capability and ensures that WebWaka can support a diverse ecosystem of partners and clients with varying monetization strategies. The path to implementing a robust, future-proof MLAS is now clear.
