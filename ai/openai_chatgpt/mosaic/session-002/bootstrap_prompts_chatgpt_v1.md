# First-session bootstrap prompt for ChatGPT

Initialize this mosaic repository as a new AI-assisted working session.
Do not rely on prior chat history as authority.
First, read and interpret the stable Framework contracts:
1. `framework/REPOSITORY_CONTEXT.md`
2. `framework/DOCUMENT_SCHEMA.md`
3. `framework/AI_OPERATING_MODEL.md`

Use those repository artifacts as the authoritative operating model for this session.
Do not select an Operating Scope or authority namespace on my behalf.
After reading the Framework contracts, stop and ask me to select exactly one Operating Scope:
- `FRAMEWORK`
- `SHARED`
- `ARCHITECTURE`

If I select `SHARED`, ask me for the Domain ID.
If I select `ARCHITECTURE`, ask me for the Architecture ID.
If I select `FRAMEWORK`, no namespace ID is required.

Do not infer an unstated Domain ID or Architecture ID from repository contents, previous conversations, apparent relevance, or model memory.

After I provide the Operating Scope and any required namespace ID:
1. Establish exactly one mutable authority namespace;
2. Load that namespace's authoritative control state according to `framework/AI_OPERATING_MODEL.md`;
3. Load its relevant governance and decision state;
4. Retrieve baseline, topic, or other namespace content only as needed for the task;
5. Treat every other authority namespace as read-only;
6. Preserve source namespace, classification, status, authority, applicability, and provenance when retrieving external material;
7. Do not use another namespace's state to fill missing state in the selected namespace;
8. Preserve `NONE`, `NOT ESTABLISHED`, unresolved, candidate, or other explicit states without inference;
9. Treat repository durable state—not chat memory—as the source of continuity.

Optional namespace-specific AI configuration may specialize behavior only after repository authority has been established and may not override Framework contracts or namespace authority state.

Before beginning substantive work, report briefly:
- Selected Operating Scope;
- Selected authority namespace;
- Current state;
- Baseline state, if applicable;
- Ordered work, if established;
- Resume state, if established;
- Unresolved questions materially relevant to the requested task.

If no ordered work or resume point is established, report that explicitly rather than inventing one.
Begin by reading the three Framework contracts, then ask me to select the Operating Scope.

# End first-session bootstrap prompt for ChatGPT

<!--
# Document Control

**Last Updated:** v1

**Change Log:**

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-08-28 | DSOt | Initial version |
-->
