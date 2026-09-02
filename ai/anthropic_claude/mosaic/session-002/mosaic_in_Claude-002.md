# Using mosaic with Claude

> Uploaded 1st-session bootstrap prompt for Claude v1 (file: `bootstrap_prompts_claude_v1.md`).

I've read the uploaded bootstrap prompt. Quick summary of what it is, so we're aligned:

**What the file does**
- It's a starting instruction for a fresh Claude session working in this "mosaic" repository.
- It tells Claude to read the three core rulebooks first, then **stop and ask** which of the three work areas (`FRAMEWORK`, `SHARED`, `ARCHITECTURE`) you want to work in.
- It forbids guessing which area you mean, and requires Claude to give you a short "here's the current state" summary before doing any real work.

Before I do anything with it, I want to make sure I help in the way you actually want.

What would you like me to do with this bootstrap prompt?
1. Review it against the framework rules
2. Suggest improvements/edits
3. Run it (start a session)
4. Just acknowledge — no action
Something else : Skip

---

> Selected 3.

Session started. Following the bootstrap prompt, I've read the three stable Framework contracts:

**1. `REPOSITORY_CONTEXT.md` — what this repo *is***
A portable knowledge repository split into separate "authority areas" so any fresh AI session can pick up work from the files alone, without needing past chat history.

**2. `DOCUMENT_SCHEMA.md` — the filing rules**
Defines the required folder/file structure, the fixed vocabulary for labelling things (fact, constraint, assumption, decision, etc.), and the difference between "empty on purpose" states (`NONE`, `NOT ESTABLISHED`).

**3. `AI_OPERATING_MODEL.md` — how I must behave**
The key rules I'm now operating under:

| Rule | Plain meaning |
|---|---|
| One scope per session | I work in **exactly one** area at a time |
| One mutable namespace | Only that area can be changed; everything else is read-only |
| No inference | I must **not guess** which area or ID you mean |
| Preserve empty states | I keep `NONE` / `NOT ESTABLISHED` as-is; I don't invent content |
| Files are the authority | Past conversation is never the source of truth |

I have **not** selected a work area yet, as the prompt requires.

