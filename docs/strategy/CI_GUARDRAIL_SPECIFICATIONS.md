# CI Guardrail Specifications

**Status:** DRAFT - Awaiting Founder Review  
**Author:** Chief of Staff (webwakaagent2)  
**Date:** February 3, 2026

---

## 1. Mandate

This document specifies the design of four new CI-enforceable architectural guardrails, as authorized by the Founder. These guardrails are essential for maintaining the long-term integrity and extensibility of the WebWaka platform.

## 2. Guardrail Specifications

### 2.1 Guardrail #1: Mandatory Event Emission

- **Principle:** All new features must emit events for significant state changes.
- **Implementation:** A new CI check will be added to scan PRs for new database models or state-mutating API endpoints. If found, the check will fail if a corresponding event is not emitted.
- **Enforcement:** The check will be implemented as a custom linter or a GitHub Action that analyzes the PR diff.

### 2.2 Guardrail #2: Mandatory API Versioning

- **Principle:** All APIs must be versioned to ensure backward compatibility.
- **Implementation:** A new CI check will be added to scan all API endpoint definitions (e.g., in OpenAPI/Swagger files or code annotations). The check will fail if an endpoint does not have a version identifier (e.g., `/v1/`, `/v2/`).
- **Enforcement:** The check will be implemented as a regex-based linter or a dedicated GitHub Action.

### 2.3 Guardrail #3: No Direct Module-to-Module Dependencies

- **Principle:** Modules must only communicate via events or versioned APIs, not direct code-level dependencies.
- **Implementation:** A new CI check will be added to analyze the dependency graph of the codebase. The check will fail if a module directly imports or calls code from another module, bypassing the approved communication channels.
- **Enforcement:** The check will be implemented using a static analysis tool (e.g., `dependency-cruiser`, `dpdm`).

### 2.4 Guardrail #4: Mandatory Hierarchical Configuration

- **Principle:** All configuration must support hierarchical overrides (Global → Partner → Client).
- **Implementation:** A new CI check will be added to scan all new configuration variables. The check will fail if the configuration access pattern does not include logic for hierarchical overrides.
- **Enforcement:** The check will be implemented as a custom linter or a code-scanning GitHub Action.

## 3. Phased Rollout Plan

- **Phase 1 (Now):** Begin design and implementation of the four guardrails.
- **Phase 2 (Wave 1 Completion):** Deploy the guardrails in a non-blocking "audit" mode to gather data and identify existing violations.
- **Phase 3 (Wave 2 Start):** Enforce the guardrails in a blocking mode for all new pull requests.
