# FlowSurgeon

**Redesign the work before automating it.**

FlowSurgeon is a local-first, human-in-the-loop process redesign canvas built for the OpenAI WebMCP Challenge 2026. It gives a human and a browser agent a shared, structured view of the same workflow. The agent can inspect, analyze, focus, and prepare semantic change proposals; only the human can approve and apply them.

## Project status

Architecture and competition-compliance baseline approved. Product implementation has not started yet.

## Why WebMCP

Traditional agents must infer workflow state from pixels or depend on a separate backend integration. FlowSurgeon exposes precise page-native tools through `document.modelContext.registerTool()`, allowing an agent to work with the active process while both participants observe the same interface and state.

The MVP defines seven tools:

1. `get_process_overview`
2. `get_process_elements`
3. `analyze_process`
4. `focus_process_elements`
5. `create_change_proposal`
6. `get_change_proposal`
7. `revise_change_proposal`

Approval, application, deletion, import, export, restoration, and protection changes remain human-only actions.

## Architecture

- React 19 and strict TypeScript
- Vite
- React Flow
- Zustand
- Zod
- Dexie and IndexedDB
- Vitest, Testing Library, fast-check, Playwright, and axe-core
- Static Vercel deployment
- No account, backend, API key, analytics, or embedded AI service

See the [complete architecture specification](docs/architecture/architecture.md) and [technical architecture diagram](docs/architecture/technical-architecture.svg).

## Challenge timeline

This repository is being created during the official WebMCP Challenge submission period. The dated development record is maintained in [CHALLENGE_TIMELINE.md](docs/submission/CHALLENGE_TIMELINE.md).

## Development

Implementation commands will be added with the application scaffold. Until then, this repository is intentionally documentation-only and makes no runnable-product claim.

## License

FlowSurgeon is released under the [MIT License](LICENSE). Third-party components and assets are tracked separately in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
