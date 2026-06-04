# Architecture Overview

## System Flow

```text
Customer or Hive app
        |
        v
hive-tenant-gateway
        |
        v
honeycomb control plane
        |
        +--> hive-ledger
        |
        +--> comb nodes via hive-sdk / Wax native runtime
```

## Core Services

### `hive-tenant-gateway`

The public multi-tenant BYO-LLM gateway. It authenticates tenants, stores tenant LLM provider configuration, exposes MCP-equivalent tools, can run a gateway-managed orchestration loop, and forwards work to Honeycomb.

### `honeycomb`

The Rust control plane. It owns node registration, heartbeat leases, task creation, scheduling, sensitivity routing, task lifecycle, streaming, metrics, and API documentation.

### `hive-ledger`

The append-only credit ledger. It records debit, refund, credit, reserve, and release events with idempotency keys and derives balances from immutable events.

### `hive-sdk`

The shared Rust backbone. It contains protocol/domain types, IAM primitives, frontier LLM adapters, `hive-node`, the YAML catalog parser, and the `hive-bench` runner.

### `hive-app`

The user app workspace:

- `web/` is the React/Vite web app.
- `native/` is the Wax Dart/Flutter runtime and native shell.

Each surface has its own release workflow.

### `honeycomb-ui`

The operator dashboard for Honeycomb cluster visibility.

## Canonical Contracts

- Node lifecycle: register -> heartbeat lease renewals -> expiry/offline handling.
- Task lifecycle: created/queued/scheduled/running -> succeeded/failed/timed out/cancelled.
- Capability routing: model and agent capabilities are expressed as OASF-style URNs.
- Tenant boundary: tenant identity comes from gateway bearer auth and is stamped before dispatch.
- Accounting: ledger writes use idempotency keys to prevent double billing.

## Current Gaps

- Durable scheduling/state and reconciliation are still being hardened.
- Full NATS/JetStream bus migration is not complete.
- Gemini and Bedrock adapters remain future gateway/SDK work.
- Ledger reserve-before-dispatch is not fully enforced end-to-end.
- Production signing, attestation, and policy enforcement are still maturing.
