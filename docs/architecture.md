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
# Architecture

This page explains the XO architecture at a high level.

XO is built as a modular trust continuum rather than a single monolithic application. The system is designed so that different layers can evolve independently while still reinforcing one another.

!!! tip
    If you want a more narrative system view, also see [XO Universe Map](xo-universe-map.md). If you want the domain-facing version, see [XO Domain Constellation](domain-constellation.md).

## High-level Flow

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
```

This architecture groups XO into readable zones so the trust core, activation mechanisms, and public record layer can be understood at a glance.

## Core Modules

### Vault

Vault is the security and signing layer. It is responsible for storage, sealing, signatures, and trust anchors.

### Pulse

Pulse is the publishing and narrative layer. It turns activity into visible updates, stories, and public continuity.

### Drops

Drops are the activation layer. They package artifacts, experiences, and releases into forms people can actually receive, mint, or interact with.

### Traits

Traits are the evolution layer. They allow identities, collectibles, and artifacts to gain additional meaning or state over time.

### Ledger

Ledger is the public record layer. It preserves provenance, history, and verifiable continuity.

### Agent

Agent is the orchestration layer. It helps automate flows, route events, and coordinate the different parts of the system.

### Bridge

Bridge is the digital-physical layer. It connects objects, seals, QR or NFC references, and real-world verification back into the trust continuum.

## Design Principle

Each XO module should be understandable on its own, but more powerful when linked to the others.