# XO Universe Docs

This repository contains the **public documentation for the XO ecosystem**.

It explains the architecture, pillars, and activation strategy behind the XO Trust Continuum.

The documentation is designed to be readable both **directly on GitHub** and as a **rendered documentation website using MkDocs**.

XO is a modular trust continuum for verifiable digital and physical artifacts, identity, and public memory.

This repository is the public reading surface for the XO universe. It explains what XO is, what already exists, how its modules fit together, and what is being activated next.

## Start here

- [What is XO?](docs/what-is-xo.md)
- [System State](docs/system-state.md)
- [Architecture](docs/architecture.md)
- [Seven Pillars](docs/seven-pillars.md)
- [Activation Plan](docs/activation-plan.md)

## Visual Overview

If you prefer a visual introduction to the system, start with these pages:

- [XO Universe Map](docs/xo-universe-map.md)
- [Domain Constellation](docs/domain-constellation.md)

These diagrams show how the main XO modules connect and how the domain constellation exposes different parts of the ecosystem.

They provide the fastest way to understand the overall structure of the XO Trust Continuum.

## Core idea

**XO = Artifact + Story + Community + Ledger**

XO combines:

- digital artifacts and drops
- narrative publishing and public memory
- cryptographic storage and signing
- evolving traits and identity
- community participation and real-world verification

## Current direction

XO is being activated in stages:

1. establish a clear public documentation layer
2. show the current system state honestly
3. activate working artifact flows
4. expand community interaction and public trust loops

This repo is intentionally focused on clarity. It is the public-facing documentation layer for XO, while deeper experimental and development repositories remain private until they are ready.


---

# Local Development

The docs can be previewed locally using **MkDocs Material**, which renders the markdown files into a clean documentation site.

## 1. Install dependencies

```bash
pip install mkdocs mkdocs-material
```

Optional (recommended plugins):

```bash
pip install mkdocs-mermaid2-plugin mkdocs-glightbox
```

These enable:

- Mermaid diagrams (for architecture graphs)
- Clickable image viewer / zoom

## MkDocs Tip (recommended)

To make the documentation look like a **full product documentation site**, create a small MkDocs configuration file in the repository root:

```yaml
site_name: XO Universe
site_description: XO Trust Continuum Documentation

theme:
  name: material
  features:
    - navigation.instant
    - navigation.tabs
    - navigation.sections
    - content.code.copy

plugins:
  - search
  - mermaid2
  - glightbox
```

These options enable:

- a professional navigation sidebar
- tabbed top navigation
- fast page transitions
- copy‑to‑clipboard code blocks
- interactive diagrams and images

With this configuration the docs will render much closer to a **production documentation portal** rather than a simple markdown repository.

---

# 2. Run the docs locally

From the repository root:

```bash
mkdocs serve
```

Then open:

```
http://127.0.0.1:8000
```

The site will automatically reload when files change.

---

# Repository Structure

```
docs/
  index.md
  xo-universe-map.md
  domain-constellation.md
  architecture.md
  seven-pillars.md
  system-state.md
  activation-plan.md
```

Each document describes a part of the XO ecosystem.

---

# Main Concepts

XO is built around a modular trust architecture:

Vault → Pulse → Drops → Traits → Ledger

Supporting layers:

- Digest (human-readable summaries)
- Bridge (digital ↔ physical link)
- Agent (automation)

This structure forms what XO calls the **Trust Continuum**.

---

# Publishing

The docs can be deployed easily using:

- **GitHub Pages**
- **Cloudflare Pages**
- **IPFS / Arweave mirrors**

MkDocs produces a static site which works well with all of these platforms.

---

# Status

This documentation is part of the current **XO activation phase**, turning internal architecture into a publicly understandable ecosystem.

More modules and diagrams will be added as the system continues to stabilize.