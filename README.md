# Robustness and Reliability in Sequential Analysis

**A Comparative Evaluation of E-Values and Standard Significance Testing**

MSc thesis in Statistics, ETH Zürich, 2026. Author: Kilian Graef. Advisor: Lukas Meier.

This repository contains the complete Quarto source. All analyses and simulations are embedded in the chapter files and reproduce on render.

## Contents

- `index.qmd` — title metadata and abstract
- `01_introduction.qmd` … `07_chapter6.qmd` — chapters: introduction, foundations of e-values, safe tests, e-processes and confidence sequences, FDR control with e-values, ACTG 175 / BCG case study, discussion
- `99_bibliography.qmd`, `myReferences.bib` — bibliography
- `_quarto.yml` — book configuration
- `latex/my-template.tex`, `ETH*.sty`, `ETH*.str` — ETH SfS LaTeX template

## Reproducing

Requires [Quarto](https://quarto.org), a LaTeX distribution (pdflatex), and R with:
`safestats` (0.8.7), `speff2trial` (1.0.5), `metadat` (1.6-0), `BiasedUrn` (2.0.12), `survival`, `dplyr`, `kableExtra`.

```
quarto render
```

Datasets (ACTG 175, BCG vaccine trials) load at render time from the `speff2trial` and `metadat` CRAN packages; no data files are stored here. A full render takes several minutes due to the permutation and operating-characteristic simulations. Seeds are fixed in the source, so all reported numbers reproduce exactly.

The signed declaration of originality is part of the official submission only and is not distributed. The template inserts it via \includepdf{confirmation-originality-scan.pdf} at the end of latex/my-template.tex; to render from a clone, delete that \includepdf block or place any one-page PDF with that filename in the project root.

## License

MIT (code and text of this repository). The ETH SfS template files retain their original terms.
