# Comb Node Runtime (`comb-node`)

## Role

Worker runtime daemon that executes scheduled workloads.

## Responsibilities

- register and heartbeat with control-plane
- advertise capabilities and telemetry
- execute supported runtime paths (LLM/WASM/Docker)
- post task events/results

## Local run

```bash
cd comb-node
cargo check
cargo test
```

Docker stacks are available under `comb-node/docker`.
