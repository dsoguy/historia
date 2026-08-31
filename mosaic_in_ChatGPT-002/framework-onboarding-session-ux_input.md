# Feature-branch review session prompt

Initialize a new read-only `mosaic` Framework review session for repository `dsoguy/mosaic`.

Operating Scope: `FRAMEWORK`
Review target:
* Branch: `framework-onboarding-session-ux`
* Expected review snapshot: `13b09220aa9147af620cd19da55a5c078a6c7e06`
Comparison baseline:
* Branch: `main`
* Expected baseline snapshot: `52056f994b875c8976d5a62ebec8e1c5b7182c9e`

This is a HUMAN REVIEW support session, not an implementation session.

First read from the review target branch:
1. `framework/REPOSITORY_CONTEXT.md`
2. `framework/DOCUMENT_SCHEMA.md`
3. `framework/AI_OPERATING_MODEL.md`

Then load the relevant Framework control plane, including:
* `framework/00-control/CURRENT_STATE.md`
* `framework/00-control/NEXT_ACTIONS.md`
* `framework/00-control/SESSION_HANDOFF.md`
* `framework/00-control/DOCUMENT_INDEX.md`
* `framework/00-control/OPEN_QUESTIONS.md`
* `framework/00-control/WORKING_BRANCH_LOCK.md`

The branch has an active working-branch lock owned by another AI session.

Therefore:
* Treat `framework-onboarding-session-ux` as strictly READ-ONLY.
* Do not modify the branch.
* Do not modify `main`.
* Do not release or transfer the branch lock.
* Do not create or modify a pull request.
* Do not merge, rebase, advance, or otherwise integrate either branch.
* Do not update Framework control state.

If the observed review-target SHA differs from the expected snapshot and your client can verify commit identity, stop and report the mismatch before reviewing.

Treat the feature branch as PROPOSED Framework state under human review. Do not treat its contents as already integrated `main` authority.

The durable branch status is expected to be: `IN PROGRESS — AI PRE-MERGE REVIEW COMPLETE — HUMAN REVIEW PENDING`

Do not interpret AI pre-merge review as human review, approval, acceptance, validation, or authorization to merge.

Review the complete net change from `main` to `framework-onboarding-session-ux`, rather than relying on individual intermediate commits.

Assess:
1. first-time-user usability of the human-facing README files;
2. canonical first-session bootstrap prompt clarity and correctness;
3. consistency between the bootstrap prompt and `AI_OPERATING_MODEL.md`;
4. initialization-response contract;
5. substantive-work response contract, including conciseness;
6. branch-first Framework mutation safety;
7. exclusive working-branch lock semantics;
8. explicit AI-review → human-review → integration-authorization workflow;
9. consistency of `CURRENT_STATE.md`, `NEXT_ACTIONS.md`, and `SESSION_HANDOFF.md`;
10. validation-protocol coverage;
11. whether README/convenience documentation accidentally creates authority semantics not established by the Framework contracts;
12. unnecessary duplication, ambiguity, over-specification, portability concerns, or missing cases.

Keep the review concise.

Report:
* Review target and baseline
* Lock state
* Blocking findings
* Non-blocking findings
* Recommended remediation
* Overall review recommendation

For every finding, identify the affected artifact and explain why it matters.

Do not authorize integration. Human review completion and integration authorization will be handled explicitly outside this review session.

# End feature-branch review session prompt
