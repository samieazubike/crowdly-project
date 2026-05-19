# contracts/

Purpose: Soroban smart contracts (Rust) for the crowdfunding platform.

What to add here:

- Rust workspace with contract crates (e.g., `campaign`, `escrow`, `registry`).
- Build instructions using `cargo` and `soroban` toolchain.
- Tests: unit and integration tests that run on local soroban testnet or mock harness.
- CI steps to compile to WASM and run basic contract tests.

Notes:

- Keep private keys out of the repo. Use ephemeral test accounts for CI and populate secrets via the CI provider.
- Consider depending on Trustless Work primitives for milestones/escrow logic instead of re-implementing.
