`docs/xo-universe-map.md`
```md
# XO Universe Map

This page provides a **visual overview of the XO ecosystem** and how its modules connect into a single trust continuum.

XO is not designed as a monolithic platform. Instead it is a **network of cooperating layers** where each component performs a clear role.

!!! tip
    For a **domain-level view** of how the ecosystem is exposed publicly, also see:

    - [XO Domain Constellation](domain-constellation.md)

    That page shows how the XO modules map onto the domain architecture of the ecosystem.

---

# The XO Trust Continuum

```mermaid
%% XO Trust Continuum lifecycle diagram
flowchart LR

subgraph Core[Core Trust Layer]
    Vault[Vault\nSeal + Store]
    Pulse[Pulse\nPublish]
    Agent[Agent\nAutomation]
end

subgraph Activation[Activation Layer]
    Drops[Drops\nArtifacts]
    Traits[Traits\nEvolution]
    Bridge[Bridge\nPhysical Link]
end

subgraph Public[Public Memory Layer]
    Ledger[Ledger\nPublic Record]
    Digest[Digest\nDaily Memory]
end

Vault --> Pulse
Pulse --> Drops
Drops --> Traits
Traits --> Ledger
Pulse --> Digest
Agent --> Vault
Agent --> Pulse
Agent --> Drops
Bridge --> Ledger