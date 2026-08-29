# First-session bootstrap prompt for GitHub Copilot

Initialize this repository according to the mosaic Framework before performing any substantive work.
Treat repository artifacts as authoritative. Do not infer current repository state from previous chat messages, general model knowledge, or assumptions about the project.
First inspect:
1. `framework/REPOSITORY_CONTEXT.md`
2. `framework/DOCUMENT_SCHEMA.md`
3. `framework/AI_OPERATING_MODEL.md`

Follow those files as the repository operating contract.
Do not automatically select a project, architecture, Shared domain, folder, or working scope based on the files currently open in the editor.
After reading the Framework contracts, ask me to select exactly one Operating Scope:
- `FRAMEWORK`
- `SHARED`
- `ARCHITECTURE`

If I choose `SHARED`, ask for the Domain ID.
If I choose `ARCHITECTURE`, ask for the Architecture ID.
If I choose `FRAMEWORK`, no namespace ID is required.

Do not infer a missing namespace ID.

After I select the scope:
1. Establish exactly one mutable authority namespace;
2. Read that namespace's control-plane artifacts before making repository changes;
3. Read relevant governance and decision artifacts;
4. Use its document index and task context to retrieve additional material as needed;
5. Keep all other authority namespaces read-only;
6. Do not modify another namespace as a side effect of the current task;
7. Do not treat retrieval as ownership or applicability;
8. Preserve explicit unknown, empty, candidate, unresolved, baseline, and decision states exactly as represented by repository authority;
9. Never manufacture missing state from another namespace, repository history, model knowledge, or file presence.

Optional namespace AI configuration may guide behavior only after Framework and namespace authority have been established. It cannot override Framework contracts or authoritative namespace state.

Before editing or implementing anything, summarize:
- Operating Scope;
- Mutable authority namespace;
- Current state;
- Baseline state where applicable;
- Ordered work, if established;
- Resume state, if established;
- Materially relevant unresolved questions.

If no ordered work or resume point exists, report `NOT ESTABLISHED` rather than choosing work yourself.
Do not make repository changes until the Operating Scope and required namespace ID have been explicitly supplied.
Begin by inspecting the three Framework contracts, then ask me to choose the Operating Scope.

# End first-session bootstrap prompt for GitHub Copilot

<!--
# Document Control

**Last Updated:** v1

**Change Log:**

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-08-28 | DSOt | Initial version |
-->
