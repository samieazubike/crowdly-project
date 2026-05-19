# web/

Purpose: Monorepo folder that contains both the Next.js frontend and the backend services for the crowdfunding platform.

Suggested layout:

- `client/` — Next.js app (React + TypeScript recommended). Handles campaign browsing, pledging flows, wallet integration, and creator-facing UIs.
- `server/` — Node.js/TypeScript API server or serverless functions. Handles webhooks, fiat anchor integrations, KYC, admin tools, and background jobs.
- `package.json` (root) — optional workspace package file if using pnpm/Yarn Workspaces.

What to add here:

- For the client: scaffold `app/` or `pages/` with Wallet SDK + passkey-friendly UX, pledge UI, campaign creation UX, and dashboards.
- For the server: scaffold API endpoints for campaign metadata, notifications, webhook handlers for anchors, and admin endpoints for dispute resolution/payouts.
- Local dev scripts to run both client and server concurrently (e.g., `pnpm dev` or `npm-run-all`).

Local dev (example):

- From `web/` when scaffolded:

```bash
# install dependencies and run client + server
pnpm install
pnpm --filter client dev & pnpm --filter server dev
```

Security:

- Do not embed private keys or service account secrets in client code.
- Store API keys and anchor credentials in a secrets manager; use environment variables for local development.
- Recommended env var names (placeholders only): `SORBAN_RPC_URL`, `SORBAN_NETWORK_PASSPHRASE`, `WEB_URL`, `WEB_API_KEY`.

Notes:

- Consider using Next.js API routes for small backend needs; for heavier integrations (fiat, KYC) prefer a separate `server/` service.
- Keep environment-specific config out of source control and use CI secrets for deployments.
