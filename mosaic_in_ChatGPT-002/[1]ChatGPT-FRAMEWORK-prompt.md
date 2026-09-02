# 1 — ChatGPT / FRAMEWORK

Validate the `mosaic` repository using a fresh, read-only AI-assisted session.

Repository: `dsoguy/mosaic`
Validation target: `main @ f61aa2d124fd6e9a683c8c5fea5459a1cd6a1116`
Operating Scope: `FRAMEWORK`

Use repository artifacts only as authority. Do not rely on prior chat history.

First read the stable Framework contracts required by `framework/AI_OPERATING_MODEL.md`, then initialize the session according to the current Framework contract.

Validate that:
* exactly one mutable authority namespace would be established: `framework/`;
* all Architecture and Shared namespaces remain read-only;
* Framework current state, ordered work, handoff state, and applicable governance are reconstructed correctly;
* Framework baseline is not confused with the Shared/Architecture `BASELINE.md` model;
* explicit repository states are preserved rather than inferred away;
* user-requested Framework mutations would require a non-`main` working branch before the first mutation;
* AI review, Human review, integration authorization, and formal validation remain distinct states;
* the active Framework branch-lock semantics are vendor-neutral.

Do not modify the repository or advance durable state.

At the end, report:
1. `PASS`, `PASS WITH FINDINGS`, or `FAIL`;
2. blocking findings;
3. non-blocking findings;
4. observations or known harness limitations;
5. the repository state you reconstructed.
