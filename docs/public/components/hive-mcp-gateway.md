# hive-mcp-gateway

`hive-mcp-gateway` exposes HiveFabric dispatch capabilities as MCP-compatible tools.

## Modes

- Library mode, consumed by `hive-tenant-gateway`.
- Stdio MCP server mode for clients that can talk directly to MCP servers.

## Tools

- `describe_cluster`
- `run_subagent`
- `estimate_cost`
