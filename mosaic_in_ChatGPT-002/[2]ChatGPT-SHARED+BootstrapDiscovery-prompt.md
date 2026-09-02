# 2 — ChatGPT / SHARED + Bootstrap Discovery

Validate the `mosaic` repository using a fresh, read-only AI-assisted session.

Repository: `dsoguy/mosaic`
Validation target: `main @ f61aa2d124fd6e9a683c8c5fea5459a1cd6a1116`

Use repository artifacts only as authority. Do not rely on prior chat history.

Begin as a bootstrap-interaction validation.

Operating Scope = `SHARED`

I am intentionally not supplying the Domain ID yet.

Follow the current `framework/AI_OPERATING_MODEL.md` behavior. Verify that you:
* do not infer a Domain ID;
* inspect `shared-knowledge/` read-only and list existing Domain IDs available for selection;
* let me choose rather than choosing for me.

After listing the available IDs, continue this same validation using: Domain ID = `IAM`

Then initialize `SHARED / IAM` and validate that:
* `shared-knowledge/IAM/` is the one mutable authority namespace;
* all other authority namespaces remain read-only;
* IAM current state, baseline state, ordered work, handoff/resume state, unresolved questions, and applicable governance are reconstructed correctly;
* initialized-empty or `NOT ESTABLISHED` state is preserved;
* repository presence or retrieved material is not incorrectly promoted into baseline or authority state;
* Framework mutable state is not treated as active Shared state.

Do not modify the repository or advance durable state.

At the end, report:
1. `PASS`, `PASS WITH FINDINGS`, or `FAIL`;
2. blocking findings;
3. non-blocking findings;
4. observations or known harness limitations;
5. whether missing-ID discovery behaved according to the Framework contract.
