# Crowdly — Stellar Reward-Based Crowdfunding (Scaffold)

This repository is a scaffold for a reward-based crowdfunding/pre-order platform built on Stellar (Soroban). It contains folders for smart contracts, a Next.js frontend, and a Node-based backend plus infra and docs. No implementation code is included — this is a project skeleton.

Security note: This README intentionally avoids exposing any secrets, private keys, or credentials. Use environment variables and a secure secrets manager for sensitive values.

## Repo structure

- contracts/ — Soroban smart contract Rust workspace (WASM). Place contract source, tests, and build artifacts here.
- web/ — Monorepo folder containing both the Next.js frontend and backend services (client/ and server/).
- infra/ — Infrastructure-as-code (Terraform, CloudFormation) and deployment manifests.
- scripts/ — Helpful scripts (deploy, build helpers, CI helpers).
- docs/ — Design docs, smart-contract spec, audit checklist.
- tests/ — End-to-end and integration test harnesses.

## Quickstart (scaffold)

1. Install required tools locally (examples):
    - Rust + cargo
    - Soroban CLI (https://soroban.stellar.org)
    - Node.js 18+
    - pnpm or npm

2. Follow per-folder READMEs to initialize each workspace when ready.

## Secrets & keys

- Never commit private keys, mnemonic phrases, or API secrets.
- Use `.env` files excluded by `.gitignore` for local development and a secret manager (e.g., Vault, GitHub Secrets) for CI.
- Recommended env var names (placeholders only):
    - `SORBAN_RPC_URL`
    - `SORBAN_NETWORK_PASSPHRASE`
    - `FRONTEND_URL`
    - `BACKEND_API_KEY`

## Next steps

- Implement Soroban escrow contract(s) under `contracts/` using Trustless Work primitives or custom logic.
- Scaffold Next.js app under `frontend/` with Wallet SDK and passkey support.
- Implement backend integration patterns for fiat on/off-ramps and KYC in `backend/`.

## Contributing

Open issues for feature requests, and follow the coding guidelines in `docs/`.

---

This file is a scaffold only. Remove this notice when adding real implementation code.
