# 5 — ClaudeCode / Cross-Model Spot Check

I'll start by examining the repository state and structure, then read the Framework contracts as instructed.

HEAD is exactly at the pinned SHA `f61aa2d124fd6e9a683c8c5fea5459a1cd6a1116` — I can confirm the target. Let me read the Framework contracts first, as instructed.

Confirmed: `f61aa2d` is the tip of `origin/main`, matching the pinned target. Now let me read the stable Framework contracts.

Now the remaining stable contracts and the migration record (for the COMBINED-semantics check).

Framework contracts read. Now initializing `ARCHITECTURE / ADOPT` — loading its control plane, governance, and decisions.

Now the ADOPT governance, decisions, AI profile, plus the containers and framework control plane to verify separation.

I have completed a full read-only initialization and validation of `ARCHITECTURE / ADOPT`. Everything needed is in hand — no repository modifications were made. Here is the report.

---

# Cross-Model Spot Check — `ARCHITECTURE / ADOPT`

## 0. What I did (plain-language summary)

I opened the `mosaic` repository at the pinned point, read the four stable "rulebook" files (Framework contracts) first, then rebuilt the ADOPT architecture's state purely from its own files — no memory, no other model's results. I then checked that ADOPT sits in its own locked lane and that nothing leaked in from neighboring lanes.

---

## 1. Result

### ✅ PASS

The ADOPT namespace initializes correctly, its authoritative state reconstructs exactly from durable files, all explicit "governed" states are preserved, and namespace isolation holds. No blocking or non‑blocking findings against the ADOPT objective. One Framework‑scope observation is noted below for transparency (it is outside ADOPT authority and does not affect this result).

---

## 2. Blocking findings

**NONE.**

---

## 3. Non-blocking findings

**NONE** within the ADOPT validation scope.

---

## 4. Observations

| # | Observation | Why it doesn't change the result |
|---|---|---|
| O‑1 | **Framework control‑plane vs. `main` tension (Framework scope, not ADOPT).** `framework/00-control/CURRENT_STATE.md` and `WORKING_BRANCH_LOCK.md` describe the onboarding/session‑UX work as still *in progress* on a locked feature branch `framework-onboarding-session-ux`, "HUMAN RE‑REVIEW PENDING," not yet integrated to `main`. Yet that same state, and commit `f61aa2d` titled *"Improve first-session onboarding and AI workflow UX,"* physically sit on `main`. This is an internal Framework‑state matter. | ADOPT is the validation target. Framework mutable state is **read‑only** here and out of ADOPT authority. It does not touch any ADOPT file. I preserve it as‑is rather than "fixing" or inferring it away. A separate `FRAMEWORK` session owns any reconciliation. |
| O‑2 | **Isolation is real, not just claimed.** The repository contains other authority namespaces — `architectures/ouroboros/`, `shared-knowledge/IAM/`, `shared-knowledge/ghe_copilot/` — plus the `framework/` namespace. All were treated as read‑only; none contributed state to ADOPT. | Confirms the single‑mutable‑scope rule rather than contradicting it. |
| O‑3 | **Correct separation of Framework history from ADOPT.** Framework state carries Phase 1/2, ACT‑001…006, and a branch lock. ADOPT's control plane correctly carries **none** of these; the `FRAMEWORK_MIGRATION_RECORD.md` documents the ACT‑004D remediation that historically pulled these apart. | This is exactly the behavior the check demanded — a positive result, recorded as an observation. |

---

## 5. Client / harness limitations (especially Git SHA visibility)

| Aspect | This session's harness (Claude Code CLI + local git) |
|---|---|
| **Exact Git SHA visibility** | **Available.** `git rev-parse HEAD` → `f61aa2d124fd6e9a683c8c5fea5459a1cd6a1116`, matching the declared target exactly. `origin/main` also resolves to `f61aa2d`, so the pinned `main @ f61aa2d…` content is confirmed. |
| **Relation to recorded limitation** | The Client Capability Register (`VALIDATION_PROTOCOL.md`) records that the *"ClaudeAI repository view"* could **not** expose commit metadata as of 2026‑08‑17. This session runs a **different** harness (CLI with direct git), which **does** expose it. Per protocol, I report the observed capability rather than re‑applying the old limitation; I do not reclassify the pre‑recorded limitation as a new finding. |
| **Content vs. target consistency** | No observable repository‑content inconsistency with the declared target. Working tree is clean; the validation branch `claude/cross-model-spot-check-tic3kg` is at the same tree as `main @ f61aa2d`. |

