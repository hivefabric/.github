# HiveFabric Public Documentation

This documentation reflects two realities at the same time:

- the long-term vision of HiveFabric as a distributed autonomous agent fabric
- the current implementation state across active repositories

## Vision (North Star)

HiveFabric aims to be a local-first distributed platform where autonomous workloads run across heterogeneous user-owned devices, coordinated by a control plane with policy, scheduling, and observability.

## Current State (2026-03-01)

The current platform is functional but still in a hardening phase:

- `hive-control-plane/service` handles node registration, heartbeat, task lifecycle, scheduling, metrics, and streams.
- `hive-control-plane-ui` exposes operational visibility for nodes and tasks.
- `hive-sdk` is the contract backbone (`hive-sdk`, `hive-iam`, `hive-node`).
- `honeycomb` consumes `hive-node` to execute task workloads through supported runtime paths (LLM/WASM/Docker) on desktop/mobile/headless.
- `apiary-market` provides a catalog and OCI-oriented packaging/indexing foundation.
- `honeycomb` provides cross-platform runtime modes (desktop/mobile/headless).

## What Is Not Finished Yet

- durable persistence for core control-plane state
- production-grade scheduler resilience and reconciliation
- complete trust/signing policy for marketplace packaging
- full operational automation for all cross-repo runbooks

## Start Here

- Getting started: `public/getting-started.md`
- Architecture: `public/architecture.md`
- Components by repository: `public/components/*`
- API reference: `public/apis.md`
- Roadmap: `public/roadmap.md`

## Scope

Public docs describe implemented contracts and explicit in-progress work.
Private planning, investor runbooks, and internal execution notes are in `.github-private`.
