# Public Release Notes

## 2026-06-06 - Honeycomb single-backend merge

- Embedded the tenant gateway and ledger into `honeycomb`, so the default local backend is now one process instead of three.
- Moved the shared MCP gateway code into the `hive-sdk` root package so Honeycomb can serve the tool surface directly.
- Updated the operator UI service-status view and local docs to describe the merged backend and embedded health paths.
- Prepared the retired `hive-tenant-gateway`, `hive-ledger`, and `hive-mcp-gateway` repositories for removal after the cleanup push.

## 2026-06-03 - Repository consolidation and documentation reset

- Removed obsolete remote repositories: `hive-demos` and `hive-gateway-tests`.
- Merged the standalone Wax runtime into `hive-app/native` and removed the standalone `wax` repository after the migration landed.
- Split `hive-app` into independently releasable `web/` and `native/` folders.
- Documented the current active repository map and removed stale `apiary-market` / `hive-control-plane` workspace references from public current-state docs.
- Established this public release-notes page as the human-readable change log for public documentation state.

## 2026-05-30 - Gateway and app maturity pass

- `hive-tenant-gateway` gained self-service signup, tenant LLM provider management, routing preferences, and ledger debit/refund integration.
- `hive-app` became the user-facing app surface for chat, hive management, and settings.
- `honeycomb` continued as the control-plane repository while the Rust package name still carries the historical `hive-control-plane` name.
