# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

Awesome-FAS is a curated "awesome list" of Face Authentication Security resources — face anti-spoofing / presentation-attack detection / liveness detection papers, datasets, and benchmarks. It contains **only Markdown** (no source code, build, lint, or test tooling). All work is editing Markdown tables and links. The list is maintained by adding entries via pull requests/issues.

## Structure

The list is split by **attack type** (see `README.md`'s taxonomy table):

- `README.md` — overview/index. Holds the Type 1 vs Type 2 taxonomy, links to the two collection files, the **Unified (Type 1 + Type 2) Attack Detection** bridge table, the shared `# Notes` venue glossary, and the maintainers' BibTeX citations. The venue glossary lives here and is referenced by the other files — add new abbreviations here.
- `Face-Anti-Spoofing.md` — **Type 1** (presentation attacks, ISO/IEC 30107): Databases, Learning-based methods (subsectioned by year, Before 2018 → 2026), System / Mobile Applications, Attack.
- `Deepfake-Detection.md` — **Type 2** (digital/injection deepfakes): Datasets, Surveys, Detection Methods (by year 2022 → 2026). CCF-A curated, not exhaustive.
- `index.html` — the GitHub Pages project page: a self-contained insights dashboard (Chart.js via CDN) showing research momentum, venue distribution, and theme frequency. **Its hardcoded numbers are derived from the Markdown lists** — when adding many papers, re-aggregate (e.g. `awk -F'|' '/^\|\[/{print $3}'`) and update the `t1`, `t2`, `venV`, `thV` arrays and the stat cards. Served at https://rizhaocai.github.io/Awesome-FAS/ (enable Pages → branch `master`, root).
- `Benchmarks/README.md` — links to external spreadsheets for intra-dataset and cross-dataset results.
- `Benchmarks/CASIA+REPLAY-ATTACK.md` — a benchmark table (methods sorted by HTER on the CASIA↔REPLAY-ATTACK cross-dataset protocol), with a legend mapping each method abbreviation to its paper.

## Conventions when adding entries

- Decide Type 1 vs Type 2 first: presentation/physical → `Face-Anti-Spoofing.md`; deepfake/digital → `Deepfake-Detection.md`; detects both → the Unified table in `README.md`.
- **Databases** rows use columns: `Name | Release year | Attacks | Modalities | #subjects | #videos`. Name links to the dataset page; add a separate `[paper]` link when the dataset page differs from the paper.
- **Paper rows** (Learning-based / Detection / System / Attack) use columns: `Title | Venue | Note`. Title links to the paper PDF/page. Venue is an abbreviation + year (e.g. `T-IFS 2024`, `CVPR 2025`). The Note column carries tags like the method name/abbreviation, attack type, modality (RGB/IR/Depth/multi-modal), keywords (domain generalization, CLIP/vision-language, diffusion, frequency, audio-visual), and a `[Code](url)` link when available.
- Place a new paper under the **year subsection matching its venue year**. Add ArXiv-only papers too, but per the Notes section they are "regarded not published" — collected for reference only.
- Venue abbreviations must be defined in the `# Notes` section of `README.md`. If you introduce a new abbreviation, add it there.
- Every paper must be grounded in a real, verifiable source (openaccess.thecvf.com / ecva.net / IEEE-DOI / ojs.aaai.org / ijcai.org / openreview.net / dl.acm.org / arXiv) — never invent titles, venues, or links.
- In `Benchmarks/CASIA+REPLAY-ATTACK.md`, keep the table sorted by the HTER (CASIA→REPLAY-ATTACK) column and add the method's expansion to the legend below the table.
- Strikethrough (`~~Name~~`) marks datasets/resources that are no longer available — preserve rather than delete them.

## Editing notes

- Preserve the existing table column counts and alignment markers (`:--------:`) so tables render correctly on GitHub.
- Markdown content is the deliverable; "verifying" a change means checking the table renders and links are well-formed, not running a tool.
