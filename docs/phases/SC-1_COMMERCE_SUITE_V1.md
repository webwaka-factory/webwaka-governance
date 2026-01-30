# SC-1: Commerce Suite V1 - Authoritative Phase Definition

**Version:** 1.0  
**Date:** January 30, 2026  
**Author:** Manus AI  
**Status:** ✅ Fully Specifiable

---

## 1. Core Objective

To build a unified, channel-agnostic commerce suite that empowers WebWaka partners and clients to sell goods and services across multiple online and offline channels. The suite must be flexible, scalable, and fully aligned with the platform's core invariants, particularly Offline-First, Pricing Flexibility, and Partner-Led Operations.

---

## 2. Key Features & Scope (In-Scope)

This suite will be delivered with the following capabilities, which can be enabled or disabled based on client needs:

| Feature | Description | Key Attributes |
| :--- | :--- | :--- |
| **Offline-First POS** | A point-of-sale system designed for unreliable connectivity. | Optional, not mandatory; foundational but not compulsory. |
| **Single Vendor Marketplace (SVM)** | A standard e-commerce storefront for a single merchant. | Channel |
| **Multi Vendor Marketplace (MVM)** | A marketplace platform for multiple independent vendors. | Channel |
| **Inventory Sync** | Synchronizes inventory across all enabled channels (POS, SVM, MVM). | Opt-in, configurable, event-driven. |
| **Advanced Logistics** | Tools for managing shipping, delivery, and fulfillment. | Integrated with order lifecycle. |
| **Accounting & Tax Automation** | Automated ledger entries and tax calculations. | Hooks into the Financial Ledger Service (CS-1). |
| **Loyalty, Coupons, Subscriptions** | Tools for customer retention and recurring revenue. | Configurable at the Partner and Client level. |
| **Returns & Refunds** | A complete system for managing product returns and refunds. | Integrated with inventory and financial ledger. |

### 2.1. Actor Role Distinction

The suite must explicitly recognize and enforce distinct roles and permissions for:

*   **Partner:** Manages multiple clients and their marketplaces.
*   **Client:** Owns and operates one or more channels (POS, SVM, MVM).
*   **Merchant/Vendor:** Sells products within a marketplace.
*   **Agent:** Sells on behalf of a merchant or the marketplace itself.
*   **End User:** The final customer.

---

## 3. Architectural Principles & Alignment

This suite must adhere to all 10 platform invariants.

| Invariant | Implementation in Commerce Suite |
| :--- | :--- |
| **INV-001: Pricing Flexibility** | Prices can be set at the Partner, Client, Merchant, and even Agent level, with support for overrides and dynamic pricing rules. |
| **INV-005: Partner-Led Operating Model** | Partners can create and manage their own commerce ecosystems, inviting clients and vendors. |
| **INV-006: MLAS as Infrastructure** | All sales transactions will generate events that can be consumed by the MLAS capability for commission calculation. |
| **INV-010: Realtime as Optional** | Inventory updates and order statuses will be realtime-enhanced but will fall back to async/eventual consistency. No critical transaction will require realtime. |
| **Offline-First** | The POS will be fully functional offline. All transactions will be queued and reconciled when connectivity is restored. |

---

## 4. Dependencies

*   **CB-1: MLAS Capability:** For revenue sharing on sales.
*   **CB-2: Reporting & Analytics Capability:** For sales and performance dashboards.
*   **CB-3: Content Management Capability:** For product descriptions and marketing content.
*   **CB-4: Inventory Management Capability:** As the single source of truth for inventory.

---

## 5. Execution Readiness

*   **Status:** ✅ **Fully Specifiable Now**
*   **Blockers:** None. All foundational decisions have been made.

---

## 6. Deliverables

*   **Code:**
    *   POS Application (cross-platform)
    *   SVM Application (web)
    *   MVM Application (web)
*   **Documentation:**
    *   User guides for all applications and roles.
    *   API documentation for all services.
    *   Architectural decision records for key implementation choices.
