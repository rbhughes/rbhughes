# Hi, I'm Bryan 👋

I'm a data engineer in Chicago. I've spent 15+ years wrangling petroleum and geoscience data — the messy, vendor-locked kind — and building the pipelines and tooling to set it free. Lately that means AI systems that answer questions from real data without making things up. My portfolio lives at **[purr.io](https://purr.io)**.

## 🛠️ Recent contract work

For the past while I built the AI side of a commercial oil & gas data platform: you ask questions in plain English, it answers from the actual well database. The work is proprietary so there's no code to show and I won't name the client, but the part worth describing is everything built around the model to keep it honest:

- The model never supplies a number from memory. Every figure comes from a query run against the database at answer time; the model's job is deciding which queries to run and writing prose around the results.
- After it writes, ordinary Python checks the draft against the query results. A number that isn't in the results gets deleted. An operator or formation the queries never returned can't be named. Each answer keeps a record of where every fact came from.
- When a query fails, the agent gets a few chances to figure out why and try another approach, then stops and says why. It doesn't flail, and it doesn't paper over the gap with a guess.
- Quality was checked by replaying a suite of real analyst conversations against the live system on every change, scored against fixed pass bars, with a running history so a slow slide in answer quality shows up as a red build instead of a hunch. One test feeds it deliberately misleading input just to prove the guardrails hold.
- Underneath, the data moved from Oracle to Parquet through a pipeline that refuses to publish a release with fewer rows than the last one. Silent data loss fails loudly.

Everything below applies the same ideas in public, with code you can read.

## 🔬 In the open at [purr.io](https://purr.io) — findings, not features

- **[walker.purr.io](https://walker.purr.io)** ([agentic_dog_walker](https://github.com/rbhughes/agentic_dog_walker)) — watch a small LLM plan dog-walking routes live: every tool call, validation bounce, and audit veto streamed as it happens. A hand-rolled agent loop with a deterministic referee and auditor, an MCP facade, and a model picker whose entries must pass an automated qualification gauntlet. Served from a retired laptop in a closet for about $1/month.
- **[spacing.purr.io](https://spacing.purr.io)** ([well-spacing-playbook](https://github.com/rbhughes/well-spacing-playbook)) — how close is too close for horizontal wells? The naive regression has the wrong sign; holding geology fixed flips it. A calibrated P10/P50/P90 interference model on public Alberta data, all 105,724 laterals mapped, and an honest account of where public data ends.
- **[methane.purr.io](https://methane.purr.io)** ([methane-outliers](https://github.com/rbhughes/methane-outliers)) — who flares and vents the most, relative to their own production? Alberta and Texas side by side on identical rolling windows, refreshed on schedule by a zero-cost pipeline (GitHub Actions + Cloudflare R2).
- **[comed.purr.io](https://comed.purr.io)** ([power_puddle](https://github.com/rbhughes/power_puddle)) — in 2025 this project called PJM's data-center load forecast a puddle of wishful thinking. Volume 2 grades that call a year later, with receipts.
- **[kingfisher.purr.io](https://kingfisher.purr.io)** ([kingfisher_wells](https://github.com/rbhughes/kingfisher_wells)) — three commercial data vendors, one Oklahoma county, and well locations that can't all be right. A medallion pipeline preserved as an interactive data-quality museum.
- **[clay-ai-hyperscale](https://github.com/rbhughes/clay-ai-hyperscale)** — a *failed* attempt to fine-tune the Clay foundation model to spot data centers from satellite imagery. The post-mortem is the point; the [hand-labeled dataset](https://huggingface.co/datasets/rbhughes/hyperscale-datacenter-segmentation-naip) is published for anyone who wants to beat the baseline.

## 🛢️ Earlier: energy data tooling

[pg_ppdm](https://github.com/rbhughes/pg_ppdm) (the PPDM 3.9 well-data model, Oracle → PostgreSQL) · [purr_petra_cli](https://github.com/rbhughes/purr_petra_cli) · [purr_geographix](https://github.com/rbhughes/purr_geographix) / [purr_petra](https://github.com/rbhughes/purr_petra) — extraction tooling for vendor-locked geoscience project databases.

## 📫 Reach me

- Email: [bryan@purr.io](mailto:bryan@purr.io)
- Web: [purr.io](https://purr.io) — home base
- The cat distribution system also assigned me [thequirkykitty.com](https://thequirkykitty.com)
