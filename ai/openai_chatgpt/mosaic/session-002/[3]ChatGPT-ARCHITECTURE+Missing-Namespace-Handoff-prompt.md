# 3 — ChatGPT / ARCHITECTURE + Missing-Namespace Handoff

Validate the `mosaic` repository using a fresh, read-only AI-assisted session.

Repository: `dsoguy/mosaic`
Validation target: `main @ f61aa2d124fd6e9a683c8c5fea5459a1cd6a1116`

Use repository artifacts only as authority. Do not rely on prior chat history.

Begin as a bootstrap-interaction validation with:

Operating Scope = `ARCHITECTURE`
Architecture ID = `banane`

`banane` is intentionally used to exercise missing-namespace behavior.

Validate that you:
* do not initialize a nonexistent Architecture namespace;
* clearly report that the requested namespace does not exist;
* list existing Architecture IDs when repository access permits;
* do not silently choose another Architecture ID;
* do not create repository structure;
* do not silently switch this session to `FRAMEWORK`;
* offer the separate Framework namespace-creation setup path;
* provide a concise copy/paste-ready next-session instruction that preserves:
  * repository identity;
  * `Operating Scope = FRAMEWORK`;
  * requested setup = creation of an `ARCHITECTURE` namespace;
  * Architecture ID = `banane`;
* make clear that the handoff does not bypass Framework initialization, branch, lock, review, or mutation-safety rules.

After completing that missing-namespace validation, continue this same read-only session using:

Architecture ID = `ADOPT`

Initialize `ARCHITECTURE / ADOPT` and validate that:
* `architectures/ADOPT/` is the one mutable authority namespace;
* all other authority namespaces remain read-only;
* ADOPT current state, baseline, ordered work, handoff/resume state, unresolved questions, governance, and decisions are reconstructed correctly;
* explicit states such as `NONE`, `NOT ESTABLISHED`, `CANDIDATE`, `ACTIVE`, `OPEN`, or `BLOCKED` are preserved where established;
* Framework lifecycle or mutable Framework state is not incorrectly promoted into ADOPT authority.

Do not modify the repository or advance durable state.

At the end, report:
1. `PASS`, `PASS WITH FINDINGS`, or `FAIL`;
2. blocking findings;
3. non-blocking findings;
4. observations or known harness limitations;
5. whether the nonexistent-ID and actionable Framework-handoff behavior matched the Framework contract.
