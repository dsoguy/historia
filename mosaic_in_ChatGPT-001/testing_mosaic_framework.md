# Testing mosaic framework

In Claude:
1. Create new project `testing mosaic framework`, no instructions, add files from GitHub repository `dsoguy/mosaic` using `main` branch.
2. Start new chat session, type the following:

```text
Use repository dsoguy/mosaic on main.

Initialize an ADOPT architecture session using:
architectures/ADOPT/09-prompts/Session_Bootstrap_Prompt.md

Operating Scope: ARCHITECTURE
Architecture ID: ADOPT
Task / Topic: FY26 baseline onboarding exercise

Reconstruct current ADOPT authority from the repository before doing any analysis.

Do not modify GitHub.
Do not create decisions or baseline membership.
Report the initialization result and stop.
```

---

# ADOPT Session Initialization Result

## Operating Scope
- **Confirmed scope:** `ARCHITECTURE` (ADOPT only)
- **Architecture ID:** `ADOPT`
- **Framework state:** Not loaded. Scope is `ARCHITECTURE`, not `COMBINED`, so `mosaic` framework lifecycle/actions are intentionally excluded.
- **Task / Topic:** FY26 baseline onboarding exercise (retrieval focus only — does not grant authority)

*(Plain-language note: I rebuilt ADOPT's current status only from the saved repository files, not from memory or chat history. I changed nothing.)*

## Authority Sources Established
Read in required order before analysis: `REPOSITORY_CONTEXT.md` → `DOCUMENT_SCHEMA.md` → `AI_OPERATING_MODEL.md` → ADOPT control plane → applicable Shared governance → ADOPT governance. Engagement Profile loaded last, for behavior only.

## ADOPT Lifecycle / Current State
| Item | Status |
|---|---|
| Lifecycle phase | **NOT ESTABLISHED** |
| Approved architecture baseline | **NOT ESTABLISHED** (no members) |
| Requirements baseline | Not established |
| Accepted ADRs / decisions | None recorded |
| Ordered active-work queue | **NOT ESTABLISHED** |
| Exact resume task | None — no authoritative ordered ADOPT work item to resume |

I did not infer a lifecycle phase or action order from framework work, open questions, or the migration history.

## Baseline Status (relevant to your task)
- ADOPT baseline is **empty**.
- **Known baseline candidate:** the TAC-approved **November 2025 DSO Solution Architecture**. It is a *candidate only* — its onboarding decision is open under **OQ-004**.
- Existence in Git, Shared placement, or prior external approval does **not** make it a baseline member.

*(Plain-language note: "FY26 baseline onboarding" is exactly the work that OQ-004 is about, but no artifact has been approved into the baseline yet. Per your instruction, I'm not creating that membership or a decision.)*

## Applicable Shared Governance (loaded because ADOPT explicitly references it)
All nine Shared constraints are marked **ACTIVE** for ADOPT:

| Shared ID | Subject |
|---|---|
| SH-CON-001 | Canadian cloud-region requirement |
| SH-CON-002 | ISO governance checkpoints |
| SH-CON-003 | Observability / audit treatment |
| SH-CON-004 | Microsoft Azure required when cloud is used |
| SH-CON-005 | Landing-zone / hub-and-spoke requirement |
| SH-CON-006 | Approved cloud-resource requirement |
| SH-CON-007 | Cloud cost-management obligations |
| SH-CON-008 | Mandatory resource tagging |
| SH-CON-009 | Resource naming standard |

## ADOPT-Specific Governance
**Constraints**
- **CON-003** (ED-109A/DO-278A aviation assurance) — `CANDIDATE`, blocked pending S&Qt guidance (OQ-008)
- **CON-011** (in-transit geographic-residency) — `ACTIVE`, provenance = TAC-approved 2025 DSO SA

**Principles**
- **PRN-001** Zero Trust — `CANDIDATE`
- **PRN-002** Environment isolation — `CANDIDATE`
- **PRN-003** Immutable-artifact SDLC — `CANDIDATE`
- **PRN-004** Infrastructure as Code — `ACTIVE`

**Assumptions:** No active working assumptions (all legacy items resolved).

## Unresolved ADOPT Open Questions
| ID | Topic | Status |
|---|---|---|
| OQ-001 | Formal project name | OPEN |
| OQ-002 | Business problem / scope boundaries | OPEN |
| OQ-004 | Baseline onboarding (incl. Nov 2025 SA) | OPEN |
| OQ-005 | Who can approve ADOPT decisions | OPEN |
| OQ-006 | Requirements baseline | OPEN |
| OQ-007 | Landing-zone ↔ Dev/Test/Stage/Prod mapping | OPEN |
| OQ-008 | ED-109A/DO-278A obligations | BLOCKED (S&Qt) |
| OQ-009 | Zero Trust mandate provenance | OPEN |
| OQ-010 | Source references for Shared cloud-standard extracts | OPEN |

(OQ-003 and OQ-011 are resolved.)

## Authority / Source Gaps Blocking Baseline Onboarding
For your FY26 task specifically, these must be resolved by the appropriate authority before anything can enter the baseline:
- **OQ-004** — which documents/diagrams to onboard as the baseline, and the exact reference to the approved Nov 2025 SA.
- **OQ-005** — who is authorized to approve ADOPT decisions (needed to move any ADR to `Accepted`).
- **OQ-001 / OQ-006** — formal project name and requirements baseline still unknown.

## Behavior Configuration
- **Engagement Profile:** Loaded — Senior Solution Architect (Azure / DevSecOps). Governs AI behavior only; establishes no facts, decisions, or baseline membership.

## Initialization Complete — Stopping as Instructed
No GitHub modifications made. No decisions or baseline membership created. No action queue synthesized.

**Ready state:** I can now support the FY26 baseline onboarding *analysis* (e.g., outlining what OQ-004 needs, or drafting a candidate onboarding approach as a `PROPOSAL`) without changing any authoritative state. Tell me how you'd like to proceed.


