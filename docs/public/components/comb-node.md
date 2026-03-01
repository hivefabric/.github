# Node Runtime SDK (`hive-sdk/packages/hive-node`)

## Role

Worker runtime implementation used by clients (primarily Honeycomb) to execute scheduled workloads.

## Responsibilities

- register and heartbeat with control-plane
- advertise capabilities and telemetry
- execute supported runtime paths (LLM/WASM/Docker)
- post task events/results

## Local run

```bash
cd hive-sdk
cargo check -p hive-node
cargo test -p hive-node
```

For runnable node instances, use `honeycomb` (desktop/mobile/headless or Docker).
