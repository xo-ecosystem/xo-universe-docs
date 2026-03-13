`docs/domain-constellation.md`
```md
# XO Domain Constellation

The XO ecosystem is supported by a large constellation of domains. Each domain acts like a **planet or gateway** that exposes a specific part of the XO trust continuum.

Rather than one central platform, XO is intentionally distributed across multiple domains. This keeps the system modular, resilient, and easier to evolve over time.

!!! tip
    If you want to understand the **functional architecture behind these domains**, start with:

    - [XO Universe Map](xo-universe-map.md)

    That page explains how Vault, Pulse, Drops, Traits, and Ledger interact inside the trust continuum.

---

# Constellation Overview

```mermaid
%% XO domain constellation overview
flowchart TD

subgraph Core[Core Infrastructure]
    Vault[xo-vault.com]
    Pulse[xopulse.com]
    Ledger[xoledger.com]
    Center[xo.center]
end

subgraph Identity[Identity + Evolution]
    Traits[xotraits.com]
    Seals[xoseals.com]
    Community[xo.community]
end

subgraph Activation[Activation + Exchange]
    Exchange[21xo.exchange]
    Digest[xo-digest.com]
end

Center --> Vault
Center --> Community
Vault --> Pulse
Pulse --> Digest
Pulse --> Seals
Seals --> Traits
Traits --> Ledger
Ledger --> Exchange
Community --> Pulse