# mosaic

> A combination of many diverse parts that come together to form a cohesive whole.

## Purpose

`mosaic` is a portable, self-describing, AI-assisted Solution Architecture knowledge repository framework.

It is designed so that a human or repository-aware AI can enter a fresh session, determine where authority lives, reconstruct durable work state, and continue correctly without depending on prior chat history.

<!-- what is authority here -->

## Repository Map

```text
mosaic/
├── README.md
├── architectures/                     container
│   ├── README.md
│   └── <architecture-id>/             ARCHITECTURE authority
├── framework/                         FRAMEWORK authority
│   ├── README.md
│   ├── REPOSITORY_CONTEXT.md
│   ├── DOCUMENT_SCHEMA.md
│   ├── AI_OPERATING_MODEL.md
│   ├── VALIDATION_PROTOCOL.md
│   ├── 00-control/
│   └── templates/
└── shared-knowledge/                  container
    ├── README.md
    └── <domain-id>/                   SHARED authority
```

`architectures/` and `shared-knowledge/` are navigation containers only. Authority begins in their direct child namespaces.

## Three Operating Scopes

### `ARCHITECTURE`

Use this when the work belongs to one Solution Architecture. You must explicitly identify the Architecture ID, which resolves to:

```text
architectures/<architecture-id>/
```

### `SHARED`

Use this when the work belongs to one reusable knowledge domain. You must explicitly identify the Domain ID, which resolves to:

```text
shared-knowledge/<domain-id>/
```

Shared means reusable; it does not mean universally applicable.

### `FRAMEWORK`

Use this only when changing or maintaining the repository framework itself: authority semantics, schema, templates, validation, Framework documentation, or Framework control state.

User-requested Framework repository changes are developed on a non-`main` working branch. Direct working edits to `main` are prohibited; integration to `main` is an explicit later step governed by the Framework operating model.

## Authority Model

> Authority namespace determines the authority boundary; topic determines the retrieval boundary.

Every AI-assisted working session has exactly one mutable authority namespace. Other namespaces may be read for relevant context, but they remain read-only unless separately selected in another working session.

## Starting documentation to navigate:

The README files are onboarding and navigation guides. They explain how to use the repository but are not intended to duplicate every normative rule.

1. Use this `README` to select the area of work.
2. Use `framework/README.md` to understand framework mechanics.
3. Use `architectures/README.md` or `shared-knowledge/README.md` to enter an authority namespace.

## Normative Contracts

The stable Framework contracts are authoritative for repository semantics:

1. `framework/REPOSITORY_CONTEXT.md` — repository meaning and namespace model.
2. `framework/DOCUMENT_SCHEMA.md` — structure, metadata, classification, status, authority, and baseline conventions.
3. `framework/AI_OPERATING_MODEL.md` — AI-assisted session initialization, authority handling, response behavior, and Framework mutation safety.
4. `framework/VALIDATION_PROTOCOL.md` — formal fresh-session validation procedure.

If a README or convenience prompt conflicts with those contracts, the Framework contracts govern.

## Starting Examples

You do not need to understand the full Framework model before using the repository. Start with what you want to do.

| I want to... | Start here | AI scope / next step |
|---|---|---|
| Work on an existing Solution Architecture | `architectures/README.md`, then choose an explicit Architecture ID | `ARCHITECTURE` |
| Work on reusable knowledge shared across solutions | `shared-knowledge/README.md`, then choose an explicit Domain ID | `SHARED` |
| Change or maintain `mosaic` itself | `framework/README.md` | `FRAMEWORK` |
| Create a new Architecture or Shared namespace | `framework/templates/README.md` | Follow the creation guidance; after creation, substantive work uses the resulting `ARCHITECTURE` or `SHARED` scope |
| Start my first AI-assisted chat | `framework/templates/SESSION_BOOTSTRAP_PROMPT.md` | Selected interactively |

If you are unsure which namespace applies, do not guess. The AI bootstrap flow is designed to ask for the Operating Scope and any required namespace ID explicitly.

### First AI-Assisted Session

1. Open a fresh chat or equivalent AI workspace that can read this repository.
2. Copy the canonical prompt from `framework/templates/SESSION_BOOTSTRAP_PROMPT.md`.
3. The AI reads the stable Framework contracts first.
4. The AI asks you to select exactly one Operating Scope: `FRAMEWORK`, `SHARED`, or `ARCHITECTURE`, unless you already supplied it explicitly.
5. For `SHARED`, provide the Domain ID. For `ARCHITECTURE`, provide the Architecture ID. `FRAMEWORK` requires no namespace ID.
6. The AI reconstructs the selected authority namespace from durable repository state and reports its current state, ordered work, resume state, and other required initialization information before substantive work begins.

You may include your intended task or topic in the first prompt, but the task does not authorize the AI to infer an unstated scope or namespace ID.

## Durable Continuity

Repository durable state, not chat memory, is the source of continuity.

A new session should be able to reconstruct the selected authority namespace from its control plane. Missing or explicitly unestablished state is valid state and must not be filled from prior conversations, model memory, another namespace, or inference.