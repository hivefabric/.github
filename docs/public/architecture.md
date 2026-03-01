# Architecture Overview

## Vision Architecture

Target architecture is a distributed fabric with:

- a control plane for policy, scheduling, state, and observability
- runtime nodes on heterogeneous devices
- shared contracts and identity boundaries
- marketplace packaging/distribution for reusable agent capabilities

## Current Architecture (2026-03-01)

### Control and orchestration

- `hive-control-plane/service`
  - node registry
  - lease-based heartbeat model
  - task lifecycle/state transitions
  - scheduler and dispatch
  - metrics and websocket task streams

- `hive-control-plane-ui`
  - node and task operational visibility
  - telemetry and runtime capability display

### Runtime and execution

- `hive-sdk/packages/hive-node`
  - canonical node registration/heartbeat SDK
  - capability and telemetry reporting
  - LLM/WASM/Docker execution paths
  - event/log/result reporting primitives used by clients

- `honeycomb`
  - runtime client modes (desktop/mobile/headless)
  - consumes `hive-node` from `hive-sdk`
  - adds cross-platform operational UX (splash connection gate, retry, LAN host override/discovery)

### Shared contracts and platform modules

- `hive-sdk`
  - protocol DTOs and domain contracts
  - IAM primitives (`hive-iam`)
  - reusable node SDK (`hive-node`)

- `apiary-market`
  - catalog service/UI
  - OCI-oriented packaging/indexing foundation

## Canonical Contracts

- Node lifecycle: register -> heartbeat lease renewals -> expiry/offline handling.
- Task lifecycle: `Created -> Queued -> Scheduled -> Running -> Succeeded|Failed|TimedOut -> Retried|Cancelled`.
- Auth boundary: API-key and role-scoped access through IAM-aligned primitives.

## Gap to Vision

The architecture direction is aligned, but current implementation still needs:

- durable persistence and retention for state
- stronger scheduler hardening under churn/failure
- mature trust and signature enforcement for packaged artifacts
