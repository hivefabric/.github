# Public Release Notes

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
