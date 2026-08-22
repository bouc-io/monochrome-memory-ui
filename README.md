# monochrome-memory-ui

React/Vite web UI for **memory-api-server** — browse, search, and manage the
agent's long-term memories (pgvector semantic search over stored memories).

Part of the [bouc.io AI platform](../../../documentation/getting-started/README.md#ai-assistant-platform).

## Features

- Semantic + keyword search across stored memories
- Inspect memory category (persona/preference/fact/instruction/context) and importance
- Create, edit, and delete memories
- Keycloak SSO auth, or `stub` mode for local dev
- Built with React, TypeScript, Vite, shadcn-ui, and Tailwind CSS

## Prerequisites

- Node.js 18+ and npm
- A running `memory-api-server` (see its README)

## Setup & Run

```sh
npm install
cp .env.example .env      # then edit values
npm run dev               # dev server at http://localhost:8080
```

## Build & Test

```sh
npm run build             # production build -> dist/
npm run build:dev         # dev-mode build
npm run preview           # preview the production build
npm run lint              # ESLint
npm run test              # Vitest
```

## Environment

All config is via `VITE_*` variables — see [`.env.example`](./.env.example) for the
full list (backend API URL, Keycloak SSO, identity-provider mode, dev tokens).

## Project structure

- `src/pages/` — top-level pages
- `src/components/` — UI components
- `src/context/` — auth / theme / language providers
- `src/hooks/` — custom hooks
- `src/lib/` — API utilities

## License

[Elastic License 2.0](./LICENSE) — source-available; not OSI open source.
