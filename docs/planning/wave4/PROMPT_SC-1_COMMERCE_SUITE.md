# PaA Execution Prompt: SC-1 - Commerce Suite V1

**Prompt Version:** 1.0  
**Phase ID:** SC-1  
**Phase Name:** Commerce Suite V1  
**Assigned Platform:** Manus  
**Execution Wave:** 4 (Parallel)

---

## 1. Objective

Build a unified, feature-rich commerce suite that integrates four existing capabilities (CB-1, CB-2, CB-3, CB-4) into a cohesive, user-facing product. This is the first and largest suite to be built on the WebWaka platform.

---

## 2. Scope & Requirements

### Mandatory Features:
1.  **Unified Dashboard:** A single dashboard for partners and clients to manage all commerce-related activities.
2.  **Offline-First POS:** An optional, offline-first Point-of-Sale system.
3.  **Marketplaces:** Both Single Vendor Marketplace (SVM) and Multi-Vendor Marketplace (MVM) models.
4.  **Inventory Sync:** Configurable, opt-in inventory synchronization across POS, SVM, and MVM.
5.  **Logistics & Accounting:** Integration with advanced logistics, accounting, and tax automation.
6.  **Customer Engagement:** Loyalty programs, coupons, subscriptions, and returns/refunds management.

### Target Repository:
*   `webwaka-suites` (This repository must be created as the first step of execution)

### Implementation Path:
*   `/implementations/sc1-commerce-suite/`

---

## 3. Governance & Compliance

*   **INV-004 (Layered Dependency Rule):** This suite must depend on the underlying capabilities, not the other way around.
*   **INV-012v2 (Multi-Repository Topology):** All work must be committed to the new `webwaka-suites` repository.

---

## 4. Completion & Verification

*   **Repository Creation:** The `webwaka-suites` repository must be created and publicly accessible.
*   **Code Complete:** All features implemented and E2E tests passing.
*   **Documentation:** A comprehensive architecture document (`ARCH_SC1_COMMERCE_SUITE.md`) and implementation summary must be created.
*   **Verification:** Founder will verify all features and integrations.

---

## 5. Execution Backlinks

*   **Final Commit SHA:** [To be filled upon completion]
*   **Completion Report:** [To be filled upon completion]

---

**End of Prompt**
