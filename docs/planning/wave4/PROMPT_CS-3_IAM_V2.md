# PaA Execution Prompt: CS-3 - Identity & Access Management V2

**Prompt Version:** 1.0  
**Phase ID:** CS-3  
**Phase Name:** Identity & Access Management V2  
**Assigned Platform:** Replit  
**Execution Wave:** 4 (Parallel)

---

## 1. Objective

Implement advanced Identity & Access Management (IAM) features to enhance platform security and user experience. This phase builds upon the existing IAM foundation (Phase 2B) and is a critical component of the platform's enterprise readiness.

---

## 2. Scope & Requirements

### Mandatory Features:
1.  **Social Login:** Integrate OAuth 2.0 for major providers (Google, GitHub).
2.  **Two-Factor Authentication (2FA):** Implement TOTP-based 2FA for all user roles.
3.  **Multi-Factor Authentication (MFA):** Add support for additional factors, such as security keys (WebAuthn).
4.  **Account Recovery:** Design and implement a secure account recovery flow for users who have lost access to their 2FA device.
5.  **Audit Trail:** Ensure all security-sensitive actions (login, 2FA enable/disable, password change, etc.) are logged in a dedicated, immutable audit trail.

### Target Repository:
*   `webwaka-core-services`

### Implementation Path:
*   `/implementations/cs3-iam-v2/`

---

## 3. Governance & Compliance

*   **INV-002 (Strict Tenant Isolation):** All IAM data must be strictly isolated by tenant.
*   **INV-003 (Audited Super Admin Access):** Super admin access to IAM data must be explicitly audited.
*   **INV-012v2 (Multi-Repository Topology):** All work must be committed to the `webwaka-core-services` repository.

---

## 4. Completion & Verification

*   **Code Complete:** All features implemented and unit/integration tests passing.
*   **Documentation:** Architecture and implementation summary documents created in the implementation directory.
*   **Verification:** Founder will verify all features and security considerations.

---

## 5. Execution Backlinks

*   **Final Commit SHA:** [To be filled upon completion]
*   **Completion Report:** [To be filled upon completion]

---

**End of Prompt**
