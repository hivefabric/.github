# hive-tenant-gateway

`hive-tenant-gateway` is the public multi-tenant BYO-LLM gateway.

## Responsibilities

- Tenant signup and bearer-token authentication.
- Tenant LLM provider registry and encrypted key vault.
- MCP-equivalent tools: `describe_cluster`, `run_subagent`, and `estimate_cost`.
- Gateway-managed orchestration through `/v1/orchestrate`.
- Tenant routing preferences and per-tenant rate limiting.
- Ledger debit/refund integration for dispatched work.

## Default port

`8090`
