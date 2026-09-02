# 4 — ClaudeAI / Cross-Model Spot Check

Perform an independent, fresh, read-only validation of the `mosaic` repository.

Repository: `dsoguy/mosaic`
Validation target: `main @ f61aa2d124fd6e9a683c8c5fea5459a1cd6a1116`
Operating Scope: `ARCHITECTURE`
Architecture ID: `ADOPT`

Use repository artifacts only as authority. Do not rely on prior conversations, memory, or another AI model's validation results.

If your repository interface does not expose the exact Git commit SHA, do not infer or claim that you independently verified it. The validation coordinator has pinned the target out-of-band. Report any observable repository-content inconsistency with the declared target.

Read the stable Framework contracts first, then initialize `ARCHITECTURE / ADOPT` according to the current operating model.

Validate that:
* exactly one mutable authority namespace is established: `architectures/ADOPT/`;
* Framework, Shared, and other Architecture namespaces remain read-only;
* ADOPT authoritative current state, baseline, ordered work, resume state, unresolved questions, governance, and decisions are reconstructed correctly;
* explicit governed states are preserved and not inferred away;
* cross-namespace retrieval does not transfer authority;
* Framework mutable state is not confused with Architecture state;
* the current model uses `FRAMEWORK`, `SHARED`, and `ARCHITECTURE` scopes only and does not resurrect historical `COMBINED` semantics;
* initialization reporting follows the information contract in `framework/AI_OPERATING_MODEL.md`.

Do not modify the repository or advance durable state.

At the end, report:
1. `PASS`, `PASS WITH FINDINGS`, or `FAIL`;
2. blocking findings;
3. non-blocking findings;
4. observations;
5. client/harness limitations, especially Git SHA visibility;
6. the authoritative ADOPT state you reconstructed.
