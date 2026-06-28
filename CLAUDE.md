# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

Awesome-FAS is a curated "awesome list" of Face Authentication Security resources — face anti-spoofing / presentation-attack detection / liveness detection papers, datasets, and benchmarks. It contains **only Markdown** (no source code, build, lint, or test tooling). All work is editing Markdown tables and links. The list is maintained by adding entries via pull requests/issues.

## Structure

- `README.md` — the main list. Sections in order: **Databases**, **Learning-based methods** (subsectioned by year: 2022, 2021, 2020, 2019-2018, Before 2018), **System / Mobile Applications**, **Attack**, **Notes**. The header's `# Contents` is a hand-maintained table of contents. The footer holds the maintainers' BibTeX citations.
- `Benchmarks/README.md` — links to external spreadsheets for intra-dataset and cross-dataset results.
- `Benchmarks/CASIA+REPLAY-ATTACK.md` — a benchmark table (methods sorted by HTER on the CASIA↔REPLAY-ATTACK cross-dataset protocol), with a legend mapping each method abbreviation to its paper.

## Conventions when adding entries

- **Databases** rows use columns: `Name | Release year | Attacks | Modalities | #subjects | #videos`. Name links to the dataset page; add a separate `[paper]` link when the dataset page differs from the paper.
- **Paper rows** (Learning-based / System / Attack) use columns: `Title | Venue | Note`. Title links to the paper PDF/page. Venue is an abbreviation + year (e.g. `T-IFS 2020`, `CVPR 2022`). The Note column carries tags like the method name, attack type (2D/3D), modality (RGB/IR/Depth), keywords (Domain generalization, Meta Learning, NAS), and a `[Code](url)` link when available.
- Place a new paper under the **year subsection matching its venue year**. Add ArXiv-only papers too, but per the Notes section they are "regarded not published" — collected for reference only.
- Venue abbreviations must be defined in the `# Notes` section at the bottom of `README.md`. If you introduce a new abbreviation, add it there.
- In `Benchmarks/CASIA+REPLAY-ATTACK.md`, keep the table sorted by the HTER (CASIA→REPLAY-ATTACK) column and add the method's expansion to the legend below the table.
- Strikethrough (`~~Name~~`) marks datasets/resources that are no longer available — preserve rather than delete them.

## Editing notes

- Preserve the existing table column counts and alignment markers (`:--------:`) so tables render correctly on GitHub.
- Markdown content is the deliverable; "verifying" a change means checking the table renders and links are well-formed, not running a tool.
