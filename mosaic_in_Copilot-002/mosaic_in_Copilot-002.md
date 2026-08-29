# Using mosaic with GitHub Copilot

> Uploaded 1st-session bootstrap prompt for GitHub Copilot v1 (file: `bootstrap_prompts_copilot_v1.md`).

I'll read the three framework contract files you specified (framework/REPOSITORY_CONTEXT.md, framework/DOCUMENT_SCHEMA.md, framework/AI_OPERATING_MODEL.md) so I can follow the repository operating contract, then I'll ask you to choose one Operating Scope. I'll fetch those three files now.Please choose exactly one Operating Scope now: FRAMEWORK, SHARED, or ARCHITECTURE.

What I did (brief): I read the three required framework contracts you asked me to inspect:
- framework/REPOSITORY_CONTEXT.md
- framework/DOCUMENT_SCHEMA.md
- framework/AI_OPERATING_MODEL.md

Key constraints I noted (concise):
- Every session must have exactly one Operating Scope ↔ one mutable authority namespace (FRAMEWORK → framework/, SHARED → shared-knowledge/<domain-id>/, ARCHITECTURE → architectures/<architecture-id>/).
- Do not infer a missing Domain ID or Architecture ID — you must supply it.
- If scope is SHARED or ARCHITECTURE, I must load that namespace’s 00-control/ (CONTEXT.md, CURRENT_STATE.md, BASELINE.md, DOCUMENT_INDEX.md, OPEN_QUESTIONS.md, NEXT_ACTIONS.md, SESSION_HANDOFF.md) before substantive work.
- All other namespaces remain read-only; retrieval does not transfer mutation authority.
- Missing/unknown state must be preserved explicitly (e.g., NOT ESTABLISHED); I must not invent or infer state.
- I will not modify the repository until you supply the Operating Scope (and ID if required).

What I need from you now:
- Choose one Operating Scope: FRAMEWORK, SHARED, or ARCHITECTURE.
  - If you choose SHARED, give the Domain ID (the exact <domain-id> string).
  - If you choose ARCHITECTURE, give the Architecture ID (the exact <architecture-id> string).

What I will do immediately after you reply:
1. Resolve the mutable authority namespace from your choice.
2. Read that namespace’s control-plane files (00-control/) and required governance/decisions files.
3. Use the namespace DOCUMENT_INDEX.md and control-plane to retrieve any additional relevant material.
4. Then summarize: Operating Scope; Mutable authority namespace; Current state; Baseline state; Ordered work (or NOT ESTABLISHED); Resume state (or NOT ESTABLISHED); materially relevant unresolved questions.

I’m ready — please pick one scope (and supply the ID if you choose SHARED or ARCHITECTURE).

---

> SHARED

You chose SHARED — please provide the exact Domain ID (the <domain-id> string). I cannot infer it.

Please reply with the Domain ID exactly as it appears (it will map to shared-knowledge/<domain-id>/). 

After you supply the Domain ID I will immediately:
1. Resolve the mutable authority namespace to shared-knowledge/<domain-id>/.
2. Read that namespace’s control-plane files in 00-control/ (CONTEXT.md, CURRENT_STATE.md, BASELINE.md, DOCUMENT_INDEX.md, OPEN_QUESTIONS.md, NEXT_ACTIONS.md, SESSION_HANDOFF.md).
3. Read required governance and decisions files under governance/ and decisions/.
4. Use DOCUMENT_INDEX.md and the control-plane to retrieve any additional relevant artifacts.
5. Then summarize: Operating Scope; Mutable authority namespace; Current state; Baseline state; Ordered work (or NOT ESTABLISHED); Resume state (or NOT ESTABLISHED); materially relevant unresolved questions.

Provide the Domain ID to continue.

---

> banane

Summary (direct): the SHARED namespace you selected, shared-knowledge/banane/, is not present in the repository — its control-plane and governance artifacts are missing.

What I did:
- Attempted to read shared-knowledge/banane/00-control/CONTEXT.md and other control-plane files and found the path does not exist.

Current findings / state (authoritative, not inferred):
- Operating Scope: SHARED
- Mutable authority namespace: shared-knowledge/banane/
- Namespace presence: NOT FOUND (no filesystem path at shared-knowledge/banane/)
- Control-plane files (required) — all MISSING:
  - 00-control/CONTEXT.md
  - 00-control/CURRENT_STATE.md
  - 00-control/BASELINE.md
  - 00-control/DOCUMENT_INDEX.md
  - 00-control/OPEN_QUESTIONS.md
  - 00-control/NEXT_ACTIONS.md
  - 00-control/SESSION_HANDOFF.md
