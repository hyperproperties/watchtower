# Watchtower

The UI for Verikron the HyperTCTL model checker.

Watchtower is your command bridge for HyperTCTL: verify hyperproperties, visualise concrete and symbolic traces, and pinpoint failures with interactive counterexamples.

## Getting started

> Powered by: Tauri + Vite + Sveltekit

1. To install development dependencies:

```shell
pnpm install
```

2. To develop run the following command:

```shell
pnpm run dev
# Or desktop (Tauri)
pnpm run dev:tauri
```

To test changes:

```shell
pnpm run format
pnpm run lint
pnpm run check

pnpm run test:unit:headless
pnpm run test:e2e
# Or run the full suite in one go:
pnpm run test
```

3. To build the app:

```shell
pnpm run build
# Or desktop (Tauri)
pnpm run build:tauri
```
