# Hi, I'm Bryan 👋

I'm a **Senior AI Engineer** in Chicago. I've spent 20+ years wrangling petroleum and geoscience data — the messy, vendor-locked kind — and I now build AI systems on top of it that answer questions from real data without making things up. My portfolio lives at **[purr.io](https://purr.io)**.

## 🛠️ Recent contract work

I built the data pipeline, AI backend and CLI test framework for a commercial oil & gas analytics product: a *fact-gating* harness turns English queries or spatial AOIs into insight that carries only the numbers the deterministic stats support. Dataset-centric agents run ad-hoc SQL, generate and edit charts, and monitor their own quality. The harness detects any ephemeral drops in LLM quality and retries. The full Oracle-to-Parquet pipeline opens well, production, spatial, legal, financial and forecasting data to AI-assisted investigation.

*Proprietary work — the client is unnamed and there is no code to show. The same ideas, in public and with code you can read, are below.*

## 🔬 In the open at [purr.io](https://purr.io) — findings, not features

- **[walker.purr.io](https://walker.purr.io)** ([agentic_dog_walker](https://github.com/rbhughes/agentic_dog_walker)) — watch a small LLM plan dog-walking routes live: every tool call, validation bounce, and audit veto streamed as it happens. A hand-rolled agent loop with a deterministic referee and auditor, an MCP facade, and a model picker whose entries must pass an automated qualification gauntlet. Served from a retired laptop in a closet for about $1/month.
- **[spacing.purr.io](https://spacing.purr.io)** ([well-spacing-playbook](https://github.com/rbhughes/well-spacing-playbook)) — how close is too close for horizontal wells? The naive regression has the wrong sign; holding geology fixed flips it. A calibrated P10/P50/P90 interference model on public Alberta data, all 105,724 laterals mapped, and an honest account of where public data ends.
- **[methane.purr.io](https://methane.purr.io)** ([methane-outliers](https://github.com/rbhughes/methane-outliers)) — who flares and vents the most, relative to their own production? Alberta and Texas side by side on identical rolling windows, refreshed on schedule by a zero-cost pipeline (GitHub Actions + Cloudflare R2).
- **[comed.purr.io](https://comed.purr.io)** ([power_puddle](https://github.com/rbhughes/power_puddle)) — in 2025 this project called PJM's data-center load forecast a puddle of wishful thinking. Volume 2 grades that call a year later, with receipts.
- **[kingfisher.purr.io](https://kingfisher.purr.io)** ([kingfisher_wells](https://github.com/rbhughes/kingfisher_wells)) — three commercial data vendors, one Oklahoma county, and well locations that can't all be right. A medallion pipeline preserved as an interactive data-quality museum.
- **[clay-ai-hyperscale](https://github.com/rbhughes/clay-ai-hyperscale)** — a *failed* attempt to fine-tune the Clay foundation model to spot data centers from satellite imagery. The post-mortem is the point; the [hand-labeled dataset](https://huggingface.co/datasets/rbhughes/hyperscale-datacenter-segmentation-naip) is published for anyone who wants to beat the baseline.

## 🤖 How I work with AI

Every commit here is co-authored with Claude. I'd rather tell you how than let you guess.

The same rule governs the code and the process: **language at the boundaries, deterministic code in the middle.** Anything with an exact answer — route order, safety thresholds, schema validation, which well an identifier refers to — is plain code with tests; the model translates intent and narrates results. That's the stated architecture of [agentic_dog_walker](https://github.com/rbhughes/agentic_dog_walker/blob/main/CLAUDE.md), it's why [geo-mini-rag](https://rag.purr.io) replaced embedding search with exact lookup once I measured that embeddings cannot resolve identifiers, and on contract work it is a grounding layer that checks every generated number against the rows behind it before anyone sees it.

How I direct the work is written down per project, in the `CLAUDE.md` files committed next to the code — including [one](https://github.com/rbhughes/well-spacing-playbook/blob/main/CLAUDE.md) that overrides autonomous mode outright: explain before writing, one step at a time, and leave the parts that carry the learning for me to type.

None of it ships on vibes. The fact-gated harness described above is one example; agentic_dog_walker does the same to models, where none reaches the picker until it clears an automated qualification gauntlet.

AI makes me faster. The harness is what makes me willing to ship.

## 🛢️ Earlier: energy data tooling

[pg_ppdm](https://github.com/rbhughes/pg_ppdm) (the PPDM 3.9 well-data model, Oracle → PostgreSQL) · [purr_petra_cli](https://github.com/rbhughes/purr_petra_cli) · [purr_geographix](https://github.com/rbhughes/purr_geographix) / [purr_petra](https://github.com/rbhughes/purr_petra) — extraction tooling for vendor-locked geoscience project databases.

## 📫 Reach me

- Email: [bryan@purr.io](mailto:bryan@purr.io)
- Web: [purr.io](https://purr.io) — home base
- The cat distribution system also assigned me [thequirkykitty.com](https://thequirkykitty.com)
