# GoIT Advanced JavaScript — Homework 05

Introduction to TypeScript: project compiler setup, `src/` → `dist/`, and source maps for browser debugging.

## Source files

- [`src/index.ts`](src/index.ts)
- [`src/concatenation.ts`](src/concatenation.ts)
- [`tsconfig.json`](tsconfig.json)

## Setup

```bash
bun install
bun run build
```

`sourceMap: true` in `tsconfig.json` emits `.js.map` files next to compiled JavaScript so DevTools can map breakpoints to TypeScript sources.

## Run

```bash
bun run start
```

Opens the app with `@web/dev-server` (required for ES modules; `file://` will fail with CORS).

Watch TypeScript in a second terminal:

```bash
bun run build:watch
```

## Debug

1. Open DevTools → **Sources**.
2. Find `src/concatenation.ts` (via source maps).
3. Set a breakpoint and click **Concat!** — execution pauses on TypeScript lines.
