# hive-ledger

`hive-ledger` is the event-sourced credit accounting service.

## Responsibilities

- Append-only credit/debit/refund/reserve/release events.
- Idempotency-key protection for retries.
- Balance derivation from immutable event history.
- Internal HTTP API for gateway and operational tooling.

## Default port

`8100`
