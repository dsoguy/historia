# Session Bootstrap Prompt

Initialize this repository according to `framework/AI_OPERATING_MODEL.md`.

## Inputs

Operating Scope: `<FRAMEWORK | SHARED | ARCHITECTURE>`
Namespace ID: `<domain-id | architecture-id | N/A>`
Task / Topic: `<optional>`

## Required Behavior

- Read the stable framework contracts first.
- Establish exactly one mutable authority namespace.
- For `SHARED` or `ARCHITECTURE`, require the explicit Namespace ID; do not infer it.
- Load the selected namespace control plane before substantive content.
- Treat all other authority namespaces as read-only.
- Use task/topic and document indexes to narrow retrieval.
- Preserve authority, classification, status, applicability, provenance, baseline state, and missing information.
- Apply optional namespace AI configuration only after durable authority is established.
- Do not use this prompt as a source of substantive repository truth.
