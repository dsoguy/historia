# First-session bootstrap prompt for Claude

Initialize this mosaic repository as a new AI-assisted working session using repository artifacts as the durable source of authority.
Do not rely on prior conversation history as repository authority.
First, read:
1. `framework/REPOSITORY_CONTEXT.md`
2. `framework/DOCUMENT_SCHEMA.md`
3. `framework/AI_OPERATING_MODEL.md`

Interpret those files as the stable Framework contracts governing repository scope, ownership, mutation authority, retrieval, continuity, classification, baseline behavior, and missing-information handling.
Do not choose an authority namespace yet.
After reading those contracts, stop and ask me to select exactly one Operating Scope:
- `FRAMEWORK`
- `SHARED`
- `ARCHITECTURE`

For `SHARED`, ask me for the Domain ID.
For `ARCHITECTURE`, ask me for the Architecture ID.
For `FRAMEWORK`, no namespace ID is required.

Never infer an unstated Domain ID or Architecture ID from file names, repository inventory, prior conversation, likely intent, or model knowledge.

Once I make the selection:
1. Resolve it to exactly one mutable authority namespace;
2. Reconstruct that namespace from its durable control-plane artifacts;
3. Load relevant namespace governance and decisions;
4. Retrieve additional local content only as required by the task;
5. Treat Framework mutable state and every unselected Shared or Architecture namespace as read-only unless `FRAMEWORK` itself is selected;
6. Distinguish retrieval from applicability, ownership, and mutation authority;
7. Preserve the source authority namespace and its classification, status, provenance, and applicability when external material is consulted;
8. Never substitute external or historical state for missing state in the selected namespace;
9. Retain explicit `NONE`, `NOT ESTABLISHED`, `OPEN`, `BLOCKED`, `CANDIDATE`, or equivalent repository states without silently resolving or promoting them.

If the selected namespace contains optional AI configuration, load it only after Framework and namespace authority have been established. Such configuration is behavioral guidance and cannot override repository authority.

Before substantive work begins, provide a concise reconstruction containing:
- Operating Scope;
- Selected authority namespace;
- Current authoritative state;
- Baseline state where applicable;
- Ordered work, if any;
- Durable resume state, if any;
- Materially relevant unresolved questions.

If ordered work or a resume state is not established, say so explicitly.
Begin now by reading the three Framework contracts. Then ask me which Operating Scope I want to use.

# End first-session bootstrap prompt for Claude

<!--
# Document Control

**Last Updated:** v1

**Change Log:**

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-08-28 | DSOt | Initial version |
-->
