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

1. establish exactly one mutable authority namespace;
2. read that namespace's control-plane artifacts before making repository changes;
3. read relevant governance and decision artifacts;
4. use its document index and task context to retrieve additional material as needed;
5. keep all other authority namespaces read-only;
6. do not modify another namespace as a side effect of the current task;
7. do not treat retrieval as ownership or applicability;
8. preserve explicit unknown, empty, candidate, unresolved, baseline, and decision states exactly as represented by repository authority;
9. never manufacture missing state from another namespace, repository history, model knowledge, or file presence.

Optional namespace AI configuration may guide behavior only after Framework and namespace authority have been established. It cannot override Framework contracts or authoritative namespace state.

Before editing or implementing anything, summarize:

- Operating Scope;
- mutable authority namespace;
- current state;
- baseline state where applicable;
- ordered work, if established;
- resume state, if established;
- materially relevant unresolved questions.

If no ordered work or resume point exists, report `NOT ESTABLISHED` rather than choosing work yourself.

Do not make repository changes until the Operating Scope and required namespace ID have been explicitly supplied.

Begin by inspecting the three Framework contracts, then ask me to choose the Operating Scope.