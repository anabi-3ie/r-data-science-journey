# Resource Atlas

*External resources mapped to course sessions. Scaffolding for the spine.*

> Living document. Updated as resources are added, used, or re-evaluated.
> Last updated: 2026-05-27 (final pre-launch build).
> *For navigation: GitHub renders a sticky outline panel on the right; in VS Code use the Outline view in the Explorer sidebar; in any viewer, the TOC below is clickable.*

---

## Table of Contents

- [1. How to read this atlas](#1-how-to-read-this-atlas)
- [2. The spine: one primary text per phase](#2-the-spine-one-primary-text-per-phase)
- [3. Phase-by-phase mapping (R course)](#3-phase-by-phase-mapping-r-course)
  - [Phase 0 — Setting the Stage](#phase-0--setting-the-stage)
  - [Phase 1 — R Fluency Foundations](#phase-1--r-fluency-foundations)
  - [Phase 2 — Data Wrangling Mastery](#phase-2--data-wrangling-mastery)
  - [Phase 3 — Visualisation: Solid → Stunning](#phase-3--visualisation-solid--stunning)
  - [Phase 4 — Reproducibility & Communication](#phase-4--reproducibility--communication)
  - [Phase 5 — Programming in R](#phase-5--programming-in-r)
  - [Phase 6 — Statistical Computing in R](#phase-6--statistical-computing-in-r)
  - [Phase 7 — The Modern R Ecosystem](#phase-7--the-modern-r-ecosystem)
  - [Phase 8 — AI-Assisted Workflow & Staying Current](#phase-8--ai-assisted-workflow--staying-current)
- [4. The AI-in-evidence-synthesis dossier (Phase 8 pull-out)](#4-the-ai-in-evidence-synthesis-dossier-phase-8-pull-out)
- [5. Part B — Stats course resources (inventory only)](#5-part-b--stats-course-resources-inventory-only)
  - [5.1 Viechtbauer 2021 Core Meta-Analysis Course](#51-viechtbauer-2021-core-meta-analysis-course-12-lectures)
  - [5.2 Viechtbauer 2025 Advanced MA Training](#52-viechtbauer-2025-advanced-ma-training-3-days)
  - [5.3 Polanin 2020–21 SR/MA Workshop](#53-polanin-202021-srma-workshop-11-sessions)
  - [5.4 MATI Training (excluding AI in MA dossier)](#54-mati-training-excluding-ai-in-ma-dossier)
  - [5.5 Reading Resources — Meta-Analysis](#55-reading-resources--meta-analysis)
  - [5.6 Reading Resources — Statistics & Econometrics](#56-reading-resources--statistics--econometrics)
- [6. Parking lot](#6-parking-lot)
- [7. The "you should have these" list (free, online)](#7-the-you-should-have-these-list-free-online)
- [8. How resources will be used during sessions](#8-how-resources-will-be-used-during-sessions)
- [9. Pending work](#9-pending-work)
- [10. Statuses — how to maintain this](#10-statuses--how-to-maintain-this)

---

## 1. How to read this atlas

### 1.1 Categories

Every resource is tagged with one category per session it serves:

- **Must-read** — central to the session. Engage with this before or during.
- **Should-read** — clarifies or deepens the session. Recommended.
- **Reference-only** — useful when stuck or for depth on a sub-topic. Don't read cover-to-cover.
- **Exercise-source** — drills and practice problems beyond what the session itself provides.

A resource can be *must-read* for one session and *reference-only* for another.

### 1.2 File-type tags

Every offline resource carries a tag indicating its format:

| Tag | Meaning |
|-----|---------|
| `[PDF]` | PDF document |
| `[PPTX]` | PowerPoint slides |
| `[DOCX]` | Word document |
| `[R]` | R script |
| `[Rmd]` | R Markdown document |
| `[HTML]` | HTML page (rendered from Rmd, viewable in browser) |
| `[CSV]` | Comma-separated values data |
| `[TXT]` | Plain text data |
| `[TRE]` | Phylogenetic tree file |
| `[ONLINE]` | Web resource — clickable link provided |

### 1.3 Status tags

Tracking what you've actually engaged with:

- **U** = untouched *(default for all entries in this initial build)*
- **T** = TOC read only
- **P** = partially read / dipped into
- **R** = read in full
- **E** = enrolled / accessing (for courses)

### 1.4 Two-course split

Resources are organised in two main parts:

- **Part A (sections 1–4)** — R course (this course, the spine we're working through)
- **Part B (section 5)** — Stats course (your parallel meta-analysis course)

Cross-references are flagged where a resource serves both.

---

## 2. The spine: one primary text per phase

For each phase, one resource takes the lead. Read this alongside the session; everything else is supplementary.

| Phase | Primary companion text | Status |
|-------|----------------------|--------|
| 0 | [*Happy Git with R*](https://happygitwithr.com) — Bryan `[ONLINE]` ⚠️ | U |
| 1 | [*R for Data Science (2e)*](https://r4ds.hadley.nz) — Wickham et al. `[ONLINE]` | U |
| 2 | [*R for Data Science (2e)*](https://r4ds.hadley.nz) — Wickham et al. `[ONLINE]` | U |
| 3 | [*ggplot2: Elegant Graphics for Data Analysis (3e)*](https://ggplot2-book.org) `[ONLINE]` ⚠️ + *R Graphics Cookbook* `[PDF]` | U |
| 4 | [*Quarto Guide*](https://quarto.org/docs/guide/) — Posit `[ONLINE]` ⚠️ | U |
| 5 | [*R Packages (2e)*](https://r-pkgs.org) — Wickham & Bryan `[ONLINE]` ⚠️ + *The Art of R Programming* — Matloff `[PDF]` | U |
| 6 | [*Applied Statistics with R*](https://book.stat420.org/) — Dalpiaz `[ONLINE]` + [*Introduction to Econometrics with R*](https://www.econometrics-with-r.org/) — Hanck et al. `[ONLINE]` | U |
| 7 | [*Mastering Shiny*](https://mastering-shiny.org) `[ONLINE]` ⚠️ + [*Tidy Modeling with R*](https://www.tmwr.org/) `[ONLINE]` ⚠️ | U |
| 8 | Course-built; no single text | — |

⚠️ = recommended free online resource you don't have downloaded yet. See [section 7](#7-the-you-should-have-these-list-free-online) for the full list.

---

## 3. Phase-by-phase mapping (R course)

For each session, the resources placed there with category, status, and brief reasoning.

### Phase 0 — Setting the Stage

#### Session 0.1 — Install & configure (R, RStudio, Rtools, Git, GitHub)

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Happy Git with R*](https://happygitwithr.com) — Bryan `[ONLINE]` | Should-read | U | Best installation walkthrough for Git + RStudio integration. Chapters 4–7 specifically. |
| MATI: *Notes - AI in Meta-Analysis.docx* `[DOCX]` | Reference-only | U | Not for this session, but worth knowing it's there once you're set up. |

#### Session 0.2 — First R Project, `here` package, GitHub connection, first commit

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Happy Git with R*](https://happygitwithr.com) — Bryan `[ONLINE]` | Must-read | U | Chapters 9–15. The definitive guide for this exact workflow. |
| [*R for Data Science (2e)*](https://r4ds.hadley.nz/workflow-scripts) — Ch 8 (Workflow: scripts and projects) `[ONLINE]` | Reference-only | U | Project structure best practices. |

---

### Phase 1 — R Fluency Foundations

**Primary text:** [*R for Data Science (2e)*](https://r4ds.hadley.nz) — chapters 1–5

#### Session 1.1 — R as a calculator, vectors, types, the assignment ritual

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 2](https://r4ds.hadley.nz/workflow-basics) `[ONLINE]` | Must-read | U | Cleanest intro to objects, names, calls. |
| *R Programming for Data Science* — Peng `[PDF]` (Ch 4-5) | Should-read | U | Stronger on the base-R mental model; types, atomic vectors. |
| *The Art of R Programming* — Matloff `[PDF]` (Ch 2 vectors) | Reference-only | U | When you want to understand vectors *deeply* later. |

#### Session 1.2 — Data frames, tibbles, meeting the tidyverse

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 1, 3](https://r4ds.hadley.nz/data-visualize) `[ONLINE]` | Must-read | U | First contact with the tidyverse mindset. |
| *R Programming for Data Science* — Peng `[PDF]` (data frames chapter) | Should-read | U | Base-R data frame vs tibble — useful contrast. |
| *R Cookbook* (r.cookbook.pdf) `[PDF]` | Reference-only | U | Quick lookup for one-line "how do I…" questions. |

#### Session 1.3 — The pipe (`|>` vs `%>%`) and the tidyverse mental model

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 4 (Workflow: code style)](https://r4ds.hadley.nz/workflow-style) `[ONLINE]` | Must-read | U | Best contemporary explanation of the native pipe. |

#### Session 1.4 — Mini-project: explore a real evidence-synthesis dataset

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 1 (Data visualisation)](https://r4ds.hadley.nz/data-visualize) `[ONLINE]` | Must-read | U | Sets up the data-explore loop you'll use forever. |
| Polanin Session 05 — *Intro to R.pptx* `[PPTX]` | Should-read | U | A second pass at the same material from a meta-analysis-specific lens. |
| Polanin: `BAIforYouth.csv` `[CSV]` | Exercise-source | U | Real meta-analysis dataset — perfect for an exploratory project. |

---

### Phase 2 — Data Wrangling Mastery

**Primary text:** [*R for Data Science (2e)*](https://r4ds.hadley.nz) — chapters 5–13

#### Session 2.1 — `dplyr` deep dive

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 5 (Data transformation)](https://r4ds.hadley.nz/data-transform) `[ONLINE]` | Must-read | U | The canonical dplyr chapter. |
| *Data Science with R: A Step By Step* `[PDF]` | Reference-only | U | Generic but has dplyr examples; useful if Wickham doesn't click. |

#### Session 2.2 — `tidyr`: pivoting, separating, nesting

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 6 (Data tidying)](https://r4ds.hadley.nz/data-tidy) `[ONLINE]` | Must-read | U | The "what is tidy data" foundational chapter. |
| [Wickham (2014) "Tidy Data" paper](https://www.jstatsoft.org/article/view/v059i10) `[ONLINE]` | Should-read | U | The original 2014 paper that defines the principle. Short, important. |

#### Session 2.3 — Strings, dates, factors

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 14 (strings)](https://r4ds.hadley.nz/strings), [Ch 16 (factors)](https://r4ds.hadley.nz/factors), [Ch 17 (dates)](https://r4ds.hadley.nz/datetimes) `[ONLINE]` | Must-read | U | One chapter per topic. |
| *R Cookbook* (r.cookbook.pdf) `[PDF]` | Reference-only | U | Quick lookup for regex and date format codes. |

#### Session 2.4 — Joining datasets + `janitor`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 19 (Joins)](https://r4ds.hadley.nz/joins) `[ONLINE]` | Must-read | U | Inner/left/full join logic. |

#### Session 2.5 — When tidyverse isn't enough: `data.table`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| *The Art of R Programming* — Matloff `[PDF]` (Ch 6-7 lists, data frames) | Should-read | U | Background mindset for understanding data.table's design choices. |
| [`data.table` introduction vignette](https://cran.r-project.org/web/packages/data.table/vignettes/datatable-intro.html) `[ONLINE]` | Must-read | U | The official intro vignettes are the best resource. |

---

### Phase 3 — Visualisation: Solid → Stunning

**Primary text:** [*ggplot2: Elegant Graphics for Data Analysis* (3e online)](https://ggplot2-book.org) + your *R Graphics Cookbook*

#### Session 3.1 — Grammar of graphics: the mental model

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| *The Grammar of Graphics* — Wilkinson `[PDF]` (Ch 1-3 only) | Should-read | U | The foundational theory ggplot2 is based on. |
| *ggplot2 Book* — ggplot2-Book09hWickham.pdf `[PDF]` (Ch 1) | Must-read | U | Wickham's translation of the grammar into R. |

#### Session 3.2 — `ggplot2` essentials: geoms, aesthetics, scales

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 1, 9-11](https://r4ds.hadley.nz/layers) `[ONLINE]` | Must-read | U | Where most beginners learn ggplot2. |
| *R Graphics Cookbook* `[PDF]` | Should-read | U | Recipe-style; perfect for "how do I make this exact plot?" |
| *ggplot2 Book* `[PDF]` | Reference-only | U | When you need to understand *why* a recipe works, not just copy it. |

#### Session 3.3 — Themes, fonts, colour, design for publication (+15-min vector-graphics-editor awareness)

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| *R Graphics Cookbook* `[PDF]` (themes & legends) | Must-read | U | Concrete recipes for publication look. |
| *ggplot2 Book* `[PDF]` (themes chapter) | Should-read | U | The systematic theory of theme elements. |
| *The Elements of Data Analytic Style* — Leek `[PDF]` | Should-read | U | Slim, opinionated, full of good "design for communication" instincts. |

#### Session 3.4 — Extensions: patchwork, ggtext, ggrepel, gghighlight

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [`patchwork` website](https://patchwork.data-imaginist.com) `[ONLINE]` | Must-read | U | Authoritative, by maintainer. |
| [`ggtext` website](https://wilkelab.org/ggtext/) `[ONLINE]` | Must-read | U | Same — short, authoritative. |
| [`ggrepel` vignette](https://cran.r-project.org/web/packages/ggrepel/vignettes/ggrepel.html) `[ONLINE]` | Must-read | U | All you need in 15 minutes. |

#### Session 3.5 — Tables that publish: `gt`, `gtsummary`, `flextable`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [`gt` package website](https://gt.rstudio.com) `[ONLINE]` | Must-read | U | Best-in-class documentation. |
| [`gtsummary` website](https://www.danieldsjoberg.com/gtsummary/) `[ONLINE]` | Must-read | U | Essential for descriptive tables in evidence synthesis. |
| [`flextable` book](https://ardata-fr.github.io/flextable-book/) `[ONLINE]` | Reference-only | U | When you need Word-output table polish. |

#### Session 3.6 — Maps in R: foundations

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Geocomputation with R*](https://r.geocompx.org) — Lovelace, Nowosad, Muenchow `[ONLINE]` ⚠️ | Should-read | U | The standard reference; chapters 1-2 for foundations. |
| [`sf` package vignettes](https://r-spatial.github.io/sf/) `[ONLINE]` | Must-read | U | The package's own docs are the best intro. |

#### Session 3.7 — Evidence-mapping workflows

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| MATI: *MATI_EGMs.pdf* `[PDF]` + *MATI_EGMs.pptx* `[PPTX]` | Must-read | U | Directly relevant to your work. Evidence gap maps are a sibling concept. |
| MATI: *Evidence Gap Maps in Education Research.pdf* `[PDF]` | Should-read | U | Real-world application examples. |
| MATI: `MathMeta_egm.csv` `[CSV]` | Exercise-source | U | Real EGM data — could become a worked example. |
| [`leaflet` for R website](https://rstudio.github.io/leaflet/) `[ONLINE]` | Must-read | U | The interactive-mapping package's own docs. |

---

### Phase 4 — Reproducibility & Communication

**Primary text:** [*Quarto Guide*](https://quarto.org/docs/guide/) (online, free)

#### Session 4.1 — Quarto fundamentals

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Quarto Guide*](https://quarto.org/docs/guide/) — Posit `[ONLINE]` | Must-read | U | Free, official, exhaustive. |
| [*R for Data Science (2e)* — Ch 28 (Quarto)](https://r4ds.hadley.nz/quarto) `[ONLINE]` | Should-read | U | Wickham's intro is gentler. |

#### Session 4.2 — Quarto for reports: HTML, Word, PDF

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Quarto Guide* — Output Formats](https://quarto.org/docs/output-formats/all-formats.html) `[ONLINE]` | Must-read | U | Different output formats have specific knobs. |

#### Session 4.3 — Git intermediate: branches, merges, pull requests

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Happy Git with R*](https://happygitwithr.com) — Bryan `[ONLINE]` | Must-read | U | Chapters on branches, push/pull, collaborating. |
| [*Pro Git*](https://git-scm.com/book/en/v2) — Chacon `[ONLINE]` | Reference-only | U | When Bryan isn't enough — the canonical Git book. |

#### Session 4.4 — Publishing: GitHub Pages + your live learning site

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Quarto Guide* — Quarto Websites](https://quarto.org/docs/websites/) `[ONLINE]` | Must-read | U | Quarto can publish to GitHub Pages with one config setting. |

---

### Phase 5 — Programming in R

**Primary text:** *The Art of R Programming* — Matloff + [*R Packages (2e)*](https://r-pkgs.org) for session 5.4

#### Session 5.1 — Writing functions

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 26 (Functions)](https://r4ds.hadley.nz/functions) `[ONLINE]` | Must-read | U | Wickham's intro to function-writing. |
| *The Art of R Programming* — Matloff `[PDF]` (Ch 7 programming structures) | Should-read | U | Deeper on R's function model. |
| [*Advanced R (2e)*](https://adv-r.hadley.nz) — Wickham `[ONLINE]` ⚠️ | Reference-only | U | When you want to understand functions as objects, environments. |

#### Session 5.2 — Iteration with `purrr`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R for Data Science (2e)* — Ch 27 (Iteration)](https://r4ds.hadley.nz/iteration) `[ONLINE]` | Must-read | U | The canonical `map` chapter. |

#### Session 5.3 — Errors, warnings, debugging

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Advanced R* — Ch 22 (Debugging)](https://adv-r.hadley.nz/debugging.html) `[ONLINE]` | Should-read | U | The standard guide. |
| *R Programming for Data Science* — Peng `[PDF]` (debugging chapter) | Should-read | U | Concrete examples. |

#### Session 5.4 — Your first mini-package

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*R Packages (2e)*](https://r-pkgs.org) — Wickham & Bryan `[ONLINE]` ⚠️ | Must-read | U | The definitive guide; concise enough to actually use. |

---

### Phase 6 — Statistical Computing in R

**Primary text:** [*Applied Statistics with R*](https://book.stat420.org/) — Dalpiaz + [*Introduction to Econometrics with R*](https://www.econometrics-with-r.org/) — Hanck et al.

This phase cross-links with the **stats course Phase 1-3**. Theory lives there; implementation here.

#### Session 6.1 — Descriptives & inference, the tidyverse way

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Introduction to Econometrics with R*](https://www.econometrics-with-r.org/) — Hanck et al. (Ch 2-3) `[ONLINE]` | Must-read | U | Modern, free, R-native treatment. |
| *Introductory Statistics* `[PDF]` | Reference-only | U | Theory backstop if confused. |
| [`gtsummary` website](https://www.danieldsjoberg.com/gtsummary/) `[ONLINE]` | Must-read | U | The package itself is the resource. |

#### Session 6.2 — Linear & generalised linear models + `broom`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Applied Statistics with R*](https://book.stat420.org/) — Dalpiaz (Ch 7-12) `[ONLINE]` | Must-read | U | Linear models, model selection, GLMs — all in clean R. |
| [*Introduction to Econometrics with R*](https://www.econometrics-with-r.org/) — Hanck et al. (Ch 4-6) `[ONLINE]` | Must-read | U | Stronger on interpretation and causal framing. |
| *Mostly Harmless Econometrics* — Angrist & Pischke `[PDF]` | Should-read | U | Causal thinking framework. Read selectively. |
| *Introductory Econometrics: A Modern Approach* — Wooldridge `[PDF]` | Reference-only | U | When you need depth on a specific topic. |
| [*The Effect*](https://theeffectbook.net/) — Huntington-Klein `[ONLINE]` | Should-read | U | Modern, readable intro to causal design with R examples. |

#### Session 6.3 — Modern interpretation: `marginaleffects` & `emmeans`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [`marginaleffects` website](https://marginaleffects.com/) `[ONLINE]` | Must-read | U | This package's documentation is the field's best reference. |

#### Session 6.4 — Simulation & bootstrapping basics

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Applied Statistics with R*](https://book.stat420.org/) — Dalpiaz (relevant sections) `[ONLINE]` | Must-read | U | Has worked examples of simulation. |
| ↔ Stats course Phase 3 (Week 12-13) — bootstrapping content | Cross-reference | — | Theory there, R implementation here. |

#### Session 6.5 — Meta-analysis in R: `meta`, `metafor`, `robumeta`

This session is the **most overlapping with your stats course**. The R course gives you the *syntax fluency*; the stats course gives you the *methodology*. Resources mostly live in the stats course atlas, but the following are essential for the R angle here.

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| *Conducting Meta-Analyses in R with the metafor Package* — Viechtbauer (2010) `[PDF]` | Must-read | U | The canonical metafor paper. |
| Viechtbauer 2021 course — `lecture04_meta_analysis_with_r.pdf` `[PDF]` + `code_r_bcg (2).r` `[R]` | Must-read | U | Walk through this lecture and run its R code. |
| Polanin Sessions 06-07 R scripts + data `[R]` `[CSV]` | Exercise-source | U | Effect size + synthesis worked examples. |
| [*Doing Meta-Analysis with R*](https://bookdown.org/MathiasHarrer/Doing_Meta_Analysis_in_R/) — Harrer et al. `[ONLINE]` | Should-read | U | Hands-on companion to metafor. |
| [`metafor` project site](https://www.metafor-project.org/) `[ONLINE]` | Reference-only | U | Wolfgang Viechtbauer's own package site. |
| ↔ Stats course Phase 4 — all meta-analysis methodology | Cross-reference | — | Theory and methods live there. |

---

### Phase 7 — The Modern R Ecosystem

**Primary text:** Mostly package websites; [*Tidy Modeling with R*](https://www.tmwr.org/) and [*Mastering Shiny*](https://mastering-shiny.org) for two specific sessions.

#### Session 7.1 — Pipeline orchestration with `targets`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*targets* user manual](https://books.ropensci.org/targets/) — Will Landau `[ONLINE]` ⚠️ | Must-read | U | Best-in-class documentation. |

#### Session 7.2 — Dependency management with `renv`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [`renv` website](https://rstudio.github.io/renv/) `[ONLINE]` | Must-read | U | Posit's docs are the resource. |

#### Session 7.3 — Interactive apps: Shiny + Quarto Live

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Mastering Shiny*](https://mastering-shiny.org) — Wickham `[ONLINE]` ⚠️ | Must-read | U | The definitive book on Shiny. |

#### Session 7.4 — Modern ML in R: `tidymodels`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [*Tidy Modeling with R*](https://www.tmwr.org/) — Kuhn & Silge `[ONLINE]` ⚠️ | Must-read | U | Written by tidymodels' creators. |

#### Session 7.5 — Big-ish data: `arrow`, `duckdb`, `polars`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [`arrow` for R website](https://arrow.apache.org/docs/r/) `[ONLINE]` | Must-read | U | The official arrow-for-R docs. |
| [`duckdb` R package](https://duckdb.org/docs/api/r) `[ONLINE]` | Must-read | U | DuckDB Labs maintain excellent docs. |

#### Session 7.6 — R + Python = `reticulate`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [`reticulate` website](https://rstudio.github.io/reticulate/) `[ONLINE]` | Must-read | U | Posit's own integration guide. |
| *Data Science from Scratch* (Python) `[PDF]` | Reference-only | U | Now relevant — Python primer if you bridge to Python proper. |

---

### Phase 8 — AI-Assisted Workflow & Staying Current

This phase has a **dedicated dossier** in [section 4](#4-the-ai-in-evidence-synthesis-dossier-phase-8-pull-out) (MATI AI materials).

#### Session 8.0 — Data storytelling principles

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| *The Elements of Data Analytic Style* — Leek `[PDF]` | Must-read | U | Slim and pointed. Read fully. |
| *Naked Statistics* — Wheelan `[PDF]` | Should-read | U | Communication-of-statistics craft. Read selectively. |

#### Session 8.1 — The Posit AI stack: `ellmer`, `chattr`, `gander`, `btw`

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [`ellmer` website](https://ellmer.tidyverse.org/) `[ONLINE]` | Must-read | U | Posit-maintained. |
| [`chattr` website](https://mlverse.github.io/chattr/) `[ONLINE]` | Must-read | U | Posit-maintained. |
| [`gander` website](https://simonpcouch.github.io/gander/) `[ONLINE]` | Must-read | U | New, fast-evolving — check current state. |
| [`btw` website](https://posit-dev.github.io/btw/) `[ONLINE]` | Must-read | U | Same. |

#### Session 8.2 — Positron + Positron Assistant

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [Positron documentation](https://positron.posit.co/) `[ONLINE]` | Must-read | U | The official docs. |

#### Session 8.3 — Prompting Claude / Copilot for data work

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [Anthropic's prompting guide](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview) `[ONLINE]` | Must-read | U | Authoritative. |
| MATI: *Notes - AI in Meta-Analysis.docx* `[DOCX]` | Should-read | U | Domain-specific application. |

#### Session 8.4 — Your "staying current" system

| Resource | Category | Status | Why |
|----------|----------|--------|-----|
| [R-Weekly](https://rweekly.org) `[ONLINE]` | Must-read | U | Already in COURSE-MAP's stay-current corner. |
| [Posit Blog](https://posit.co/blog/), [R-Bloggers](https://www.r-bloggers.com/) `[ONLINE]` | Reference-only | U | Curated discovery channels. |

---

## 4. The AI-in-evidence-synthesis dossier (Phase 8 pull-out)

You have a remarkable concentration of papers and notes on AI in evidence synthesis. Rather than scatter these across sessions, treat them as a **dossier** for Phase 8 (and as background reading you can dip into any time).

**Location:** *MATI Training Materials / AI in Meta-Analysis*

| Item | Category | Status | Why it matters |
|------|----------|--------|----------------|
| *Notes - AI in Meta-Analysis.docx* `[DOCX]` | Must-read | U | Your own notes — start here. |
| *Automatic extraction of quantitative data to conduct MA.pdf* `[PDF]` | Should-read | U | Direct relevance to evidence synthesis workflows. |
| *Computer-assisted screening in systematic evidence synthesis.pdf* `[PDF]` | Should-read | U | Same. |
| *Machine Learning Tools To (Semi-)Automate Evidence Synthesis.pdf* `[PDF]` | Should-read | U | Broader survey of the field. |
| *MetaMate_Wang&Luo_0811.pdf* `[PDF]` | Reference-only | U | Specific tool, useful for awareness. |
| *Statistical stopping criteria for automated screening in SRs.pdf* `[PDF]` | Reference-only | U | Niche but methodologically important. |
| *Technology-assisted title and abstract screening for SRs.pdf* `[PDF]` | Should-read | U | Practical screening implications. |
| *Toward systematic review automation.pdf* `[PDF]` | Should-read | U | Vision paper for the field. |
| *authorship-determination-scorecard.pdf* `[PDF]` | Reference-only | U | Adjacent topic. |

**Recommendation:** read in two passes — once after Session 8.3 (for context on prompting), once during your final capstone.

---

## 5. Part B — Stats course resources (inventory only)

The bulk of your meta-analysis-specific materials belong to the **stats course**, not this R course. They are listed here so you have one complete inventory, but their *primary placement* will be in the stats course atlas (to be built when we next update that course).

### 5.1 Viechtbauer 2021 Core Meta-Analysis Course (12 lectures)

This is the **most directly useful course** in your collection for the stats track. Treat it as the spine for the stats course's Phase 4.

| Item | Format | Likely placement in stats course |
|------|--------|----------------------------------|
| `introduction.pdf` | `[PDF]` | Stats Phase 4 — Course intro |
| `lecture01_intro_to_meta_analysis.pdf` | `[PDF]` | Stats Phase 4 — Core: introduction |
| `lecture02_outcome_measures.pdf` | `[PDF]` | Stats Phase 4 — Core: effect sizes |
| `lecture03_meta_analytic_models.pdf` | `[PDF]` | Stats Phase 4 — Core: fixed vs random effects |
| `lecture04_meta_analysis_with_r.pdf` | `[PDF]` | Stats Phase 4 + ↔ R course Phase 6.5 |
| `lecture05_moderator_analysis.pdf` | `[PDF]` | Stats Phase 4 — Core: meta-regression |
| `lecture06_heterogeneity.pdf` | `[PDF]` | Stats Phase 4 — Core: heterogeneity |
| `lecture07_diagnostics.pdf` | `[PDF]` | Stats Phase 4 — Core: diagnostics |
| `lecture08_refined_tests_and_cis.pdf` | `[PDF]` | Stats Phase 4 — Core: refined inference |
| `lecture09_publication_bias.pdf` | `[PDF]` | Stats Phase 4 — Core: publication bias |
| `lecture10_methods_2x2_data.pdf` | `[PDF]` | Stats Phase 4 — Binary outcomes |
| `lecture11_ma_of_regression_models.pdf` | `[PDF]` | Stats Phase 4 — Extensions |
| `lecture12_other_topics.pdf` | `[PDF]` | Stats Phase 4 — Wrap-up |
| Exercises 1a-4 + solutions | `[PDF]` | Stats Phase 4 throughout |
| R code files (code_r_bcg, _2x2, _diagnostics, etc.) | `[R]` | Stats Phase 4 + ↔ R course Phase 6.5 |
| Data files (data_bcg, data_diagnostics, data_massage, data_rosiglitazone) | `[TXT]` | Stats Phase 4 |
| Reference PDFs (Chalmers, Colditz, Durlak, Laird, LaValley, Normand, Raudenbush, Riley, Viechtbauer 2007/2010/2021, etc.) | `[PDF]` | Stats Phase 4 — supporting reading |
| `ma_definitions.pdf`, `metafor_commands.pdf`, `literature.pdf` | `[PDF]` | Stats Phase 4 — quick references |
| Study PDFs (Ferguson 1949, Hernandez-Reif 1998, Comstock 1976, Leivadi 1999) | `[PDF]` | Stats Phase 4 — example studies |

**Status for all items: U.**

### 5.2 Viechtbauer 2025 Advanced MA Training (3 days)

For **after** the stats course's core meta-analysis phase, not during.

#### Day 1 — Standard models, publication bias

| Item | Format | Likely placement |
|------|--------|------------------|
| `introduction.pdf`, `lec01_standard_models.pdf`, `lec02_publication_bias.pdf` | `[PDF]` | Stats Phase 4 — Advanced |
| `lecture01.r`, `lecture02.r` | `[R]` | Stats Phase 4 — Advanced |
| `exercise01.r` + `_sol.r`, `exercise02.r` + `_sol.r` | `[R]` | Stats Phase 4 — Advanced exercises |
| `dat_bcg.txt` | `[TXT]` | Stats Phase 4 |
| Literature folder (9 reference PDFs) | `[PDF]` | Stats Phase 4 — supporting reading |

#### Day 2 — Multilevel and multivariate

| Item | Format | Likely placement |
|------|--------|------------------|
| `lecture03_multilevel_models.pdf`, `lecture04_multivariate_models.pdf` | `[PDF]` | Stats Phase 4 — Multilevel/multivariate |
| `lecture03.r`, `lecture04.r` | `[R]` | Stats Phase 4 |
| `exercise03.r` + `_solution.r`, `exercise04.r` + `_solution.r` | `[R]` | Stats Phase 4 |
| `dat_jackson2013.txt` | `[TXT]` | Stats Phase 4 |

#### Day 3 — Network MA, phylogenetic models, MA of regressions

| Item | Format | Likely placement |
|------|--------|------------------|
| `lecture05_network_meta_analysis.pdf`, `lecture06_crossed_phylo_models.pdf`, `lecture07_ma_of_regression_models.pdf` | `[PDF]` | Stats Phase 4+ — Extensions |
| `lecture05.r`, `lecture06.r`, `lecture07.r` | `[R]` | Stats Phase 4+ |
| `exercise05.r` + `_solution.r`, `exercise06.r` | `[R]` | Stats Phase 4+ |
| `dat_jackson2013.txt`, `dat_myco.txt`, `dat_network.txt` | `[TXT]` | Stats Phase 4+ |
| `tree_fungi.tre`, `tree_plants.tre` | `[TRE]` | Stats Phase 4+ — phylogenetic models |

**Status for all items: U.**

### 5.3 Polanin 2020–21 SR/MA Workshop (11 sessions)

Lower-level pedagogy than Viechtbauer. Useful as a gentler second pass.

| Item | Format | Likely placement |
|------|--------|------------------|
| Session 01 - Introduction & Inclusion Criteria | `[PPTX]` | Stats Phase 4 — SR process |
| Session 02 - Literature Searching | `[PPTX]` | Stats Phase 4 — SR process |
| Session 03 - Screening the Literature | `[PPTX]` | Stats Phase 4 — SR process |
| Session 04 - Coding the Literature | `[PPTX]` | Stats Phase 4 — SR process |
| Session 05 - Intro to R | `[PPTX]` | ↔ R course Phase 1 — secondary perspective |
| Session 06 - Calculating Effect Sizes | `[PPTX]` | Stats Phase 4 — Core MA |
| Session 07 - Synthesizing Effect Sizes | `[PPTX]` | Stats Phase 4 — Core MA |
| Session 08 - Heterogeneity | `[PPTX]` | Stats Phase 4 — Core MA |
| Session 09 - Publication Bias | `[PPTX]` | Stats Phase 4 — Core MA |
| Session 10 - Interpreting, Reporting | `[PPTX]` | Stats Phase 4 — Wrap-up |
| Session 11 - Project Management | `[PPTX]` | Stats Phase 4 — Wrap-up |
| `1. Effect Size Calculations Example.R` | `[R]` | Stats Phase 4 + ↔ R course Phase 6.5 |
| `3. Effect Size Synthesis Example.R` | `[R]` | Stats Phase 4 + ↔ R course Phase 6.5 |
| `5. Explaining Heterogeneity Example.R` | `[R]` | Stats Phase 4 |
| `7. Publication Bias Example.R` | `[R]` | Stats Phase 4 |
| `BAIforYouth.csv`, `TDV_ES.csv` | `[CSV]` | Stats Phase 4 + ↔ R course Phase 1.4 (exercise data) |
| `Meta-Analysis Workshop_Tentative Schedule_3ie.docx` | `[DOCX]` | Admin — reference only |

**Status for all items: U.**

### 5.4 MATI Training (excluding AI in MA dossier)

#### EGMs

| Item | Format | Placement |
|------|--------|-----------|
| *Notes - EGMs.docx* | `[DOCX]` | Stats Phase 4 — SR types + ↔ R course 3.7 |
| *MATI_EGMs.pdf* / *.pptx* | `[PDF]` `[PPTX]` | Stats Phase 4 + ↔ R course 3.7 |
| *Evidence Gap Maps in Education Research.pdf* | `[PDF]` | Stats Phase 4 + ↔ R course 3.7 |
| `MathMeta_egm.csv` | `[CSV]` | ↔ R course 3.7 exercise data |

#### Effect Size Calculation

| Item | Format | Placement |
|------|--------|-----------|
| *Notes - Effect Size Calculations.docx* | `[DOCX]` | Stats Phase 4 — ES |
| *Intro escalc MATI.pdf* / *.pptx* | `[PDF]` `[PPTX]` | Stats Phase 4 — ES |
| *AdjustedESanswers.Rmd* / *.html* | `[Rmd]` `[HTML]` | Stats Phase 4 — ES exercises |
| *Using EscalcMATI.Rmd* / *Using-EscalcMATI.html* | `[Rmd]` `[HTML]` | Stats Phase 4 — ES exercises |
| `es_clust2.R` / `es_clust2-2-1.R` | `[R]` | Stats Phase 4 — ES |
| *Complex Effect Sizes-4.pdf* | `[PDF]` | Stats Phase 4 — Advanced ES |
| *Final_WWC-HandbookVer5_0-0-508.pdf* | `[PDF]` | Stats Phase 4 — WWC standards reference |
| *WWC-Procedures-Handbook-v4-1-508.pdf* | `[PDF]` | Stats Phase 4 — WWC reference |
| *jresematheduc.46.3.0331 (1).pdf* | `[PDF]` | Stats Phase 4 — application |
| Data files: `CorrEx22.csv`, `LOREx22.csv`, `SMDEx22.csv`, `dyson (1).csv`, `dyson2all (1).csv`, `prepost.csv` | `[CSV]` | Stats Phase 4 — exercises |

#### Meta Models and RVE

| Item | Format | Placement |
|------|--------|-----------|
| *MR Intro MATI-1.pdf* / *.pptx* | `[PDF]` `[PPTX]` | Stats Phase 4 — Meta-regression |
| *MR Intro MATI.Rmd* / *.html* | `[Rmd]` `[HTML]` | Stats Phase 4 — Meta-regression |
| *Meta-Analysis_ Intro.pdf* | `[PDF]` | Stats Phase 4 — Refresher |
| *Planning for Effect Size Heterogeneity MATI.pdf* / *.pptx* | `[PDF]` `[PPTX]` | Stats Phase 4 — Heterogeneity |
| *Tipton et al GM MA PB 2023.pdf* | `[PDF]` | Stats Phase 4 — RVE methods |

#### MetaSEM

| Item | Format | Placement |
|------|--------|-----------|
| *MASEM MATI 2025-3.pdf* | `[PDF]` | Stats Phase 4+ — Extensions |
| *MASEM preparing for tssem2-3.pdf* | `[PDF]` | Stats Phase 4+ — Extensions |
| *Using webMASEM 2025-1.pdf* | `[PDF]` | Stats Phase 4+ — Extensions |
| *Jansen et al 2019.pdf* | `[PDF]` | Stats Phase 4+ — Application |

#### Project Management of SRs

| Item | Format | Placement |
|------|--------|-----------|
| *Review Protocol Template (1).docx* | `[DOCX]` | Stats Phase 4 — Process |
| *Systematic Review and Meta-Analysis Project Management.pdf* / *.pptx* | `[PDF]` `[PPTX]` | Stats Phase 4 — Process |

#### Publication Bias and Missing Data

| Item | Format | Placement |
|------|--------|-----------|
| *Exploring Missing Data and Power in MA MATI.pdf* / *.pptx* | `[PDF]` `[PPTX]` | Stats Phase 4 — Pub bias |
| *MATI_2025_selective_reporting.pdf* / *.pptx* | `[PDF]` `[PPTX]` | Stats Phase 4 — Pub bias |
| *publication_bias-1.Rmd* / *publication_bias-2.R* | `[Rmd]` `[R]` | Stats Phase 4 — Pub bias exercises |

#### Scoping Reviews

| Item | Format | Placement |
|------|--------|-----------|
| *Scoping Reviews.pdf* | `[PDF]` | Stats Phase 4 — SR types |
| *Scoping in planning for a new SRMA.docx* | `[DOCX]` | Stats Phase 4 — SR types |

#### Screening

| Item | Format | Placement |
|------|--------|-----------|
| *Screening for eligible studies.pdf* | `[PDF]` | Stats Phase 4 — SR process |

**Status for all items: U.**

### 5.5 Reading Resources — Meta-Analysis

| Book | Format | Placement |
|------|--------|-----------|
| *Introduction to Meta-Analysis* — Borenstein et al. | `[PDF]` | Stats Phase 4 — Spine reading (theory) |
| *Handbook of Meta-Analysis* — Schmid et al. | `[PDF]` | Stats Phase 4 — Reference, advanced topics |
| *Conducting Meta-Analyses in R with metafor* — Viechtbauer | `[PDF]` | Stats Phase 4 + ↔ R course Phase 6.5 |
| [*Doing Meta-Analysis with R*](https://bookdown.org/MathiasHarrer/Doing_Meta_Analysis_in_R/) — Harrer et al. | `[ONLINE]` | Stats Phase 4 — Hands-on companion |
| [`metafor` project site](https://www.metafor-project.org/doku.php/metafor) | `[ONLINE]` | Stats Phase 4 + R course Phase 6.5 — Reference |
| [`metafor` GitHub pages](https://wviechtb.github.io/metafor/index.html) | `[ONLINE]` | Stats Phase 4 — Reference |

**Status for all items: U.**

### 5.6 Reading Resources — Statistics & Econometrics

| Book | Format | Placement |
|------|--------|-----------|
| *Naked Statistics* — Wheelan | `[PDF]` | Stats Phase 1 — Refresher + ↔ R course 8.0 (storytelling) |
| *Statistics without Tears* | `[PDF]` | Stats Phase 1 — Refresher |
| *Introductory Statistics* | `[PDF]` | Stats Phase 1-2 — Refresher + foundation |
| *Mostly Harmless Econometrics* | `[PDF]` | Stats Phase 3 — Regression + ↔ R course 6.2 |
| *Introductory Econometrics* — Wooldridge | `[PDF]` | Stats Phase 3 — Regression (reference) |
| [*The Effect*](https://theeffectbook.net/) — Huntington-Klein | `[ONLINE]` | Stats Phase 3 — Modern alternative + ↔ R course 6.2 |
| [Stock & Watson *Intro to Econometrics*](https://www.sea-stat.com/wp-content/uploads/2020/08/James-H.-Stock-Mark-W.-Watson-Introduction-to-Econometrics-Global-Edition-Pearson-Education-Limited-2020.pdf) | `[PDF]` | Stats Phase 3 — Reference |
| [*Introduction to Econometrics with R*](https://www.econometrics-with-r.org/index.html) — Hanck et al. | `[ONLINE]` | ↔ R course Phase 6 — primary text |
| [*Applied Statistics with R*](https://book.stat420.org/) — Dalpiaz | `[ONLINE]` | ↔ R course Phase 6 — primary text |
| [*Introduction to Inferential Statistics*](https://bookdown.org/marc_trussler/IIS/index.html) — Trussler | `[ONLINE]` | Stats Phase 2 — Inference |
| *The Elements of Data Analytic Style* — Leek | `[PDF]` | R course 3.3 + 8.0 |

**Status for all items: U.**

---

## 6. Parking lot

Things that exist in your collection but don't have a clear home in either course.

| Resource | Format | Why parked |
|----------|--------|-----------|
| *Data Science from Scratch* (Python) | `[PDF]` | Python primer. Useful if/when you bridge to Python in R course Phase 7.6, but not before. |
| Various individual paper PDFs in literature folders | `[PDF]` | Already serve as deep-reference for specific topics; don't need atlas entries. |

---

## 7. The "you should have these" list (free, online)

Free, current, authoritative resources that meaningfully strengthen the spine. None are blockers — but bookmarking or downloading them at the start saves friction later.

| Resource | URL | When you'll need it |
|----------|-----|---------------------|
| *Happy Git with R* — Jenny Bryan | [happygitwithr.com](https://happygitwithr.com) | Sessions 0.2, 4.3 |
| *R for Data Science (2e)* — Wickham et al. | [r4ds.hadley.nz](https://r4ds.hadley.nz) | Phases 1-3 throughout |
| *ggplot2: Elegant Graphics for Data Analysis (3e)* — Wickham | [ggplot2-book.org](https://ggplot2-book.org) | Phase 3 throughout |
| *Quarto Guide* — Posit | [quarto.org/docs/guide](https://quarto.org/docs/guide/) | Phase 4 throughout |
| *R Packages (2e)* — Wickham & Bryan | [r-pkgs.org](https://r-pkgs.org) | Session 5.4 |
| *Advanced R (2e)* — Wickham | [adv-r.hadley.nz](https://adv-r.hadley.nz) | Phase 5 (deeper) |
| *Mastering Shiny* — Wickham | [mastering-shiny.org](https://mastering-shiny.org) | Session 7.3 |
| *Tidy Modeling with R* — Kuhn & Silge | [tmwr.org](https://www.tmwr.org/) | Session 7.4 |
| *Geocomputation with R* — Lovelace et al. | [r.geocompx.org](https://r.geocompx.org) | Sessions 3.6, 3.7 |
| *targets* manual — Will Landau | [books.ropensci.org/targets](https://books.ropensci.org/targets/) | Session 7.1 |
| *The Effect* — Huntington-Klein | [theeffectbook.net](https://theeffectbook.net/) | Session 6.2 + stats course |
| *Pro Git* — Chacon | [git-scm.com/book](https://git-scm.com/book/en/v2) | Session 4.3 (reference) |

**Recommendation:** bookmark them all now. Download PDF copies of the books only when you're about to start the relevant phase, so they don't gather dust.

---

## 8. How resources will be used during sessions

When I deliver each session, it'll include a short box near the top:

> **From your atlas**
> - Must-read: *R for Data Science (2e)* — Ch 5 `[ONLINE]`
> - Should-read: Polanin Session 05 `[PPTX]` (alternative perspective)
> - Exercise-source: `BAIforYouth.csv` `[CSV]`

This way you know what to read alongside the session without having to re-consult the atlas every time. The atlas itself is the inventory; the session is the trigger.

---

## 9. Pending work

- [ ] **Stats course atlas** — when we next touch the stats course, build the full Part B atlas there. The placements in [section 5](#5-part-b--stats-course-resources-inventory-only) are the starting point.
- [ ] **Bookmark / download** the "should have" resources from [section 7](#7-the-you-should-have-these-list-free-online)
- [ ] **Update statuses** as you read

---

## 10. Statuses — how to maintain this

When you read or use something, update its status tag in this file. The status field is the most important live information in the atlas. Don't over-engineer it — a quick `U` → `P` → `R` is enough.

If a resource turns out to be wrong-fit for the placement, change the category or move it. The atlas is wrong if it doesn't match your actual experience.

---

*End of atlas.*
