# HiveFabric Public Documentation

This documentation tracks the public architecture and current implementation state of HiveFabric.

## Current State

As of 2026-06-03, the active public organization repositories are:

- `honeycomb` - Rust control plane for node registration, scheduling, task lifecycle, streaming, metrics, and API docs.
- `hive-tenant-gateway` - multi-tenant BYO-LLM gateway and customer-facing orchestration/API surface.
- `hive-mcp-gateway` - MCP tool interface library and stdio server.
- `hive-ledger` - event-sourced credit accounting service.
- `hive-sdk` - shared Rust contracts, IAM, frontier adapters, comb runtime SDK, model catalog parser, and benchmark runner.
- `hive-models` - YAML model, agent, and benchmark catalog.
- `hive-app` - user application workspace split into `web/` and `native/`.
- `honeycomb-ui` - operator dashboard for the Honeycomb control plane.
- `hivefabric.github.io` - public website.
- `.github` - public organization profile and documentation.

The former `hive-demos` and `hive-gateway-tests` repositories were removed on 2026-06-03. Demo and integration-test work should now live in the owning service/app repositories or the SDK benchmark runner.

## Vision

HiveFabric is a local-first distributed AI fabric where autonomous workloads run across heterogeneous user-owned devices, coordinated by a control plane with policy, scheduling, observability, and transparent accounting.

## Start Here

- Getting started: `public/getting-started.md`
- Architecture: `public/architecture.md`
- Release notes: `public/release-notes.md`
- Components by repository: `public/components/*`
- API reference: `public/apis.md`
- Roadmap: `public/roadmap.md`

## Scope

Public docs describe implemented contracts and explicit in-progress work. Private planning, investor runbooks, and internal execution notes live in `.github-private`.
