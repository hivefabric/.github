# Executors and Nodes

A node executor is any runtime instance that can accept assignments from control-plane scheduling and return execution events.

## Current executor surfaces

- `comb-node` (primary Rust runtime daemon)
- `honeycomb` runtime modes (cross-platform runtime client surface)

## Node capability model

Current scheduling signals include:

- runtime capabilities (`wasm`, `docker`, LLM profile hints)
- CPU/memory and telemetry snapshot data
- lease freshness and registration state

## Heartbeat and lease behavior

- node registers
- control-plane issues lease window
- node sends heartbeat renewals
- control-plane marks stale nodes offline/expired for placement safety

## Security boundary (current)

- role and API-key checks enforced at control-plane routes
- user-scoped vs platform-scoped route separation
- runtime-side capability gating before execution

## Current constraints

- policy and trust hardening are still in progress
- persistence/reconciliation behavior is not fully production-hardened yet
