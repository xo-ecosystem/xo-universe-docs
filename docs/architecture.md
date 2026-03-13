# Architecture

This page explains the XO architecture at a high level.

XO is built as a modular trust continuum rather than a single monolithic application. The system is designed so that different layers can evolve independently while still reinforcing one another.

!!! tip
    If you want a more narrative system view, also see [XO Universe Map](xo-universe-map.md). If you want the domain-facing version, see [XO Domain Constellation](domain-constellation.md).

## High-level flow

```mermaid
%% XO architecture overview
flowchart TD

subgraph Core[Core Trust Layer]
    Vault[Vault\nStorage + Signatures]
    Pulse[Pulse\nStory Publishing]
    Agent[Agent\nAutomation + Routing]
end

subgraph Activation[Activation Layer]
    Drops[Drops\nArtifacts + Activation]
    Traits[Traits\nEvolution + Identity]
    Bridge[Bridge\nDigital-Physical Verification]
end

subgraph Public[Public Record Layer]
    Ledger[Ledger\nPublic Record]
end

Vault --> Pulse
Pulse --> Drops
Drops --> Traits
Traits --> Ledger
Agent --> Vault
Agent --> Pulse
Agent --> Ledger
Bridge --> Ledger
Bridge --> Drops