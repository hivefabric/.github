# Honeycomb Runtime (`honeycomb`)

## Role

Cross-platform runtime client repository.

## Modes

- desktop
- mobile
- headless

## Current boundary

`honeycomb` is not the control-plane backend. It provides runtime/client capabilities and deployment surfaces for node operation.

## Current technical highlights

- Embeds `hive-sdk/packages/hive-node` as the runtime engine.
- Connection-gated startup UX (splash) with explicit retry/reconnect.
- HTTP fallback for node register/heartbeat when control-plane websocket command channel is unavailable.
- Mobile LAN host override and dev auto-discovery when config points to `localhost`.