- Required governance files — MISSING:
  - governance/ASSUMPTIONS.md
  - governance/CONSTRAINTS.md
  - governance/PRINCIPLES.md
- Decisions file — MISSING:
  - decisions/DECISION_REGISTER.md

Baseline state: NOT ESTABLISHED (no BASELINE.md present)
Ordered work (NEXT_ACTIONS): NOT ESTABLISHED
Resume state (SESSION_HANDOFF): NOT ESTABLISHED

Materially relevant unresolved questions:
1. Do you confirm the Domain ID is exactly "banane" (i.e., shared-knowledge/banane/) and want that to be the mutable authority namespace?
2. Do you want me to initialize the namespace now by creating the required 00-control/, governance/, and decisions/ files with initialized-empty content per the framework schema?
3. If yes, do you want default initialized-empty placeholders (using NOT ESTABLISHED / NONE / explicit initialized-empty semantics) or do you want to provide initial content for any of the control-plane files?

Next (action choice needed): please confirm one option:
- A: Yes — initialize shared-knowledge/banane/ control-plane and governance skeleton now (I will then create the files).
- B: No — do not create files; keep the namespace absent and proceed read-only / stop.
- C: Initialize but provide content (reply with which control-plane files you want prefilled and their content).

I’ll proceed immediately based on your choice.

---

> Sorry, wrong name, I select `ghe_copilot`.

Operating Scope: SHARED

Mutable authority namespace: shared-knowledge/ghe_copilot/

Control-plane and governance summary (authoritative file contents):

- 00-control/CONTEXT.md
  - Namespace Type: SHARED
  - Domain ID: ghe_copilot
  - Name: GitHub Enterprise and Copilot
  - Purpose: NOT ESTABLISHED
  - Scope: NOT ESTABLISHED
  - Boundaries: NOT ESTABLISHED
  - Source / Provenance: NOT ESTABLISHED
  - Applicability: NOT ESTABLISHED

- 00-control/CURRENT_STATE.md
  - Current State: NOT ESTABLISHED

- 00-control/BASELINE.md
  - Baseline Status: NOT ESTABLISHED
  - No baseline members recorded

- 00-control/DOCUMENT_INDEX.md
  - Lists the namespace’s owned artifacts (control-plane, governance, decisions) and references FRAMEWORK artifacts (framework/REPOSITORY_CONTEXT.md, framework/DOCUMENT_SCHEMA.md, framework/AI_OPERATING_MODEL.md)

- 00-control/OPEN_QUESTIONS.md
  - No open questions recorded

- 00-control/NEXT_ACTIONS.md
  - Ordered Work: NOT ESTABLISHED

- 00-control/SESSION_HANDOFF.md
  - Resume State: NOT ESTABLISHED

- governance/ASSUMPTIONS.md
  - No assumptions recorded

- governance/CONSTRAINTS.md
  - No constraints recorded

- governance/PRINCIPLES.md
  - No principles recorded

- DOCUMENT_INDEX.md also lists decisions/DECISION_REGISTER.md as an owned artifact (registry presence recorded in the index)

Baseline state: NOT ESTABLISHED

Ordered work: NOT ESTABLISHED

Resume state: NOT ESTABLISHED

Materially relevant unresolved items (explicit states preserved as recorded):
- Namespace Purpose is NOT ESTABLISHED
- Namespace Scope is NOT ESTABLISHED
- Namespace Boundaries are NOT ESTABLISHED
- Source / Provenance is NOT ESTABLISHED
- Applicability is NOT ESTABLISHED
- Current-state summary is NOT ESTABLISHED
- Baseline membership is NOT ESTABLISHED
- Ordered work is NOT ESTABLISHED
- Resume point is NOT ESTABLISHED
- No governance content (assumptions/constraints/principles) recorded
- No open questions recorded (the open-questions registry is empty)

All states above are reported exactly as recorded in the repository; missing or "NOT ESTABLISHED" values are preserved verbatim.

---

> With this session I want to explore GitHub Enterprise with Copilot from perhaps 2 different point of view:
> 1. As administrator of the company's GitHub Enterprise.
> 2. As a new User, learning the 101 of GitHub Copilot with the context of GitHub Enterprise.
> If these are somewhat too much together in one chat session and/or even within a single shared-knowledge domain, they could be broken up and separated individually.
> Comment/suggestions.

Direct answer / recommendation:
- Keep a single SHARED namespace (shared-knowledge/ghe_copilot) and model the two perspectives as separate topics (topics/admin and topics/user101). This preserves one authority namespace while keeping content, governance, and work clearly separated. Only split into separate namespaces if you require different ownership, different baseline processes, or different governance for each perspective.

