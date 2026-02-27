# API Reference (Public)

This page documents currently available local/dev APIs.

## Hive Control Plane (`http://localhost:8080`)

Auth headers expected by most endpoints:

- `x-api-key: <key>`
- `x-user-role: admin|user`

Core endpoints:

- `GET /healthz`
- `GET /api/nodes`
- `POST /api/nodes/register`
- `POST /api/nodes/heartbeat`
- `GET /api/tasks`
- `POST /api/tasks/create`
- `POST /api/tasks/{task_id}/events`
- `GET /api/tasks/{task_id}/stream` (websocket)
- `POST /api/workflows/submit`
- `POST /api/prompts/queen-bee`
- `POST /api/prompts/worker-bee`
- `GET /api/usage/summary`
- `GET /metrics`
- `GET /metrics/prometheus`
- `GET /api-doc/openapi.json`
- `GET /swagger-ui`

## Apiary Service (`http://localhost:8090` in Apiary stack)

Catalog endpoints:

- `GET /healthz`
- `GET /api/skills`
- `GET /api/skills/search?q=...`
- `POST /api/skills`

Role hints:

- `x-user-role: user|admin`
- `x-user-id: <uuid>`

## UI surfaces

- `hive-control-plane-ui` consumes control-plane APIs.
- Apiary UI consumes Apiary service APIs.

## Notes

- Port values vary by compose profile.
- Prefer OpenAPI (`/api-doc/openapi.json`) as the control-plane API source of truth.
- `honeycomb` is a runtime repository, not a public HTTP API surface in this docs set.
