# hive-models

`hive-models` is the canonical YAML catalog for supported models, agents, and benchmark suites.

## Responsibilities

- Bind model ids to OASF-style capability URNs.
- Track runtime pull tags, hardware floors, tool-calling support, license, and tier.
- Define reusable agent prompt templates and benchmark suites.
- Provide a language-agnostic source of truth consumed by Honeycomb, comb runtimes, and `hive-bench`.