What I reviewed and why that matters:
- I read the framework contracts and the ghe_copilot control-plane files you already have. The namespace exists but is initialized-empty in most places (Purpose, Scope, Baseline, NEXT_ACTIONS, etc.). That makes it easy and safe to add topic-level content and an ordered work plan without changing framework assumptions.

How I suggest we structure work (practical, minimal-change approach)
1. Keep authority: shared-knowledge/ghe_copilot/ (mutable for this session).
2. Add two topics:
   - shared-knowledge/ghe_copilot/topics/admin/ — artifacts for the Administrator POV.
   - shared-knowledge/ghe_copilot/topics/user101/ — artifacts for the New User POV.
3. Update control-plane minimally:
   - 00-control/CONTEXT.md — fill Purpose and Scope (one-liner).
   - 00-control/DOCUMENT_INDEX.md — add entries for the two topics and planned artifacts.
   - 00-control/NEXT_ACTIONS.md — add an ordered work list (see below).
   - 00-control/OPEN_QUESTIONS.md — record blocking/unknown items (see below).
   - Keep CURRENT_STATE.md / BASELINE.md as NOT ESTABLISHED until you want to lock baseline membership.

Suggested initial NEXT_ACTIONS (ordered, short):
1. Define Context: fill CONTEXT.md Purpose, Scope, Boundaries (1).
2. Create topic skeletons: admin and user101 with README.md (2).
3. Populate admin topic with: Enterprise setup checklist (SSO, SCIM, org/repo structure, licensing, policies, provisioning, audit logs) (3).
4. Populate user101 topic with: onboarding guide, installing Copilot, editor integrations, first prompts, privacy/telemetry notes (4).
5. Capture Open Questions (licenses, telemetry, data residency, allowed inference policies) (5).
6. Add decision/register entries for any policy decisions we make (6).
7. Run a gap analysis vs. official GitHub Enterprise docs and list required local customizations (7).
8. Create a short admin runbook for incidents related to Copilot (exposed secrets, hallucinations, license violations) (8).

Suggested Open Questions to record now (examples to put in OPEN_QUESTIONS.md)
- Which GitHub product: GitHub Enterprise Cloud, GitHub Enterprise Server, or both?
- What Copilot licensing model and seat counts are available/approved?
- Are there SSO/SCIM integrations required (IdP vendor, provisioning rules)?
- Data residency & telemetry: are we allowed to send code snippets to Copilot? Any policy constraints?
- Which organizations/repos are in-scope for Copilot by default vs. opt-in/opt-out?
- Acceptable use / code exposure policies (e.g., secrets, PII).
- Who is the owner for decisions about Copilot defaults and retention?

Key artifacts I recommend creating under each topic
- admin:
  - ADMIN_CHECKLIST.md (SSO, provisioning, org & repo layout, policy mapping, license tracking)
  - ADMIN_RUNBOOKS/ (incident playbooks)
  - ADMIN_CONFIG_EXAMPLES/ (sample org settings, policy templates)
  - SECURITY_ASSESSMENT.md (risks, mitigations)
- user101:
  - ONBOARDING.md (how to enable Copilot, supported editors, first steps)
  - HOWTO_PROMPTS.md (examples, good/bad prompts)
  - FAQ.md (privacy, what Copilot is/isn't)
  - TUTORIALS/ (short tasks: create PR with Copilot, use in Codespaces)

Operational suggestions and boundaries
- Don’t treat topic content as changing authority outside the shared namespace. If an Architecture or other Shared domain needs changes, handle in a separate scoped session.
- Preserve NOT ESTABLISHED where unknown — record it in control-plane so decisions and future work are auditable.
- Start lightweight: skeletons + index + open-questions + one short admin checklist draft. Expand after decisions.

Next actions for me (pick one)
A) Initialize topic skeletons and update DOCUMENT_INDEX.md and NEXT_ACTIONS.md for you now (I will create the files with initialized-empty placeholders and the ordered work list above).
B) Do not create files; instead I draft a short admin checklist or user onboarding doc here in chat.
C) Start with exploration: I can research specific technical items (e.g., "Copilot licensing for Enterprise Cloud" or "SSO/SCIM setup for GitHub Enterprise Server") and report findings (this requires internet — I can run searches).
D) Split sessions: create two separate scoped sessions (two mutable namespaces) — choose only if you want separate authority ownership.

Which would you like me to do next? If A or B, tell me whether to create files directly in the repository (I will then write them into shared-knowledge/ghe_copilot/). If C, tell me which technical question to research first. If D, say which namespace(s) and owners you want.

---















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