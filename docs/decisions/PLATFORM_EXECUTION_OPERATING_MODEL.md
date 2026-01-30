# WebWaka Platform-Wide Execution Operating Model

**Version:** 1.0 (Draft for Review)  
**Date:** January 30, 2026  
**Author:** Manus AI

---

## 1. Introduction

This document defines the foundational, platform-wide execution operating model for the WebWaka project. It synthesizes three critical, structural decisions into a single, cohesive framework designed to enable scalable, parallel, multi-agent execution while guaranteeing architectural and governance continuity for decades to come. This is the system that will build WebWaka.

---

## 2. Decision Area 1: GitHub Repository Structure

**Recommendation:** A hybrid model of four thematically-grouped monorepos.

| Repository | Purpose | Contents | Lifecycle |
| :--- | :--- | :--- | :--- |
| **`webwaka-governance`** | The single source of truth for what to build. | Master Control Board, canonical documents, phase definitions, decision records. | Living document; `main` is always canonical. |
| **`webwaka-platform`** | The stable, versioned foundation. | Core Services and Capabilities. | Strict semantic versioning (e.g., `v1.0.0`). |
| **`webwaka-suites`** | The user-facing applications. | Commerce, MLAS, Transportation, and all future suites. | Independently versioned suites. |
| **`webwaka-infra`** | The `Compile & Deploy` engine. | Infrastructure-as-code for all deployment modes. | Aligned with deployment needs. |

This structure provides a clean separation of concerns, enables parallel workstreams, and aligns perfectly with the platform's layered architecture and the `Compile & Deploy` model for SaaS, Partner, and Enterprise deployments.

---

## 3. Decision Area 2: Multi-Agent Vibe Coding Execution Model

**Recommendation:** A formal "Vibe Coding" model where the "vibe" is the complete, canonical context from the `webwaka-governance` repository.

**Core Principles:**

*   **GitHub is the Supreme Source of Truth:** An agent's internal memory is irrelevant.
*   **Partial Context is Impossible:** Onboarding starts with cloning `webwaka-governance`.
*   **Tools Enhance, They Do Not Define:** Outputs must be standard code and docs on GitHub.
*   **Handoff is Explicit and Verifiable:** All work is handed off via pull requests.

This model guarantees architectural, governance, and decision-history continuity, regardless of which agent is executing the work.

---

## 4. Decision Area 3: Documentation & Prompt Architecture

**Recommendation:** A "Living Documentation" architecture where tasks are assigned by link, not by ad-hoc messages.

**Key Features:**

*   **Canonical Hierarchy:** A strict, numbered, and organized directory structure within `webwaka-governance`.
*   **Embedded Execution Prompts:** Standardized, version-controlled prompts are embedded directly within the relevant governance documents (e.g., phase definitions).
*   **Self-Navigating Workflow:** Agents follow links from the prompt to the Master Control Board and other canonical documents, ensuring they always have the full context.

This architecture eliminates context drift and ambiguity, turning the documentation itself into an executable system for managing work.

---

## 5. Synthesis: The Complete Operating Model

These three decisions combine to create a powerful, scalable, and resilient operating model:

1.  **A task is initiated** by pointing an agent to an **embedded execution prompt** (Decision 3) in a document within the **`webwaka-governance`** repo (Decision 1).
2.  **The agent onboards** by cloning the governance repo and reading the canonical context (Decision 2).
3.  **The agent executes the work**, writing code to the appropriate repository (`webwaka-platform` or `webwaka-suites`) (Decision 1).
4.  **The agent submits the work** via a pull request for verification and handoff (Decision 2).
5.  **The `webwaka-infra` repo** consumes the versioned outputs to deploy the platform (Decision 1).

This closed-loop system ensures that every line of code is directly traceable to a version-controlled governance artifact, and that every agent is always operating from the same, complete source of truth.

---

## 6. Open Questions & Ratification Path

**Open Questions for Founder:**

1.  **Repo Structure:** Does the four-repository topology align with your long-term vision?
2.  **Execution Model:** Are you comfortable with GitHub, not agent memory, as the supreme source of truth?
3.  **Doc Architecture:** Are you comfortable with embedding execution prompts directly within the governance documents?

**Recommended Ratification Path:**

1.  **Review:** Founder reviews this synthesized proposal.
2.  **Amend:** I will incorporate any feedback into a final version.
3.  **Ratify:** Founder provides final approval.
4.  **Execute:** I will restructure the repositories and documentation to implement this operating model.
