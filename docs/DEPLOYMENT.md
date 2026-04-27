# Deployment — todo-api-nestjs

> **Status:** Stub — deployment setup is deferred to Phase 4.

## Planned Deployment Target

- Docker container (Phase 4)
- Platform: TBD (Railway / Fly.io / AWS ECS)

## Environment Variables

Copy `.env.example` to `.env` and fill in production values before deploying.

| Variable | Description |
|---|---|
| `PORT` | Port the server listens on |
| `NODE_ENV` | Set to `production` |
| `DATABASE_URL` | Production database connection string |
| `JWT_SECRET` | Secure random secret for JWT signing |

## Build & Run (manual)

```bash
pnpm install --frozen-lockfile
pnpm build
node dist/main
```

## CI/CD

See `.github/workflows/ci.yml` for the automated lint + test + build pipeline.
Deployment automation will be added in Phase 4.
