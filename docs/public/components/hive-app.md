# hive-app

`hive-app` is the HiveFabric user application workspace.

## Layout

- `web/` - React/Vite web app for chat, hive management, models, settings, and onboarding.
- `native/` - Wax native runtime and Flutter shell for desktop, mobile, and headless comb participation.

## Release model

Web and native releases are independent. Web CI/builds are scoped to `web/`; native Wax artifacts are scoped to `native/`.

## Related services

- `hive-tenant-gateway` provides tenant auth, LLM provider management, preferences, and orchestration APIs.
- `honeycomb` provides the control-plane API and comb/node state.
