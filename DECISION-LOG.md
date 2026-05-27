# Decision Log

*Why the course looks the way it does.*

> Living document. Decisions are numbered sequentially, never deleted. If we change our minds, we mark the old entry `Superseded` and write a new one.
> Entries below D-015 are retroactive reconstructions from our chat history. Entries from D-016 onward are logged in real time.
> *For navigation: GitHub renders a sticky outline panel on the right; in VS Code use the Outline view in the Explorer sidebar.*

---

## Table of Contents

- [How to read this log](#how-to-read-this-log)
- [D-001 — Two parallel courses, separate but aware of each other](#d-001--two-parallel-courses-separate-but-aware-of-each-other)
- [D-002 — Course structured as 8 phases, ~40 sessions, no fixed timeline](#d-002--course-structured-as-8-phases-40-sessions-no-fixed-timeline)
- [D-003 — Format mix: concept-then-code, with periodic challenge-first sessions](#d-003--format-mix-concept-then-code-with-periodic-challenge-first-sessions)
- [D-004 — Priorities ranked, with reproducibility treated as substrate](#d-004--priorities-ranked-with-reproducibility-treated-as-substrate)
- [D-005 — User level recalibrated: true beginner with high motivation](#d-005--user-level-recalibrated-true-beginner-with-high-motivation)
- [D-006 — Windows 11 toolchain specifics](#d-006--windows-11-toolchain-specifics)
- [D-007 — VS Code as primary markdown/notes editor](#d-007--vs-code-as-primary-markdownnotes-editor)
- [D-008 — Four operating documents at the repo root](#d-008--four-operating-documents-at-the-repo-root)
- [D-009 — JHU Coursera specialisation: don't take, but borrow selectively](#d-009--jhu-coursera-specialisation-dont-take-but-borrow-selectively)
- [D-010 — Maps promoted to two full sessions](#d-010--maps-promoted-to-two-full-sessions)
- [D-011 — Vector graphics editor: awareness only, no hands-on](#d-011--vector-graphics-editor-awareness-only-no-hands-on)
- [D-012 — Session 8.0 added: Data storytelling principles](#d-012--session-80-added-data-storytelling-principles)
- [D-013 — Operating documents updated in batches, not continuously](#d-013--operating-documents-updated-in-batches-not-continuously)
- [D-014 — External resources used as scaffolding, not parallel paths](#d-014--external-resources-used-as-scaffolding-not-parallel-paths)
- [D-015 — Decision log reconstructed retroactively from chat history](#d-015--decision-log-reconstructed-retroactively-from-chat-history)
- [D-016 — R4DS (2e) chosen as primary spine reading for Phases 1-3](#d-016--r4ds-2e-chosen-as-primary-spine-reading-for-phases-1-3)
- [D-017 — File-type tagging and status convention in atlas](#d-017--file-type-tagging-and-status-convention-in-atlas)
- [D-018 — Two-course atlas split: R course full, stats course inventory only](#d-018--two-course-atlas-split-r-course-full-stats-course-inventory-only)
- [D-019 — In-file TOCs adopted as standard for operating documents](#d-019--in-file-tocs-adopted-as-standard-for-operating-documents)
- [D-020 — Session checklists and How-to recipes added to standard structure](#d-020--session-checklists-and-how-to-recipes-added-to-standard-structure)
- [D-021 — Clarifications file added; convention documented as Recipe 5](#d-021--clarifications-file-added-convention-documented-as-recipe-5)
- [D-022 — "From your atlas" renamed to "Curated reading"](#d-022--from-your-atlas-renamed-to-curated-reading)
- [Pending decisions](#pending-decisions-not-yet-entered)

---

## How to read this log

Each entry has:

- **D-XXX** — the decision identifier
- **Date** — when the decision was made (or, for retroactive entries, our best reconstruction)
- **Status** — Adopted / Superseded by D-YYY / Reverted
- **Affects** — what part of the course or process this touches
- **Context** — what was on the table
- **Decision** — what we chose
- **Reasoning** — why this over alternatives
- **Implications** — what changes elsewhere
- **Things to revisit later** — loose ends

---

## D-001 — Two parallel courses, separate but aware of each other

**Date:** 2026-05-21
**Status:** Adopted
**Affects:** Course architecture, cross-references

**Context:**
A separate stats and meta-analysis course already existed in the same Project, built around Justin Zeltzer's Z Statistics videos plus a dedicated meta-analysis phase using Harrer et al.'s *Doing Meta-Analysis with R*, the Cochrane Handbook, Borenstein et al., and the metafor ecosystem. The question was whether the new R course should subsume the stats course, merge with it, or stay separate.

**Decision:**
Keep them as two separate courses. The R course is the spine for tooling and computation; the stats course is the spine for theory and methods. Both live in the same Project so they can reference each other.

**Reasoning:**
- They serve different goals (R fluency vs. statistical fluency)
- Merging would create a 60+ session monster
- Keeping them separate lets each have a clean structure
- Cross-references give us the benefits of integration without the cost

**Implications:**
- Phase 6 of the R course explicitly bridges to the stats course (regression, simulation, meta-analysis methods)
- Sessions will include `↔ stats course` callouts where topics touch
- I can search the parallel course's chats when relevant

**Things to revisit later:**
- Whether the R course Phase 6.5 (meta-analysis in R) duplicates too much from the stats course's Phase 4 — adjust if so

---

## D-002 — Course structured as 8 phases, ~40 sessions, no fixed timeline

**Date:** 2026-05-21
**Status:** Adopted
**Affects:** Whole course

**Context:**
You wanted modular 30 min – 2 hr sessions, extended timeline acceptable, learning by doing.

**Decision:**
Eight phases progressing from setup through fluency to advanced topics:
0. Setting the Stage
1. R Fluency Foundations
2. Data Wrangling Mastery
3. Visualisation: Solid → Stunning
4. Reproducibility & Communication
5. Programming in R
6. Statistical Computing in R
7. Modern R Ecosystem
8. AI-Assisted Workflow & Staying Current

**Reasoning:**
- Spiral structure (revisit ideas at deeper levels) rather than linear
- Each phase ends with a portfolio artifact
- Reproducibility woven through, not isolated
- Total ~40 sessions is enough to cover advanced beginner → intermediate without bloat

**Implications:**
- Sessions get incrementally harder, but each is self-contained
- COURSE-MAP tracks completion phase-by-phase

**Things to revisit later:**
- Whether Phase 5 (programming) is too lean — may need expansion if functions/iteration feel rushed

---

## D-003 — Format mix: concept-then-code, with periodic challenge-first sessions

**Date:** 2026-05-21
**Status:** Adopted
**Affects:** Session structure

**Context:**
You picked two formats out of four: (1) concept + heavily commented code + "try this", and (4) challenge-first: try it, then I explain.

**Decision:**
Default to format (1). Periodically — every 4–6 sessions or when a topic suits it — use format (4) to stretch.

**Reasoning:**
- Default format suits genuine beginners (lower cognitive load)
- Challenge-first format builds confidence and problem-solving when used selectively
- Mixing prevents passivity

**Implications:**
- Each session flags its format at the top
- Challenge-first sessions need careful curation — not every topic suits them

---

## D-004 — Priorities ranked, with reproducibility treated as substrate

**Date:** 2026-05-21
**Status:** Adopted
**Affects:** Course weighting, examples, content emphasis

**Context:**
You ranked five priorities. You explicitly said reproducibility/Git/GitHub shouldn't be on a "what do you like most" list — it's essential and applied everywhere.

**Decision:**
Priority weighting:
1. Practical evidence-synthesis workflows (highest)
2. AI-assisted coding fluency
3. Beautiful publication-ready visualisation
4. Modern/cutting-edge R ecosystem
5. Reproducibility — treated as **substrate**, woven into every session, not ranked or boxed off

**Reasoning:**
- Your framing of reproducibility as "essential everywhere" is correct and reframes the course design
- Evidence synthesis at the top means examples lean toward systematic-review data
- AI-fluency at #2 means it becomes a thread, not a finale
- Visualisation at #3 justifies the Phase 3 depth

**Implications:**
- Examples are evidence-synthesis-flavoured from day one
- AI-assisted reflection appears from Phase 1 onward (not just Phase 8)
- Phase 3 (visualisation) gets generous treatment
- Git/GitHub appears in every session as habit, not as a "Git Week"

---

## D-005 — User level recalibrated: true beginner with high motivation

**Date:** 2026-05-21
**Status:** Adopted
**Affects:** Phase 1 pacing, assumptions throughout

**Context:**
You self-described as "advanced beginner" but answered "Installed it, written a few lines, mostly copy-pasted" when pressed. Honest self-assessment matters more than the label.

**Decision:**
Treat you as a true beginner with high motivation. Slow Phase 1. Never assume prior exposure without re-grounding.

**Reasoning:**
- No bad habits to unlearn — actually good news
- Refreshers and "tiny theory" are explicitly part of your stated learning style
- Better to over-explain Phase 1 and accelerate later than the reverse

**Implications:**
- Phase 1 slightly slower than originally planned
- Frequent mini-theory boxes
- Assumes nothing from the stats course beyond what we've covered there

---

## D-006 — Windows 11 toolchain specifics

**Date:** 2026-05-21
**Status:** Adopted
**Affects:** Phase 0 install steps, ongoing workflow

**Context:**
You're on Windows 11. Some installation and workflow details differ from Mac/Linux.

**Decision:**
- Install Rtools alongside R (required on Windows for some package compiles)
- Use Git Bash for command-line Git work (cleanest experience on Windows)
- Flag Windows-specific gotchas in sessions (file paths, line endings, OneDrive conflicts)

**Reasoning:**
- Macs and Linux have compilers built in; Windows doesn't — pre-emptive Rtools avoids confusing future errors
- Git Bash ships with Git for Windows and avoids PowerShell quirks

**Implications:**
- Session 0.1 has Windows-specific install steps
- File paths in examples use forward slashes or the `here` package, not backslashes
- We avoid OneDrive-synced folders for the repo

---

## D-007 — VS Code as primary markdown/notes editor

**Date:** 2026-05-22
**Status:** Adopted
**Affects:** Toolchain

**Context:**
You needed a way to read and edit `.md` files comfortably on Windows. Options were VS Code, Obsidian, RStudio's markdown mode, or plain Notepad.

**Decision:**
VS Code, with extensions *Markdown All in One* (by `yzhang`) and *markdownlint* (by David Anson). Signed in with GitHub account. Settings Sync enabled. Word wrap on, autosave on.

**Reasoning:**
- VS Code grows with you (Positron is based on it; AI coding tools integrate with it)
- Free, well-supported, ubiquitous
- GitHub sign-in removes friction in Session 0.2
- The two extensions cover ~90% of markdown editing needs

**Implications:**
- Markdown editing experience is consistent and pleasant
- You're partly familiarised with VS Code before we eventually meet Positron in Phase 8

---

## D-008 — Four operating documents at the repo root

**Date:** 2026-05-22
**Status:** Adopted
**Affects:** Repository structure

**Context:**
You proposed serialised running summaries to track evolving decisions. The conversation expanded into a need for separate operational documents.

**Decision:**
Four documents at the repo root, each with one job:
- `COURSE-MAP.md` — what we're learning (the plan)
- `DECISION-LOG.md` — why the plan looks like this (the reasoning)
- `LOGISTICS-HANDBOOK.md` — how we work (the operations)
- `RESOURCE-ATLAS.md` — what external materials support each session (the scaffolding)

**Reasoning:**
- Separating concerns prevents the COURSE-MAP from becoming a kitchen-sink document
- A dedicated DECISION-LOG captures *reasoning chains*, not just outcomes
- A LOGISTICS-HANDBOOK frees you from remembering how we operate — it's documented
- A RESOURCE-ATLAS lets external resources reinforce the spine without overwhelming

**Implications:**
- Four documents to maintain, but each is short and focused
- DECISION-LOG entries are numbered and never deleted
- Updates are batched, not constant, to avoid download churn

**Things to revisit later:**
- If any of these documents becomes a chore in three months, kill or merge it

---

## D-009 — JHU Coursera specialisation: don't take, but borrow selectively

**Date:** 2026-05-22
**Status:** Adopted
**Affects:** Course content (Phases 3 and 8)

**Context:**
You shared the Johns Hopkins "Data Visualization & Dashboarding with R" Coursera specialisation. The question was whether to take it in parallel, replace our course with it, or pick from it.

**Decision:**
Stay primary with our course. Borrow three things from JHU:
1. Dedicated spatial/mapping content (initially proposed as light-touch — see D-010 for revision)
2. A vector-graphics-editor awareness segment (initially as a session — see D-011 for revision)
3. A data storytelling lens applied to the capstone (new session 8.0)

Skip: animated figures (`gganimate`), flexdashboard.

**Reasoning:**
- Most JHU material overlaps with our Phases 1–3 and 7
- JHU teaches R Markdown + flexdashboard (a generation behind Quarto + Quarto Dashboards)
- No Git, no AI-fluency, no evidence-synthesis flavour in JHU
- But three things are genuinely worth borrowing

**Implications:**
- Phase 3 grows
- Phase 8 gains a session
- If you ever want a Johns Hopkins certificate, take only their Course 5 (capstone) after our course ends

**Things to revisit later:**
- Whether to formally enrol in JHU Course 3 (their spatial/animation course) once we reach Phase 3, for video reinforcement

---

## D-010 — Maps promoted to two full sessions

**Date:** 2026-05-22
**Status:** Adopted (revises part of D-009)
**Affects:** Phase 3 (visualisation)

**Context:**
D-009 initially proposed maps as a single "light-touch" session, on the reasoning that evidence synthesis rarely needs maps directly. You corrected this with concrete use cases.

**User correction (verbatim):**
> "We actually need maps. To show geographic coverage of evidence (some use cases: heatmap of countries by number of eligible studies in the SR, overlaying the heatmap with prevalence of anaemia)."

**Decision:**
Add two new sessions:
- **3.6 Maps in R: foundations** (~90 min) — `sf` package, coordinate reference systems, reading shapefiles, basic choropleths
- **3.7 Evidence-mapping workflows** (~90 min) — layering data sources (study counts + prevalence overlays), bivariate maps, `leaflet` for interactivity, exporting maps for publication and web

**Reasoning:**
- The use cases you described (study coverage maps, prevalence overlays) are direct outputs of evidence synthesis
- Two sessions properly cover both static publication maps and interactive maps
- Examples can use real datasets from your work later

**Implications:**
- Phase 3 grows from 5 sessions to 7
- Total course grows from ~39 to ~41 sessions
- I should ask, when we reach Phase 3, whether you have a real dataset (study counts by country) you'd like to use as the worked example

**Things to revisit later:**
- Once we get there, whether to add `evidencemap` / `evidencemapr` packages if you share specific datasets

---

## D-011 — Vector graphics editor: awareness only, no hands-on

**Date:** 2026-05-22
**Status:** Adopted (revises part of D-009)
**Affects:** Phase 3, Session 3.3

**Context:**
D-009 initially proposed a dedicated session on Inkscape for figure polish. You said you wanted just enough awareness to know what it brings, not hands-on practice.

**User direction (verbatim):**
> "I THINK WE SHOULD TOUCH IT JUST TO HAVE AN IDEA what that will bring to my work. don't need detailed hands on materials."

**Decision:**
Fold a 15-minute segment into Session 3.3 (publication design). Cover:
- Vector vs raster images and why journals care
- That Inkscape exists, is free, and the export-tweak-save loop
- When it's worth using (rarely) vs when it signals you should fix the code (usually)
- Why we stay in code 95% of the time (reproducibility)

No installation, no exercises.

**Reasoning:**
- Awareness is real value: knowing what a colleague means when they say "I cleaned this up in Inkscape"
- Full hands-on would steal time from code-based polish, which is more reproducible

**Implications:**
- Session 3.3 grows slightly but remains within its 90-minute budget
- No new session added for this

---

## D-012 — Session 8.0 added: Data storytelling principles

**Date:** 2026-05-22
**Status:** Adopted (from D-009)
**Affects:** Phase 8

**Context:**
The JHU capstone emphasises "data storytelling" — a real communication craft beyond visualisation skill. Our Phase 8 originally had four sessions.

**Decision:**
Add **Session 8.0 — Data storytelling principles** before the existing AI-assisted sessions. Cover: audience, narrative arc, sequencing of figures, choosing what to leave out.

**Reasoning:**
- Storytelling distinguishes a competent analyst from an influential one
- Worth its own session, not buried inside the capstone
- Pairs naturally with the AI sessions that follow (you'll be asking Claude to help structure narratives)

**Implications:**
- Phase 8 grows from 4 sessions to 5
- Total course now 42 sessions

---

## D-013 — Operating documents updated in batches, not continuously

**Date:** 2026-05-22
**Status:** Adopted
**Affects:** Workflow

**Context:**
Decisions accumulate over conversations. Updating documents after every micro-decision creates download churn for you.

**Decision:**
Track changes in chat. Regenerate operating documents only when:
- You explicitly say "let's update" or
- A logical batch is complete (e.g. after a major course-direction conversation)

**Reasoning:**
- Reduces friction (fewer download-and-replace cycles)
- Keeps documents stable enough that you trust their versions
- Forces us to pause and consolidate periodically

**Implications:**
- Pending changes are tracked in chat between updates
- When updates happen, multiple changes go in together

---

## D-014 — External resources used as scaffolding, not parallel paths

**Date:** 2026-05-22
**Status:** Adopted (pending resource list)
**Affects:** Course design philosophy, future RESOURCE-ATLAS

**Context:**
You have a collection of books, courses, and other materials on stats, reviews/meta-analyses, R, and visualisation. The question was how to incorporate them without overwhelming the course or duplicating effort.

**Your framing:**
> "I am thinking our course as the spine — the building on the beginner-level know-hows I already have to stand me firmly on the intermediate level... taking time to utilize all these highly rated resources within our journey."

**Decision:**
Our course is the spine. External resources are mapped session-by-session as scaffolding, categorised as:
- **Must-read** — central to the session
- **Should-read** — clarifies or deepens
- **Reference-only** — useful when stuck
- **Exercise-source** — drills and practice

Resources that don't map anywhere are kept in a "parking lot" — known about but not used.

**Reasoning:**
- Avoids the failure mode of dumping a 12-book reading list and feeling overwhelmed
- Lets each session reach for the right resource at the right moment
- Honours the work you've already done collecting good materials

**Implications:**
- Once you share the resource list, I'll produce `RESOURCE-ATLAS.md` mapping each item to sessions
- Each delivered session will include a small box pointing to relevant atlas entries
- For books, you've read TOCs but not contents — atlas will mark TOC-read status

**Things to revisit later:**
- After Phase 2 or 3, audit which resources are actually being used. Demote unused ones.

---

## D-015 — Decision log reconstructed retroactively from chat history

**Date:** 2026-05-22
**Status:** Adopted
**Affects:** This document

**Context:**
You proposed a serialised decision log. The question was whether to start from now or back-fill earlier decisions.

**Decision:**
Reconstruct retroactively from chat history. Mark all entries before this one as retroactive in their context. From D-016 forward, log decisions in real time.

**Reasoning:**
- Honest baseline beats fragmentary memory
- Reasoning chains are most useful when complete
- The reconstruction itself was a one-time cost worth paying

**Implications:**
- Entries D-001 to D-014 above are reconstructions, not contemporaneous records
- Entries D-016 onward will include "Drafted in chat: [date]" timestamps when they were originally discussed

---

## D-016 — R4DS (2e) chosen as primary spine reading for Phases 1-3

**Date:** 2026-05-27
**Status:** Adopted
**Affects:** RESOURCE-ATLAS, Phases 1-3

**Context:**
You asked for a recommendation on whether *R for Data Science* (Wickham, Çetinkaya-Rundles, Grolemund) should be the primary spine reading. You have nine R books in your collection that overlap considerably.

**Decision:**
Use *R for Data Science (2e)* — the online 2023 edition at [r4ds.hadley.nz](https://r4ds.hadley.nz) — as the primary companion text for Phases 1-3. Treat it as the "first read" for each session: read the relevant chapter *before* or *during* the session. Other R books become reference-only for these phases.

**Reasoning:**
- Tidyverse-first, matching the course philosophy
- Free, frequently updated online
- Maps almost 1:1 onto Phase 1-3 session content
- Exercises at the end of every chapter with solutions
- Written by the people who built the tidyverse
- Peng's *R Programming* and Matloff's *Art of R Programming* are excellent but base-R focused — better positioned as reference-only or as Phase 5 (programming) primary reading

**Implications:**
- Each Phase 1-3 session will name a specific R4DS chapter as must-read
- The 2e online edition supersedes the older PDF you have
- Peng and Matloff get repositioned in Phase 5 instead

---

## D-017 — File-type tagging and status convention in atlas

**Date:** 2026-05-27
**Status:** Adopted
**Affects:** RESOURCE-ATLAS

**Context:**
The first draft of the atlas didn't make resource format obvious at a glance. You requested explicit tags for file types and consistent status defaults.

**Decision:**
- Every offline resource gets a file-type tag: `[PDF]`, `[PPTX]`, `[R]`, `[Rmd]`, `[HTML]`, `[DOCX]`, `[CSV]`, `[TXT]`, `[ZIP]`
- Online resources get `[ONLINE]` with a hyperlink to the canonical URL
- Status defaults to `U` (untouched) for all resources in this initial build
- You update status manually as you read

**Reasoning:**
- File-type tags let you predict opening cost (PPT = quick skim, PDF book = commitment)
- Consistent default for status avoids spurious "T" or "P" claims I can't verify
- Hyperlinks make online resources one-click accessible

**Implications:**
- Atlas section 5 reorganised: Viechtbauer 2021 listed before Viechtbauer 2025 (pedagogical order)
- Atlas section 7 (free resources you should have) is fully hyperlinked

---

## D-018 — Two-course atlas split: R course full, stats course inventory only

**Date:** 2026-05-27
**Status:** Adopted
**Affects:** RESOURCE-ATLAS structure

**Context:**
Most of your collected resources serve the stats course, not the R course. Forcing them into R course sessions would distort the atlas.

**Decision:**
Atlas serves both courses but in different depths:
- **Part A (sections 1-4):** R course resources, fully mapped session-by-session
- **Part B (section 5):** Stats course resources, inventoried with likely placement noted but not deeply mapped
- The stats course will have its own atlas built when we next update it

**Reasoning:**
- Each course deserves its own session-level mapping
- A single document with both fully mapped would be overwhelming
- Section 5 acts as a "starting point" for the stats course atlas later

**Implications:**
- When you bring up the stats course again, we'll build its atlas using section 5 of this one as the inventory baseline
- The "for the stats course" tag in the R course atlas is a navigation aid, not a placeholder

---

## D-019 — In-file TOCs adopted as standard for operating documents

**Date:** 2026-05-27
**Status:** Adopted
**Affects:** All four operating documents

**Context:**
You asked about sticky left-panel TOC for the markdown documents. Pure markdown can't render sticky panels natively.

**Decision:**
- Every operating document has a clickable in-file TOC at the top
- For sticky-panel experience: use VS Code's Outline view (Explorer sidebar), or GitHub's auto-generated outline panel once the repo is live
- For HTML output with sticky left TOC: deferred to Phase 4 (Quarto), where any markdown can be rendered to HTML with that feature

**Reasoning:**
- In-file TOC works everywhere with zero setup
- VS Code and GitHub both render heading outlines automatically
- HTML rendering with sticky panels is a Phase 4 concern, not a pre-launch one

**Implications:**
- All four operating documents now have TOC at the top
- The "in any viewer" navigation hint appears in each document's header
- Future operating documents follow the same convention

---

## D-020 — Session checklists and How-to recipes added to standard structure

**Date:** 2026-05-27
**Status:** Adopted
**Affects:** LOGISTICS-HANDBOOK, all future session files

**Context:**
While preparing to start Session 0.1, you raised three practical concerns: (1) needing a checklist within each session that you could come back to, (2) needing a clear pattern for taking your own notes, (3) needing instructions for viewing markdown outlines in different modes. You then suggested folding the latter two into the Logistics Handbook as documented recipes.

**Decision:**
Two changes:

1. Add **Session checklist** as a standard component of every session file, with three sections: Pre-session / During session / Post-session. Placed at top of file, just after header and TOC.
2. Add **section 16: How-to recipes** to LOGISTICS-HANDBOOK, with each recipe following the format: Problem → Alternatives considered → Recommended approach → How to do it.

Initial recipes:
- Recipe 1: Taking notes in session files
- Recipe 2: Reading markdown with an outline / TOC visible
- Recipe 3: Where to put files on Windows (and why not OneDrive)
- Recipe 4: VS Code setup for this course

**Reasoning:**
- Session checklists turn each session into a self-contained checkpoint you can resume anytime
- The recipe format preserves *reasoning chains* (the alternatives section) so future-you doesn't second-guess past decisions
- Centralising operational know-how in the handbook prevents it from being lost in chat
- Recipes 3 and 4 retroactively document decisions we'd already made implicitly

**Implications:**
- Session 0.1 retrofitted with new checklist + atlas pointer + My notes section
- All future sessions follow the new template
- LOGISTICS-HANDBOOK section 7.1 updated to reflect the new session anatomy
- Recipes will grow over time as new recurring tasks emerge

**Things to revisit later:**
- After Phase 1, audit which recipes are actually being used. Demote unused ones.
- Consider extracting recipes into a separate file if section 16 grows beyond ~8-10 entries.

---


## D-021 — Clarifications file added; convention documented as Recipe 5

**Date:** 2026-05-27
**Status:** Adopted
**Affects:** Repository structure, LOGISTICS-HANDBOOK

**Context:**
Across sessions 0.1 and 0.2 you'd asked several clarifying questions (about C/C++ compilation, Git staging, VS Code extension choices, account sign-in) and noticed that some answers were absorbed into recipes while others were just floating in chat history. You asked whether we were compiling these clarifications. We weren't.

**Decision:**
Create `clarifications.md` at the repo root. Organise by topic section. Back-fill with entries from chat history so far (four entries across three topics). Document the convention as Recipe 5 in LOGISTICS-HANDBOOK.

Format of each entry: question phrased as searchable, asked-during session, tags, short answer, longer explanation, see-also links.

Workflow going forward: when a clarification is worth keeping, Claude drafts an entry inline marked *"Draft entry for clarifications.md"* — same mechanic as the Decision Log.

**Reasoning:**
- Reference material needs a searchable home, not chat history
- Topic-organised structure scales; per-session "Clarifications" subsections don't (duplication, cross-session lookup is painful)
- Premature organisation into cheatsheets would over-engineer; single file now, spin out cheatsheets later when topics mature

**Implications:**
- New file `clarifications.md` at repo root (initial back-fill: 4 entries)
- LOGISTICS-HANDBOOK gains Recipe 5
- Future sessions: Claude proposes draft entries; you paste them in
- When a topic section grows to ~3-4 entries, spin out as `cheatsheets/<topic>.md`

**Things to revisit later:**
- After Phase 1, audit whether clarifications are actually being captured or whether the convention is being skipped
- First spin-out is likely `git-essentials` cheatsheet (already has 1 entry)

---

## D-022 — "From your atlas" renamed to "Curated reading"

**Date:** 2026-05-27
**Status:** Adopted
**Affects:** All future session files, LOGISTICS-HANDBOOK section 7.1 and 9.3

**Context:**
Sessions 0.1 and 0.2 included a section titled *"From your atlas"* pointing to resources in RESOURCE-ATLAS.md. You requested renaming this to *"Curated reading"*.

**Decision:**
From Session 1.1 onward, use **"Curated reading"** as the section title. Update LOGISTICS-HANDBOOK references accordingly. Past session files (0.1, 0.2) retain old name unless retrofitted.

**Reasoning:**
- "Curated reading" is more descriptive and doesn't require knowing what "atlas" means as a concept
- The function of the section is clearer at a glance
- Easier for future-you scanning a session months later

**Implications:**
- Session anatomy updated in LOGISTICS-HANDBOOK section 7.1
- Resource Atlas section 9.3 example updated
- The RESOURCE-ATLAS document itself keeps its name (the *atlas* metaphor still works for the inventory; the *curation* is the per-session pointer)

---


## Pending decisions (not yet entered)

These will become D-023 onward when finalised:

- *(none right now — meta-setup complete)*

---

*End of decision log.*
