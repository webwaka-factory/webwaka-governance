# Post-Migration Operating Rules

**Document ID:** GOV-004  
**Version:** 1.0  
**Effective Date:** January 30, 2026  
**Status:** 🔒 **RATIFIED AND BINDING**

---

## 1. Preamble

This document codifies the permanent, non-negotiable operating rules for the WebWaka platform following the successful completion of the Repository Topology Migration (REPO-MIG-1). These rules supersede all previous guidance related to repository structure and execution workflows. Adherence to these rules is mandatory for all platform agents and contributors.

---

## 2. Migration Closure Statement

The Repository Topology Migration is formally **CLOSED** as of January 30, 2026.

*   The multi-repository topology is now the **only valid operating model** for the WebWaka platform.
*   The original monorepo (`webwaka-monorepo-archive`) is permanently **RETIRED** and must not be used for any new work.
*   The re-introduction of monorepo patterns or the consolidation of canonical repositories is explicitly **PROHIBITED**.

---

## 3. Canonical Repositories & Responsibilities

The WebWaka platform is now composed of the following five canonical repositories. All platform artifacts, code, and documentation must reside in the correct repository according to its defined responsibility.

| Repository | Responsibility | URL |
| :--- | :--- | :--- |
| **webwaka-governance** | Governance, Control Board, PaA Prompts, Policies, Invariants | `https://github.com/webwakaagent1/webwaka-governance` |
| **webwaka-platform-foundation** | Platform Primitives & PF Phases | `https://github.com/webwakaagent1/webwaka-platform-foundation` |
| **webwaka-infrastructure** | Infrastructure & Deployment Automation (ID Phases) | `https://github.com/webwakaagent1/webwaka-infrastructure` |
| **webwaka-core-services** | Core Services (CS Phases) | `https://github.com/webwakaagent1/webwaka-core-services` |
| **webwaka-capabilities** | Business Capabilities (CB Phases) | `https://github.com/webwakaagent1/webwaka-capabilities` |

### Forward-Declaration: Suites Repository

A sixth repository, `webwaka-suites`, will be created to house all Suite (SC) layer implementations. This repository will be created during the execution of the first Suite phase.

---

## 4. Execution Rules (Non-Negotiable)

1.  **PaA-Driven Execution:** All work must originate from a formal, PaA-compliant execution prompt located in the `webwaka-governance` repository.
2.  **GitHub Persistence:** No work is considered valid unless it is committed and pushed to the correct canonical repository on GitHub.
3.  **Explicit Cross-Repository References:** All references between repositories (e.g., a Suite depending on a Capability) must be explicit, versioned, and use the `repository@commit-sha:path` format.
4.  **Real-Time MCB Updates:** The Master Control Board (MCB) in the `webwaka-governance` repository must be updated in real time to reflect the current status of all phases.
5.  **Centralized Verification:** All work is subject to verification by the Founder or a designated verification agent. Verification authority remains centralized.

---

## 5. Prompt & Agent Rules

1.  **Prompts as Canonical Artifacts:** Execution prompts are governance artifacts, not ephemeral messages. They must be version-controlled and reside in the `webwaka-governance` repository.
2.  **Agent Onboarding:** All agents, human or AI, must onboard to the platform by first reading the `README.md` and the Master Control Board in the `webwaka-governance` repository.
3.  **Execution without Persistence is Invalid:** Any work that exists only in an agent's local environment is considered invalid and will not be accepted.
4.  **Seamless Platform Switching:** The choice of execution platform (e.g., Manus, Replit) for a given phase will be documented in the MCB. Agents must be able to seamlessly switch between platforms and repositories as required by the execution plan.

---

**End of Document**
