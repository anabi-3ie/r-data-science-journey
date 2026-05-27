# R for Data Science, Visualisation & Evidence Synthesis

**Your personalised learning journey — built around your role in evidence synthesis, your AI-fluency ambition, and your wish to stay current.**

> *Last updated: 2026-05-27. Updates triggered by phase changes only.*
> *For navigation: GitHub renders a sticky outline panel on the right; in VS Code use the Outline view in the Explorer sidebar; in any viewer, the TOC below is clickable.*

---

## Table of Contents

- [R for Data Science, Visualisation \& Evidence Synthesis](#r-for-data-science-visualisation--evidence-synthesis)
  - [Table of Contents](#table-of-contents)
  - [How to use this document](#how-to-use-this-document)
  - [Course philosophy](#course-philosophy)
  - [Course at a glance](#course-at-a-glance)
  - [Phase 0 — Setting the Stage](#phase-0--setting-the-stage)
  - [Phase 1 — R Fluency Foundations](#phase-1--r-fluency-foundations)
  - [Phase 2 — Data Wrangling Mastery](#phase-2--data-wrangling-mastery)
  - [Phase 3 — Visualisation: Solid → Stunning](#phase-3--visualisation-solid--stunning)
  - [Phase 4 — Reproducibility \& Communication](#phase-4--reproducibility--communication)
  - [Phase 5 — Programming in R](#phase-5--programming-in-r)
  - [Phase 6 — Statistical Computing in R](#phase-6--statistical-computing-in-r)
  - [Phase 7 — The Modern R Ecosystem](#phase-7--the-modern-r-ecosystem)
  - [Phase 8 — AI-Assisted Workflow \& Staying Current](#phase-8--ai-assisted-workflow--staying-current)
  - [Always-on threads (every session)](#always-on-threads-every-session)
  - [Cross-references with the Stats \& Meta-Analysis course](#cross-references-with-the-stats--meta-analysis-course)
  - [Tracking your progress](#tracking-your-progress)
    - [Reflections](#reflections)

---

## How to use this document

This is your **dashboard**. Open it at the start of every session. Tick boxes as you complete sessions. Add your own notes in the margins (`> my note: ...`).

Sessions are short (30 min – 2 hr) and modular. You can pause for days or weeks between phases without losing thread — each session reminds you of prerequisites.

Files for each session live at `XX-phase-name/session-NN-title/`.

---

## Course philosophy

1. **Spiral, not linear.** We revisit core ideas at deeper levels.
2. **Evidence-synthesis flavoured.** Examples come from your world: effect sizes, screening logs, extraction tables.
3. **Reproducibility is substrate, not topic.** Git, markdown, project structure weave through every session.
4. **AI-assisted from session 3 onward.** You learn R *and* learn to leverage Claude / Copilot / Positron Assistant in parallel.
5. **Stay-current corner in every session.** One real blog / talk / package / person to know — antidote to FOMO.

---

## Course at a glance

| Phase | Title | Sessions | Status |
|-------|-------|----------|--------|
| 0 | Setting the Stage | 2 | ☑ |
| 1 | R Fluency Foundations | 4 | ☐ |
| 2 | Data Wrangling Mastery | 5 | ☐ |
| 3 | Visualisation: Solid → Stunning | 7 | ☐ |
| 4 | Reproducibility & Communication | 4 | ☐ |
| 5 | Programming in R | 4 | ☐ |
| 6 | Statistical Computing in R | 5 | ☐ |
| 7 | The Modern R Ecosystem | 6 | ☐ |
| 8 | AI-Assisted Workflow & Staying Current | 5 | ☐ |

**Total: 42 sessions.** No deadline.

---

## Phase 0 — Setting the Stage

*Your toolchain, your folders, your first commit.* — **2 sessions**

- [x] **0.1** Install & configure: R, RStudio, Rtools, Git, GitHub account — *45 min*
- [x] **0.2** Project structure, the `here` package, your first repo & commit — *60 min*

---

## Phase 1 — R Fluency Foundations

*Calibration sessions. Not "intro to R" — a thoughtful refresher with new mental models.* — **4 sessions**

- [ ] **1.1** R as a calculator, vectors, types, the assignment ritual — *60 min*
- [ ] **1.2** Data frames, tibbles, and meeting the tidyverse — *90 min*
- [ ] **1.3** The pipe (`|>` vs `%>%`), and the tidyverse mental model — *45 min*
- [ ] **1.4** Mini-project: explore a real evidence-synthesis dataset — *90 min*

**End-of-phase artifact:** A clean exploratory script committed to GitHub.

---

## Phase 2 — Data Wrangling Mastery

*The unglamorous work that is 80% of real analysis.* — **5 sessions**

- [ ] **2.1** `dplyr` deep dive: filter, select, mutate, summarise, group_by — *90 min*
- [ ] **2.2** `tidyr`: pivoting wide↔long, separating, nesting — *75 min*
- [ ] **2.3** Strings, dates, factors: `stringr`, `lubridate`, `forcats` — *90 min*
- [ ] **2.4** Joining datasets + the `janitor` package — *60 min*
- [ ] **2.5** When tidyverse isn't enough: a tour of `data.table` — *60 min*

**End-of-phase artifact:** Messy real-world dataset → clean analytical-ready dataset, with a documented pipeline.

---

## Phase 3 — Visualisation: Solid → Stunning

*Your top-priority phase. Static, interactive, geographic, tabular — all of it.* — **7 sessions**

- [ ] **3.1** Grammar of graphics: the mental model — *60 min*
- [ ] **3.2** `ggplot2` essentials: geoms, aesthetics, scales — *90 min*
- [ ] **3.3** Themes, fonts, colour, design for publication *(includes 15-min awareness of vector graphics editors)* — *90 min*
- [ ] **3.4** Extensions: `patchwork`, `ggtext`, `ggrepel`, `gghighlight` — *75 min*
- [ ] **3.5** Tables that publish: `gt`, `gtsummary`, `flextable` — *90 min*
- [ ] **3.6** Maps in R: foundations (`sf`, CRS, basic choropleths) — *90 min*
- [ ] **3.7** Evidence-mapping workflows (study coverage + prevalence overlays, `leaflet`) — *90 min*

**End-of-phase artifact:** A publication-ready figure + a country evidence map from a real dataset.

---

## Phase 4 — Reproducibility & Communication

*Make your work transmissible. By the end, your learning journal is a live website.* — **4 sessions**

- [ ] **4.1** Quarto fundamentals: documents that render anywhere — *90 min*
- [ ] **4.2** Quarto for reports: HTML, Word, PDF — *60 min*
- [ ] **4.3** Git intermediate: branches, merges, pull requests — *75 min*
- [ ] **4.4** Publishing: GitHub Pages + your live learning site — *90 min*

**End-of-phase artifact:** A public website hosting your course notes.

---

## Phase 5 — Programming in R

*From R user to R developer. Compact and high-leverage.* — **4 sessions**

- [ ] **5.1** Writing functions: anatomy, defaults, return values — *75 min*
- [ ] **5.2** Iteration with `purrr`: `map`, `walk`, list-columns — *90 min*
- [ ] **5.3** Errors, warnings, debugging — *60 min*
- [ ] **5.4** Your first mini-package — *90 min*

---

## Phase 6 — Statistical Computing in R

*Cross-linked with your stats & meta-analysis course. The other course teaches theory; this teaches clean implementation in R.* — **5 sessions**

- [ ] **6.1** Descriptives & inference, the tidyverse way: `gtsummary`, `infer` — *90 min*
- [ ] **6.2** Linear & generalised linear models + `broom` — *90 min*
- [ ] **6.3** Modern interpretation: `marginaleffects` & `emmeans` — *75 min*
- [ ] **6.4** Simulation & bootstrapping basics — *90 min*
- [ ] **6.5** Meta-analysis in R: `meta`, `metafor`, `robumeta` (bridges to stats course) — *2 hr*

**End-of-phase artifact:** A reproducible meta-analysis report.

---

## Phase 7 — The Modern R Ecosystem

*Your antidote to FOMO. By the end you'll know what exists, what it's for, and roughly when to reach for it.* — **6 sessions**

- [ ] **7.1** Pipeline orchestration with `targets` (gold for living evidence syntheses) — *90 min*
- [ ] **7.2** Dependency management with `renv` — *45 min*
- [ ] **7.3** Interactive apps: a Shiny taste + Quarto Live — *90 min*
- [ ] **7.4** Modern ML in R: `tidymodels` tour — *2 hr*
- [ ] **7.5** Big-ish data: `arrow`, `duckdb`, `polars` — *75 min*
- [ ] **7.6** R + Python = `reticulate`, and the R-vs-Python honest conversation — *60 min*

---

## Phase 8 — AI-Assisted Workflow & Staying Current

*A capstone phase, not a single session.* — **5 sessions**

- [ ] **8.0** Data storytelling principles — *60 min*
- [ ] **8.1** The Posit AI stack: `ellmer`, `chattr`, `gander`, `btw` — *90 min*
- [ ] **8.2** Positron + Positron Assistant: the new editor in town — *60 min*
- [ ] **8.3** Prompting Claude / Copilot for data work: patterns that work — *75 min*
- [ ] **8.4** Your "staying current" system: R-Weekly, Bluesky, talks, papers — *45 min*

**Final capstone (optional):** Pick a real evidence-synthesis problem from your work and solve it end-to-end with everything you've learned.

---

## Always-on threads (every session)

- **Markdown notes** — `session-NN-notes.md`
- **Git commit** — at the end, with a meaningful message
- **Stay-current corner** — one fresh thing in this area
- **Cross-references** — links to other sessions and to the stats course
- **From your atlas** — pointer to the relevant entries in `RESOURCE-ATLAS.md`

---

## Cross-references with the Stats & Meta-Analysis course

These two courses are **deliberately separate but aware of each other**. Where they touch:

| This course | Stats course | How they relate |
|-------------|--------------|-----------------|
| Phase 6.1 (descriptives in R) | Descriptive statistics | Theory there, R implementation here |
| Phase 6.2 (GLMs in R) | Regression theory | Theory there, fitting & interpreting here |
| Phase 6.4 (simulation) | Sampling distributions | Theory there, simulation demos here |
| Phase 6.5 (meta-analysis in R) | Meta-analysis methods | Methods there, hands-on syntax here |

Explicit "↔ stats course" callouts appear inside relevant sessions.

---

## Tracking your progress

After each session, jot a one-line reflection at the bottom of this file:

```
- 2026-05-22 | S0.1 | Got R installed, surprised by how clean RStudio looks
```

This serves three purposes:
1. **Your memory** — three months in, you'll want to see what you've done.
2. **My context** — when you share the file with me later, I see your journey.
3. **Honest signal** — if three sessions in a row say "felt confused," that's data for me to recalibrate.

### Reflections

- 2026-05-28 | S0.1 + S0.2 | Toolchain installed and first commit pushed. The Git pane is less scary than I expected. I need to remember this through practice. Will create a new demo project.

---

*End of course map.*
