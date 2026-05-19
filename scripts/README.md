# scripts/

Purpose: Utility scripts used during development and deployment.

Examples:

- `build-contracts.sh` — compile Rust contracts to WASM and copy artifacts.
- `deploy-contract.sh` — helper to deploy to soroban testnet/mainnet using CI-provided credentials.
- `sync-abi.sh` — sync contract ABIs to frontend/backend configs.

Keep scripts minimal and secure. Avoid embedding secrets in scripts.
