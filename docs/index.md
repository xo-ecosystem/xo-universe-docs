# XO Universe

Welcome to the public documentation surface for **XO**, a modular trust continuum designed to connect digital artifacts, stories, identity, and real-world verification.

This documentation explains how the XO ecosystem works, what already exists today, and how the different modules connect into a larger system.

XO is not a single application. It is a **continuum of interoperable modules** that together enable verifiable trust across digital and physical environments.

!!! tip
    If you prefer a **visual introduction**, start with:

    - [XO Universe Map](xo-universe-map.md)
    - [Domain Constellation](domain-constellation.md)

    These pages explain the structure of the XO ecosystem in diagrams before diving into the detailed documentation.

---

# Core Idea

**XO = Artifact + Story + Community + Ledger**

Each part reinforces the others:

- **Artifacts** — drops, collectibles, sealed files, and physical objects with digital twins
- **Stories** — pulses, narratives, updates, and public signals
- **Community** — participation, interaction, and collective verification
- **Ledger** — the permanent memory preserving provenance and continuity

---

# The Trust Continuum

XO organizes its system into interconnected layers rather than isolated apps.

```mermaid
%% XO docs landing overview
flowchart TD

subgraph Core[Core Trust Layer]
    Vault[Vault\nStorage + Signatures]
    Pulse[Pulse\nStory Publishing]
    Agent[Agent\nAutomation]
end

subgraph Activation[Activation Layer]
    Drops[Drops\nArtifacts]
    Traits[Traits\nEvolution]
    Bridge[Bridge\nDigital-Physical Link]
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
Bridge --> Ledger