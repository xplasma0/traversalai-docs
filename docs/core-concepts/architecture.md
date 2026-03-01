# Architecture

TraversalAI is composed of:

- Control gateway (core runtime)
- UI dashboard (operations interface)
- CLI (automation interface)
- Channel adapters (message ingress/egress)
- Session and state subsystem

## Design Goals

- Clear trust boundaries
- Reliable long-running control plane
- Extensible integration points
