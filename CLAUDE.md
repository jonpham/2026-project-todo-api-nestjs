# CLAUDE.md — todo-api-nestjs

> Loaded automatically at the start of every session.

---

## Working Context

**This repo is a downstream mirror of the monorepo.**

All development happens in the monorepo at `jonpham/2026-project-todo-skeleton-monorepo`
under `apps/todo-api-nestjs/`. After merging to monorepo `main`, the `sync-subtrees-push.yml`
workflow pushes changes here automatically via `git subtree split`.

**Do not open Claude in this repo.** Open it in the monorepo instead.
**Do not make changes here directly** — they will be overwritten on the next monorepo push.

---

## Purpose

Standalone NestJS v11 REST API skeleton — independently deployable template demonstrating
a production-ready API structure with TypeScript strict mode, Prisma + SQLite, Vitest
testing, ESLint flat config, Prettier, and Husky pre-commit hooks. Usable as a template
for future projects of similar type.

**Monorepo:** `github.com/jonpham/2026-project-todo-skeleton-monorepo` (source of truth)
**This repo:** `github.com/jonpham/2026-project-todo-api-nestjs` (deployable mirror)

---

## Code Standards

### TypeScript

- Strict mode throughout (`strict: true`, `noImplicitAny`, `strictNullChecks`)
- `ES2022` target, `NodeNext` module resolution
- Decorators enabled (`emitDecoratorMetadata`, `experimentalDecorators`)

### Linting & Formatting

- ESLint flat config (`eslint.config.js`)
- Prettier with double quotes, `es5` trailing commas, 2-space indent, 80-char width
- Pre-commit hook via Husky + lint-staged

### Testing

- Vitest for unit and integration tests
- Run: `pnpm test`

---

## CI

| Workflow | Trigger                 | What it does      |
| -------- | ----------------------- | ----------------- |
| `ci.yml` | Push / PR to any branch | Lint, test, build |

---

## Project Structure

```
todo-api-nestjs/
├── src/
│   ├── main.ts
│   ├── app.module.ts
│   ├── health/
│   ├── todos/
│   └── prisma/
├── prisma/
│   └── schema.prisma
├── docs/
│   └── features/
├── .github/
│   └── workflows/
│       └── ci.yml
└── .env.example
```
