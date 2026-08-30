# FlowSurgeon Agent Instructions

## Language

All source code, identifiers, comments, documentation, interface copy, accessibility text, errors, tests, fixtures, commit messages, pull request descriptions, Devpost materials, screenshots, and video narration must be written in English.

## Normative source

`docs/architecture/architecture.md` is the approved product and technical specification. Do not silently expand the MVP or reinterpret a mandatory requirement. Record any necessary architecture change as an explicit decision before implementing it.

## Human-control boundary

Agents may read, analyze, focus interface elements, and create or revise pending change proposals. Agents must never approve, apply, reject, delete, import, export, restore, protect, or unprotect process state. Human-only actions must not be exposed through WebMCP, URL parameters, hidden DOM actions, or indirect tool composition.

## Dependency rules

- The domain layer must remain pure and browser-independent.
- Application services may depend on domain types and ports.
- Infrastructure implements application ports.
- Presentation and WebMCP adapters call application services.
- React components must not access IndexedDB directly.
- WebMCP handlers must not contain domain rules.

## Implementation discipline

- Use strict TypeScript without `any` shortcuts.
- Validate external input at every boundary.
- Treat user-authored process content as untrusted.
- Preserve protected steps and their incident connections.
- Keep proposal application atomic and human-only.
- Add tests before or with each behavior change.
- Do not weaken tests, schemas, coverage thresholds, or security controls to make a check pass.

## Required verification

Before declaring implementation work complete, run the repository-defined formatting, linting, type-checking, unit, coverage, build, end-to-end, accessibility, and WebMCP contract checks.
