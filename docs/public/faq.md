# FAQ

## What is HiveFabric?

A distributed orchestration platform for AI workloads across heterogeneous devices, with a local-first execution bias and centralized policy/scheduling.

## What is production-ready today?

Core flows are demoable and UAT-capable, but the platform is still in hardening:

- control-plane scheduling/lifecycle
- node registration/heartbeat/execution reporting
- operator UI visibility
- marketplace catalog and packaging/indexing foundation

## Why do docs emphasize both vision and current state?

Because the project is actively evolving. The docs explicitly separate:

- target direction (vision)
- implemented surfaces (current state)
- known gaps

## Is Honeycomb the control-plane backend?

No. Current control-plane backend is `hive-control-plane/service`.
`honeycomb` currently refers to runtime modes in the Dart/Flutter repository.

## Is the marketplace fully complete?

No. `apiary-market` is functional for catalog and packaging/indexing workflows, but trust/signing/policy maturity is still in progress.

## Where should contributors start?

1. Read `architecture.md` and `components/*`.
2. Use `getting-started.md` to run the stack.
3. Make changes in the repository owning that boundary.
