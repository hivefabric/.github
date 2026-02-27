# Control Plane Service (`hive-control-plane/service`)

## Role

Authoritative scheduling and lifecycle service for nodes and tasks.

## Responsibilities

- node registration and heartbeat lease handling
- task lifecycle state transitions
- scheduling and dispatch
- event ingestion and websocket stream fanout
- metrics and usage surfaces

## Public endpoints

See `../apis.md` for complete endpoint list.

## Current maturity

Functional for demo/UAT workflows; persistence and deeper reconciliation remain in progress.
