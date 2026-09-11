# Hi, I'm Bryan 👋

I'm a data engineer in Chicago. I've spent 15+ years wrangling petroleum and geoscience data — the messy, vendor-locked kind — and building the pipelines and tooling to set it free. These days that thread runs into **grounded-LLM systems**: agents you can trust with real data, and the deterministic machinery that keeps them honest. My portfolio lives at **[purr.io](https://purr.io)**.

## 🛠️ Production grounded-LLM systems

Most recently I built and evaluated a production grounded-LLM system — a conversational analytics engine over oil & gas well data (DuckDB over Parquet, multi-provider LLM back end) for a commercial well-data platform. That work is proprietary, so no code or names here — but the parts I care most about are the ones that exist because the model can't be trusted:

- **Grounding as code, not prompts** — the model writes prose with fact references, never raw numbers; deterministic gates resolve citations, strip anything ungrounded (numbers, entities, fabrication phrases), and emit a provenance audit with a zero-leak invariant. Table-driven unit tests pin every gate behavior, in CI on every push.
- **A bounded agent loop with failure-driven re-planning** — hard step caps with failure headroom, so a failed SQL hop is diagnosed and re-planned instead of aborting; typed stop reasons on every exit; deterministic "belt tools" for recurring analytics so the planner calls code, not vibes.
- **Evaluation that survives stochasticity** — an LLM-as-judge harness with rubric dispatch (factual turns graded on correctness, analysis turns on insight — never the reverse), median-of-N grading gated on the typical roll, per-fixture grade history with drift detection, and a fixture that uploads a hostile persona and asserts the grounding gates hold.
- **Data releases that can't silently degrade** — ETL from Oracle/PPDM to Parquet with atomic writes, bounded memory, and a provenance manifest carrying per-file row counts: a release that unexpectedly shrinks fails loudly instead of shipping.

The same design DNA runs through everything below — in the open, with receipts.

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