---

## 6. Reconstructed authoritative ADOPT state

Rebuilt solely from `architectures/ADOPT/`, reported in the `AI_OPERATING_MODEL.md` initialization order:

**1. Operating Scope** — `ARCHITECTURE`

**2. Authority Namespace (the one mutable lane)** — `architectures/ADOPT/`
- All other namespaces (`framework/`, `shared-knowledge/IAM/`, `shared-knowledge/ghe_copilot/`, `architectures/ouroboros/`) are **read‑only**.

**3. Current State**
| Concept | Value |
|---|---|
| Architecture ID | `ADOPT` |
| Formal SA name | `NOT ESTABLISHED` (OQ‑001) |
| Lifecycle State | `NOT ESTABLISHED` |
| Architecture Baseline | `NOT ESTABLISHED` |
| Requirements Baseline | `NOT ESTABLISHED` |
| Accepted Decisions | `NONE` |
| Ordered Architecture Work | `NOT ESTABLISHED` |
| Resume State | `NOT ESTABLISHED` |

**4. Baseline State** — `NOT ESTABLISHED`. Current members: `NONE`. One **candidate** only: the TAC‑approved November 2025 DSO Solution Architecture (open under OQ‑004). Presence/external approval does **not** make it a baseline member.

**5. Ordered Work** — `NOT ESTABLISHED`. No action queue exists; open questions do not imply an action order. (Preserved as explicit absence, not invented.)

**6. Resume State** — `NOT ESTABLISHED`. A fresh session should reconstruct from the control plane and **not** invent a resume task.

**7. Relevant Unresolved Questions**
- **OPEN:** OQ‑001, OQ‑002, OQ‑004, OQ‑005, OQ‑006, OQ‑007, OQ‑009
- **BLOCKED:** OQ‑008 (ED‑109A/DO‑278A obligations — awaiting Safety & Quality guidance)
- **RESOLVED:** OQ‑003, OQ‑010 (retired Shared governance), OQ‑011 (ID = `ADOPT`)

**8. Task-Relevant Governance / Decisions**
- **Constraints:** CON‑003 `CANDIDATE` (aviation assurance, pending S&Qt); CON‑011 `ACTIVE` (in‑transit geographic‑residency, from TAC‑approved 2025 SA). External Shared constraint mappings: `NONE` (former SH‑CON‑001…009 retired, not copied in).
- **Principles:** PRN‑001 `CANDIDATE`, PRN‑002 `CANDIDATE`, PRN‑003 `CANDIDATE`, PRN‑004 `ACTIVE`.
- **Assumptions:** Active = `NONE` (ASM‑001…004 all `RESOLVED`/retired).
- **Decisions:** `NONE` recorded.

---

### Validation checks — pass/fail detail

| Required check | Result |
|---|---|
| Exactly one mutable authority namespace = `architectures/ADOPT/` | ✅ |
| Framework / Shared / other Architecture namespaces read‑only | ✅ |
| ADOPT current state, baseline, ordered work, resume state, open questions, governance, decisions reconstructed correctly | ✅ |
| Explicit governed states (`NOT ESTABLISHED`, `NONE`, `CANDIDATE`, `ACTIVE`, `OPEN`, `BLOCKED`, `RESOLVED`) preserved, not inferred away | ✅ |
| Cross‑namespace retrieval does not transfer authority (only read‑only FRAMEWORK refs in the index; no Shared applicable) | ✅ |
| Framework mutable state not confused with Architecture state (ADOPT holds no Phase/ACT/lock state) | ✅ |
| Current model uses `FRAMEWORK`/`SHARED`/`ARCHITECTURE` only; no resurrected `COMBINED` semantics | ✅ |
| Initialization reporting follows the `AI_OPERATING_MODEL.md` information contract | ✅ |

**Repository was not modified and no durable state was advanced.**
