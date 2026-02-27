# Getting Started

This quickstart reflects the current stack and repository boundaries.

## Prerequisites

- Docker + Docker Compose
- Rust toolchain
- Node.js 20+
- Dart SDK (optional, for Honeycomb runtime)

## 1. Start control-plane + UI + multi-node

```bash
cd hive-control-plane
docker compose \
  -f docker/docker-compose.with-ui-multi-node.yml \
  -f docker/docker-compose.with-ui-multi-node.local.yml \
  up -d
```

Verify:

```bash
curl -fsS http://localhost:8080/healthz
curl -fsS -H 'x-api-key: dev-hive-key' -H 'x-user-role: admin' http://localhost:8080/api/nodes
```

## 2. Start Apiary service + UI

```bash
cd apiary-market
docker compose -f docker/docker-compose.yml up -d apiary-service apiary-ui
curl -fsS http://localhost:8090/healthz
```

## 3. Open UIs

- Control-plane UI: `http://localhost:5175`
- Apiary UI: `http://localhost:5176`

## 4. Submit a task

```bash
curl -X POST http://localhost:8080/api/tasks/create \
  -H 'content-type: application/json' \
  -H 'x-api-key: dev-hive-key' \
  -H 'x-user-role: admin' \
  -d '{"task_id":"00000000-0000-0000-0000-000000000123","agent":"queen-bee-advanced","description":"Plan distributed execution for a hello-world task"}'
```

Then list tasks:

```bash
curl -H 'x-api-key: dev-hive-key' -H 'x-user-role: admin' http://localhost:8080/api/tasks
```

## 5. Optional: run Honeycomb runtime

```bash
cd honeycomb
dart pub get
dart run headless_main.dart config/honeycomb.example.json
```

This runtime is not part of the control-plane compose stack by default.