**Next step — you choose the scope**
The three options mean:
- **FRAMEWORK** — work on the repo's own rules/machinery (no ID needed).
- **SHARED** — a reusable knowledge domain (you'll give me a **Domain ID**).
- **ARCHITECTURE** — a specific solution design (you'll give me an **Architecture ID**).

I won't guess the ID — if you pick SHARED or ARCHITECTURE, I'll ask you for it next.

Which Operating Scope do you want for this session?
1. FRAMEWORK
2. SHARED
3. ARCHITECTURE
Something else 

---

> ARCHITECTURE

Scope set to **ARCHITECTURE** — one specific solution design, which will be the only area I can change this session.

I now need the **Architecture ID** from you. I won't guess it. The repository currently contains two architecture namespaces, so you can pick one — or tell me a different ID if you mean something else.

Which Architecture ID should this session work in?
1. ADOPT
2. ouroboros
3. Other (I'll type it)
Something else

---

> ADOPT

Reconstruction complete. Here is the durable state of the **ADOPT** namespace, rebuilt from its own files only.

## 1. Session setup
- **Operating Scope:** ARCHITECTURE
- **Mutable namespace:** `architectures/ADOPT/` (the only area I can change)
- **Everything else:** read-only
- **Optional AI profile:** an ADOPT "Engagement Profile" exists and is now loaded as *behaviour guidance only* — it has me act as a Senior Solution Architect (Azure / DevSecOps focus, challenger role). It cannot override anything in the files.

## 2. Identity (what ADOPT is)
- **Architecture ID:** ADOPT
- **Formal name:** `NOT ESTABLISHED` (open — OQ-001)
- **Confirmed context:** Azure is *one* platform in the solution, not the whole thing. A separate Cloud Infrastructure team owns Azure (hub-and-spoke landing zones). A Solution Architecture was approved by the Technical Architecture Committee in **Nov 2025**.

## 3. Current authoritative state
| Item | State |
|---|---|
| Lifecycle state | `NOT ESTABLISHED` |
| Architecture baseline | `NOT ESTABLISHED` |
| Requirements baseline | `NOT ESTABLISHED` |
| Accepted decisions | `NONE` |
| Active assumptions | `NONE` |

## 4. Baseline
- **Status:** `NOT ESTABLISHED` — no members recorded.
- **Known candidate:** the TAC-approved Nov 2025 DSO Solution Architecture. It is a *candidate only* — being approved elsewhere does **not** make it a baseline member here. Onboarding is open (OQ-004).

## 5. Governance (rules currently on the books)
**Constraints** (must-satisfy conditions):
- **CON-011** — geographic-residency for data in transit → **ACTIVE**
- **CON-003** — aviation assurance (ED-109A/DO-278A) implications → **CANDIDATE**, waiting on Safety & Quality (OQ-008)

**Principles** (guidance):
- **PRN-004** — Infrastructure as Code → **ACTIVE**
- **PRN-001** Zero Trust, **PRN-002** env isolation, **PRN-003** immutable-artifact builds → all **CANDIDATE**

## 6. Ordered work
**`NOT ESTABLISHED`.** No task queue exists. (The open questions below are *not* a to-do list — order isn't implied.)

## 7. Resume state
**`NOT ESTABLISHED`.** There is no saved "pick up here" point. I will not invent one.

## 8. Unresolved questions that matter most
- **OQ-001** — formal name of the architecture (OPEN)
- **OQ-002** — business problem, scope, out-of-scope (OPEN)
- **OQ-004** — which docs to onboard as baseline, incl. the Nov 2025 SA (OPEN)
- **OQ-005** — who can approve ADOPT decisions (OPEN)
- **OQ-006** — requirements baseline (OPEN)
- **OQ-007** — how landing-zone vs Dev/Test/Stage/Prod environments map (OPEN)
- **OQ-008** — aviation assurance obligations (**BLOCKED**, needs S&Qt)
- **OQ-009** — is Zero Trust actually mandated (OPEN)

**Where that leaves us:** ADOPT is structurally set up but deliberately "early stage" — no baseline, no decisions, no ordered work, no resume point. That's valid state, not a gap to fill.

Since there's no task to resume, what would you like to work on in ADOPT this session?

---

> I would like to perform a `reset` of ADOPT and restart clean, whatever information is currently recorded is not to my satisfaction.
> In a nutshell, there is an approved Solution Architecture (SA) dated from November 2025.
> I need to evolve this SA to our end-of-year current-state, which is August 2026, this will become our FY26 baseline for the end of Q4.
> A lot has changes between those 2 points in time, several ADRs (Architecture Decision Record) were created, most are outdate. Perhaps new ones will be required as well.
> Comment.

Comment — from the Solution Architect seat, operating in ARCHITECTURE / ADOPT.

Your goal is sound: take the approved Nov 2025 SA, evolve it to an Aug 2026 current-state, and stamp that as the **FY26 Q4 baseline**. That's a legitimate and well-scoped architecture activity. My pushback is about *method*, not intent — a blanket "reset" is the part I'd slow down on.

## 1. Reality check — what a "reset" actually touches
Most of ADOPT is already empty-on-purpose, so there's far less to clear than it feels like:

| Item | Current state | Would a reset lose anything real? |
|---|---|---|
| Lifecycle / baselines / decisions | `NOT ESTABLISHED` / `NONE` | No — already blank |
| Nov 2025 SA | Candidate reference only, **not in the repo** | No — it lives outside; reset can't touch it |
| Open questions (OQ-001…009) | Several still valid | **Yes — you'd bin questions you still need answered** |
| **CON-011** (data-in-transit residency) | **ACTIVE** | **Yes — this is a real, approved requirement** |
| CON-003, PRN-001…004 | CANDIDATE / mixed | Maybe — some may survive into FY26 |

**101 note:** in this framework a "reset" doesn't delete files — the required files must always exist. It means returning them to their initialized-empty state. So "reset" = *empty the content*, not *remove the structure*.

## 2. My main concern (challenger hat)
A **blanket wipe throws away things you'll immediately need back** — notably the **ACTIVE residency constraint (CON-011)** and the still-open questions. Rebuilding them from memory later is exactly what the framework is designed to prevent. **Risk: Medium–High** (loss of approved requirement + audit trail).

Also: the framework forbids silently deleting, promoting, or resolving state. A reset and a new baseline are fine, but each is a **deliberate, recorded action** — I can only *propose* them; you approve, then it's written down. Nothing changes by me just saying so.

## 3. On the ADRs
- ADOPT's decision register is currently **empty** — your ADRs live outside the repo right now.
- "Most are outdated" → the clean way is **supersede, don't delete**: each onboarded decision gets a status (`ACCEPTED`, `SUPERSEDED`, `DEPRECATED`) so FY26 keeps the *why* behind changes. Wiping them loses that history.

## 4. What I'd need to actually do this
1. The **Nov 2025 SA document** itself (not in the repo yet).
2. The **ADR set**, with each one's current status/intent.
3. **Who can approve** an ADOPT baseline/decision (OQ-005 is still open — without an approver, nothing can become the official FY26 baseline).
4. What specifically is **"not to your satisfaction"** — so a reset doesn't just recreate the same dissatisfaction.

## 5. Recommended sequence (instead of "wipe then rebuild")
1. Confirm **what** to preserve vs clear (don't blanket-wipe).
2. Onboard the Nov 2025 SA + ADRs as the working input.
3. Triage each ADR: keep / supersede / new needed.
4. Derive the Aug 2026 current-state.
5. Have the approver **accept it → FY26 Q4 baseline** (recorded in `BASELINE.md`).

**Confidence:** Highly Confident (80–95%) on the process points — they come straight from the framework contracts. Lower on the substance until I see the SA and ADRs.

One thing to pin down before anything else:

When you say 'reset', how far should it go?
1. Full wipe to empty
2. Clear all except ACTIVE items (keep CON-011)
3. Keep the shell, evolve in place (no wipe)
4. Not sure — advise me
Something else

---

> I fully agree, a `reset` = empty the content, not remove the structure!
> I don't want to trash/delete the existing information, we should transfer the current content for safeguard in a temporary artifact and filter one-by-one, what to keep, update, and place back versus what should be truly discarded.
> I want to reset ASSUMPTIONS, CONSTRAINTS, and PRINCIPLES and restart clean.
> I want to clean-up and/or update all the content within `00-control/`


---
<br>

<br><br><br><br>

<!--

```text/markdown
```

Uploaded test results for `ACT-004D.1 Fresh ChatGPT Validation` from file `Handoff_Lab001_Session005_ChatGPT.md`.
Analyze & comment.

Explain using 101 dummy-style plain language.

In-chat preview first, no artifact generation without a review & approval.

How are we doing regarding this conversation length limit? Be brief. 

Do we have enough room for another exercise?

Provide a recap of this session activities.

Provide full session recap, in-chat preview, no artifact generation.

Generated file: [whatever-title](whatever-filename.md "tag")

[Display Filename Title](filename "tag")
[Display Link Title](URL "tag")
![Display Image title](filename "tag")

-->