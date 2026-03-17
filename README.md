# national claude day

a small fan-canon website for an entirely unofficial holiday.

the site counts down to the next local march 14 reset, keeps a playful lowercase handwritten visual style, and includes a few extra pages about claude lore, favorite things, protocol, and age.

## what it is

- a tanstack start app inside a better-t-stack monorepo
- a countdown that resets every march 14 at local midnight
- a tiny multi-page site with:
  - `countdown`
  - `about claude`
  - `favorite things`
  - `protocol`
  - `how old is claude?`
- a shared shadcn/ui package in `packages/ui`

## stack

- `bun`
- `typescript`
- `tanstack start` + `tanstack router`
- `tailwindcss`
- `shadcn/ui` shared through `packages/ui`
- `turborepo`
- `oxlint` + `oxfmt`

## local development

install dependencies:

```bash
bun install
```

run the app:

```bash
bun run dev
```

the web app is available at `http://localhost:3001`.

## scripts

```bash
bun run dev        # run the repo in dev mode
bun run dev:web    # run only the web app
bun run build      # production build
bun run check      # lint + format
```

## project structure

```text
claudeday/
├── apps/
│   └── web/
│       ├── src/routes/        # site pages
│       ├── src/components/    # page shell + shared app components
│       └── src/hooks/         # countdown / age logic
├── packages/
│   └── ui/                    # shared shadcn/ui primitives
```

## notes

- the march 14 holiday framing is fan canon, not official anthropic canon
- claude age references are based on the public march 2023 launch timeline
- theme tokens live in `packages/ui/src/styles/globals.css`

## design direction

the current site aims for:

- dark, minimal, and full-screen
- handwritten lowercase display text
- simple framing and light lore instead of dense product copy

## deployment

this repo does not require any backend setup for the current site. a plain frontend deployment is enough after `bun run build`.
