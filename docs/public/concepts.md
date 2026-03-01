# Core Concepts

## Fabric

A distributed system of control and execution surfaces coordinating agent workloads across many devices.

## Control Plane

The authoritative scheduler/state owner implemented in `hive-control-plane/service`.

## Control Plane UI

The operator-facing observability surface in `hive-control-plane-ui`.

## Node Runtime

A node runtime (`hive-sdk/packages/hive-node` embedded in Honeycomb modes) that advertises capabilities, receives assignments, and returns execution events.

## Contracts Layer

`hive-sdk` defines shared contracts and identity boundaries used by control-plane/runtime modules.

## Marketplace Layer

`apiary-market` provides catalog and packaging/indexing capabilities for reusable agent artifacts.

## Current Principle

System boundaries are explicit:

- control plane owns scheduling and lifecycle state
- nodes execute workloads and report events
- shared contracts prevent DTO drift across repositories
