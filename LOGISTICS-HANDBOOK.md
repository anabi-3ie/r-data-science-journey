# Logistics Handbook

*How we operate. Where things live. How we coordinate.*

> Living document. Last updated: 2026-05-27.
> *For navigation: GitHub renders a sticky outline panel on the right; in VS Code use the Outline view in the Explorer sidebar; in any viewer, the TOC below is clickable.*

---

## Table of Contents

- [1. Mental model](#1-mental-model)
- [2. Where things live](#2-where-things-live)
- [3. The four operating documents](#3-the-four-operating-documents)
- [4. Tools we use and why](#4-tools-we-use-and-why)
- [5. How we exchange files](#5-how-we-exchange-files)
- [6. How we ask questions](#6-how-we-ask-questions)
- [7. Sessions: how they work](#7-sessions-how-they-work)
- [8. Decisions and how we log them](#8-decisions-and-how-we-log-them)
- [9. The Resource Atlas](#9-the-resource-atlas)
- [10. Cross-course coordination](#10-cross-course-coordination)
- [11. AI-assisted learning thread](#11-ai-assisted-learning-thread)
- [12. Staying current](#12-staying-current)
- [13. When things go wrong](#13-when-things-go-wrong)
- [14. End-of-session checklist](#14-end-of-session-checklist)
- [15. The handbook itself](#15-the-handbook-itself)
- [16. How-to recipes](#16-how-to-recipes)
  - [Recipe 1 — Taking notes in session files](#recipe-1--taking-notes-in-session-files)
  - [Recipe 2 — Reading markdown with an outline / TOC visible](#recipe-2--reading-markdown-with-an-outline--toc-visible)
  - [Recipe 3 — Where to put files on Windows (and why not OneDrive)](#recipe-3--where-to-put-files-on-windows-and-why-not-onedrive)
  - [Recipe 4 — VS Code setup for this course](#recipe-4--vs-code-setup-for-this-course)
  - [Recipe 5 — Capturing clarifications as we go](#recipe-5--capturing-clarifications-as-we-go)

---

## 1. Mental model

This journey has **three actors**:

- **You** — the learner. Owner of the local repository, the GitHub account, the final say on direction.
- **Claude (me)** — the teacher and course architect. I produce material, suggest changes, answer questions, and search past chats for context. I cannot reach your computer.
- **The repository** — the bridge. Files committed and pushed here are visible to both of us. Files only on your local machine are visible to only you.

Everything else in this handbook is mechanics for keeping these three in sync.

---

## 2. Where things live

### 2.1 Local folder

Path: `C:\Users\<YourName>\Documents\r-data-science-journey\`
(or wherever you've placed it — see [Recipe 3](#recipe-3--where-to-put-files-on-windows-and-why-not-onedrive))

Structure:

```
r-data-science-journey/
├── README.md                       ← public-facing intro
├── COURSE-MAP.md                   ← the plan: what we're learning
├── DECISION-LOG.md                 ← the reasoning: why the plan looks like this
├── LOGISTICS-HANDBOOK.md           ← this file
├── RESOURCE-ATLAS.md               ← external resources mapped to sessions
├── 00-setting-the-stage/
│   └── session-01-install/
│       └── session-01-notes.md
├── 01-r-fluency/
├── 02-data-wrangling/
├── 03-visualisation/
├── 04-reproducibility/
├── 05-programming/
├── 06-statistical-computing/
├── 07-modern-ecosystem/
├── 08-ai-and-staying-current/
├── cheatsheets/                    ← quick-reference cards
├── datasets/                       ← reusable example data
├── projects/                       ← bigger applied work
└── resources.md                    ← simple list of useful links
```

### 2.2 GitHub repository

Created in Session 0.2. URL pattern: `https://github.com/<your-username>/r-data-science-journey`

The repo is the **canonical source of truth** once it exists. Local edits that haven't been committed and pushed are still "in flight." Pushed commits are the official version.

### 2.3 What lives in this chat (and its successors)

Each chat session is conversational and **ephemeral as a venue** — but **searchable as a record** because we're inside a Project. I can search past chats within this Project. So:

- Conversational decisions live in chat
- The *outcome* of those decisions gets committed to the relevant document (DECISION-LOG, COURSE-MAP, etc.)
- I can find old context by searching past chats, but it's much faster if it's already in a committed document

---

## 3. The four operating documents

Each has one job. Don't mix them up.

| Document | Job | Updated when |
|----------|-----|--------------|
| `COURSE-MAP.md` | What we're learning | Sessions added/removed/reordered |
| `DECISION-LOG.md` | Why the plan looks like this | A real decision is made |
| `LOGISTICS-HANDBOOK.md` | How we work | Our process changes |
| `RESOURCE-ATLAS.md` | What external materials support each session | Resources added or status changes |

Session notes (`session-NN-notes.md`) are content, not operating documents. They live in phase folders.

---

## 4. Tools we use and why

### 4.1 Primary toolchain

| Tool | Purpose | Why this one |
|------|---------|--------------|
| **R** | The language | The whole point |
| **RStudio** | Primary IDE | Mature, stable, designed for R |
| **Rtools** | Compiles C/C++ in packages | Required on Windows |
| **VS Code** | Markdown editing, possibly later code | Best general-purpose editor; AI-integration-friendly |
| **Git** | Version control | Industry standard |
| **GitHub** | Hosting and bridge between us | Most universal; integrates with everything |
| **Git Bash** | Command line for Git on Windows | Cleanest Git experience on Windows |
| **Quarto** | Documents, reports, websites | Modern successor to R Markdown |
| **Inkscape** | (Awareness only) Vector graphics | Free, open-source, when code-only polish hits a limit |

### 4.2 What we explicitly chose not to use (and why)

- **Positron over RStudio (for now):** Positron is Posit's newer IDE and we'll explore it in Phase 8. RStudio is more stable and has more tutorials. We'll switch only if/when Positron clearly wins.
- **R Markdown:** Quarto replaces it. Old projects use R Markdown; we'll start fresh with Quarto.
- **flexdashboard:** Replaced by Quarto Dashboards. Modern equivalent, longer shelf life.
- **gganimate / animated figures:** Not relevant to evidence synthesis output.
- **OneDrive-synced folders for our repo:** Conflicts with Git. See [Recipe 3](#recipe-3--where-to-put-files-on-windows-and-why-not-onedrive).

### 4.3 VS Code configuration we've agreed

See [Recipe 4](#recipe-4--vs-code-setup-for-this-course) for the full step-by-step.

---

## 5. How we exchange files

### 5.1 You → me

**Before GitHub is set up:** paste contents in chat, or upload the file.

**After GitHub is set up:** just give me a URL like `https://github.com/<you>/r-data-science-journey/blob/main/COURSE-MAP.md` and I'll fetch it directly.

**For code with errors:** copy-paste the *exact* code and the *exact* error message. Not paraphrased. Verbatim.

**For data files:** small (<10 MB) — upload directly. Larger — commit to the repo's `datasets/` folder and share the URL.

### 5.2 Me → you

I produce files as artifacts. You download and place them in the right folder of your repo. Then commit when ready.

I will **never** edit your files directly. Every file you have was either downloaded from me or written by you.

### 5.3 Updates to existing documents

When I update an existing document (e.g. a new version of COURSE-MAP), I'll produce the full updated file. You replace the old one. Don't try to manually patch; it leads to drift.

To minimise download churn, I update the operating documents **in batches**, not every change. The triggers for an update:

- COURSE-MAP — when phase structure changes
- DECISION-LOG — when a decision is made and you say "log it"
- LOGISTICS-HANDBOOK — when our process actually changes
- RESOURCE-ATLAS — when you add resources or change their status

---

## 6. How we ask questions

### 6.1 You asking me

Just talk. No formal pattern needed. Useful conventions:

- **"Quick question:"** → I reply with a descriptive headline + plain language + paste-friendly formatting
- **"Ultra plain"** → strip all markdown, pure prose
- **"Walk me through"** → step-by-step explanation
- **"Why does this work?"** → I'll go into the *why*, not just the *how*
- **No prefix** → I read the question and respond in whatever format fits

For errors and stuck-points, the pattern is: *what you tried* → *what happened* → *what you expected*. Verbatim outputs > paraphrases.

### 6.2 Me asking you

Mid-session questions for calibration or preferences. I'll keep them short. If I'm asking multiple things, I'll use a structured format with selectable options where possible.

For clarification on direction (not knowledge), I'll explicitly mark it: *"Decision needed:"* — meaning we shouldn't proceed until you've weighed in.

---

## 7. Sessions: how they work

### 7.1 Anatomy of a session

Every session file has this structure:

1. **Header** — session number, title, phase, estimated time, format
2. **Session checklist** — pre/during/post tickboxes you can come back to
3. **Why this matters** (2–3 sentences linking to your work)
4. **Curated reading** (pointer to relevant resources in `RESOURCE-ATLAS.md`)
5. **Prerequisites** (what you need from earlier sessions)
6. **Mini-theory** (just enough framing)
7. **Walkthrough** (annotated code, run it, see what happens)
8. **Your turn** (2–4 exercises)
9. **Going deeper** (optional rabbit holes)
10. **Stay-current corner** (one fresh thing in the area)
11. **Commit message suggestion** (for the Git habit)
12. **Cross-references** (other sessions, stats course)
13. **How I'd ask Claude this** (meta-skill, from Phase 1 onward)
14. **My notes** (your space, at the bottom — see [Recipe 1](#recipe-1--taking-notes-in-session-files))

### 7.2 Session formats

You picked a mix:

- **Default:** concept → annotated code → "your turn" (most sessions)
- **Periodically:** challenge-first (here's a puzzle, try it, then I'll explain)

I'll flag the format at the top of each session.

### 7.3 Session length

30 min – 2 hr. Each session estimates its time. Treat it as a rough estimate, not a target.

If you find a session is taking much longer than estimated, that's data. Tell me.

### 7.4 Pace adjustments are welcome any time

- *"Slow down."*
- *"Skip ahead."*
- *"Shorter session today."*
- *"Pause this and come back to it."*

None of these are interruptions. They're calibration.

---

## 8. Decisions and how we log them

### 8.1 What counts as a decision

Worth logging:
- Adding or removing sessions
- Changing course priorities
- Choosing a tool over alternatives
- Reinterpreting your goals based on new information
- Adopting or rejecting an external influence

Not worth logging:
- Quick clarifications
- Minor wording choices
- One-off questions

### 8.2 The logging ritual

At the end of a session where we made a real decision:

1. I draft a Decision Log entry in chat
2. You confirm or edit it
3. You paste it into `DECISION-LOG.md` and commit
4. Future-you (and future-me, via past-chat search) can find it

Entries are numbered sequentially: `D-001`, `D-002`, etc.

### 8.3 Entry format

```
## D-XXX — [Short descriptive title]

Date: YYYY-MM-DD
Status: Adopted | Superseded by D-YYY | Reverted
Affects: [Phase / document / scope]

Context:
[What was happening, what we were considering]

Decision:
[What we chose]

Reasoning:
[Why this over alternatives]

Implications:
[What changes elsewhere as a result]

Things to revisit later:
[Loose ends, open questions]
```

### 8.4 Superseding, not deleting

If we change our minds, we **don't delete the old entry**. We mark its status as `Superseded by D-YYY` and write a new entry. The reasoning history stays intact.

---

## 9. The Resource Atlas

A separate document mapping your collected books, courses, and other materials to specific sessions.

### 9.1 Categories

For each resource, against each session it touches:

- **Must-read** — central to the session, do it
- **Should-read** — clarifies or deepens, recommended
- **Reference-only** — useful when stuck, not needed otherwise
- **Exercise-source** — drills and practice problems

### 9.2 Status tracking

- **U** = untouched
- **T** = TOC read only
- **P** = partially read / dipped into
- **R** = read in full
- **E** = enrolled / accessing (for courses)

### 9.3 How it gets used

Each session, when I deliver it, includes a short section titled **Curated reading**:

> **Curated reading:** *R for Data Science* Ch 5 (must-read), `BAIforYouth.csv` (exercise-source).

If a resource doesn't map to any session, it gets a **"parking lot"** entry — kept for awareness, not used right now.

---

## 10. Cross-course coordination

You have a **separate stats and meta-analysis course** in the same Project. The two courses are deliberately separate but aware of each other.

### 10.1 What "aware of each other" means

- I can search past chats from the stats course when relevant
- Where topics overlap (regression, simulation, meta-analysis methods), the R course shows the **R implementation**; the stats course shows the **theory**
- Both courses include "↔" callouts to the other when topics touch

### 10.2 You can ask me to bridge

Any time:
- *"What did we cover about X in the stats course?"*
- *"Connect this to the stats course."*
- *"Don't duplicate — focus on the R angle here."*

I'll search the parallel course and synthesise.

---

## 11. AI-assisted learning thread

Starting around Phase 1, every session includes a small box: **How I'd ask Claude this.** Shows a prompt I'd write if I were learning the session's topic myself.

The goal: by the end of the course, prompting Claude (and Copilot, Positron Assistant, etc.) for data work is second nature.

Phase 8 dedicates full sessions to AI-assisted workflow, prompting patterns, and staying current.

---

## 12. Staying current

Each session ends with a **stay-current corner** — one specific fresh thing (a blog, a package, a person to follow) in that area.

Phase 8 builds a personal "staying current" system end-to-end: R-Weekly, RSS feeds, Bluesky lists, conferences worth knowing, talks worth watching.

---

## 13. When things go wrong

### 13.1 You're stuck mid-exercise

Share verbatim code + verbatim error + what you expected. I'll diagnose.

### 13.2 You don't have time this week

Tell me. We pause. When you come back, just say "picking up at session X.Y" and I'll resume.

### 13.3 A session feels wrong

If a session feels too easy, too hard, too long, too short, off-topic, or just *off* — tell me. Often this is a signal we should log as a decision and adjust the COURSE-MAP.

### 13.4 You disagree with my recommendation

Push back. I'd rather be corrected than confidently wrong. Your "actually, we do need X" is one of the most valuable inputs in this whole process.

### 13.5 You're losing motivation

Tell me that too. We can shorten sessions, switch to a more applied phase early, or take a planned break. The course adapts to your life, not the reverse.

---

## 14. End-of-session checklist

At the end of every session, ideally:

- [ ] Session notes saved in the right phase folder
- [ ] Any new decisions added to DECISION-LOG
- [ ] Git commit with a meaningful message
- [ ] Pushed to GitHub (after Session 0.2)
- [ ] Reflection line added to COURSE-MAP (one sentence: what stuck, what didn't)

This takes about three minutes. Don't skip it; it's where the learning consolidates.

---

## 15. The handbook itself

This document is **living**. If our process changes, update it. If something here isn't working, change it.

Major changes to the handbook get logged in DECISION-LOG just like any other decision.

---

## 16. How-to recipes

Practical guides for recurring tasks. Each recipe follows the same format: the problem, brief alternatives, the chosen approach, and step-by-step instructions.

If you find yourself solving the same small problem twice, write a recipe for it.

---

### Recipe 1 — Taking notes in session files

**Problem**
You want to annotate session files with your own observations, questions, half-formed thoughts, things to look up later. Your existing instinct is the MS Word comment-pane model — side-pinned notes that live alongside the content.

**Alternatives considered**

| Option | Pros | Cons | Verdict |
|--------|------|------|---------|
| **A. Inline blockquotes** with a tag prefix (e.g. `> **My note:**`) | Lives right next to the content; zero setup; visible everywhere | Mixes with my text; file becomes co-authored | ✅ Chosen for general use |
| **B. Dedicated `## My notes` section at end of file** | Clean separation; easy to find all your notes | Not next to the thing they're about; lose context | ❌ Skipped — worst of both worlds |
| **C. Separate `session-NN-my-notes.md` file** | Total freedom; doesn't touch the lesson; easy to share with me | Two files per session; more switching | ⏸ Reserve for later if A overflows |

**Recommended approach: start with A, fall back to C if needed**

Use inline blockquotes with a consistent tag prefix so you can find all your notes via a search. The session template includes a `## My notes` section at the very bottom for longer reflections that don't belong inline.

**How to do it**

1. **For short inline annotations**, paste a blockquote where the thought happens:

   ```markdown
   The pipe operator `|>` was introduced in R 4.1...

   > **Note (Z):** Need to check which R version I have. Run `R.version.string`?

   The native pipe differs from magrittr's `%>%` in a few ways...
   ```

2. **Use a consistent tag prefix** — `**Note (Z):**` or `**Q:**` or just `📝`. This makes them findable. In VS Code, `Ctrl + Shift + F` searches across all files; in your repo, GitHub's search finds the same.

3. **For longer reflections**, use the `## My notes` section at the bottom of the session file:

   ```markdown
   ## My notes

   - *Confused by why `<-` vs `=`. Asked Claude, got answer: `<-` is R convention, `=` works but isn't idiomatic.*
   - *The `here()` function solves my Windows path pain. Loved this.*
   - *Need to revisit factors — felt rushed.*
   ```

4. **If your inline notes start crowding the file** (more than ~10 per session, or you want to write essays), graduate to Pattern C: create a sibling file `session-NN-my-notes.md` and move notes there. The lesson file stays clean.

**Bonus — side-by-side editing in VS Code**

Open the lesson file, then press `Ctrl + \` to split the editor. Drag your notes file (or the second copy of the lesson) to the right pane. This is the closest thing to a Word comment pane: two files side-by-side, both editable, both previewable.

---

### Recipe 2 — Reading markdown with an outline / TOC visible

**Problem**
Long markdown files (the operating documents in particular) need a clickable outline so you can jump around. You wanted a "sticky left panel" — like Word's Navigation pane.

**Alternatives considered**

| Option | Setup | Where outline appears | Verdict |
|--------|-------|-----------------------|---------|
| **A. VS Code built-in Outline (sidebar)** | None | Left sidebar (Explorer → Outline section) | ✅ Pre-GitHub default |
| **B. Markdown Preview Enhanced extension** | Install one extension | Inside the rendered preview pane (floating TOC) | ✅ If you want it *inside* preview |
| **C. GitHub web view** | Push to GitHub first | Right side of the rendered page (sticky) | ✅ Best after Session 0.2 |
| **D. In-file TOC at top** | Already there | Inside the file content | ✅ Universal fallback — works everywhere |

**Recommended approach: layer them**

- **Always available:** the in-file TOC at the top of every operating document (already done)
- **For everyday editing:** VS Code's sidebar Outline (no setup)
- **For sticky-panel reading:** GitHub once your repo is live (Session 0.2 onward)
- **Only if you really want TOC inside VS Code preview:** install Markdown Preview Enhanced

**How to do it**

**Option A — VS Code sidebar Outline (works now)**

1. Open any markdown file in VS Code
2. Open the Explorer sidebar (`Ctrl + Shift + E`)
3. Look for the **Outline** section at the bottom of the sidebar — it expands to show all headings in the current file
4. If you don't see it: right-click the Explorer header → tick *Outline*
5. Click any heading to jump to it

**To get edit + preview side-by-side with outline still visible:**

1. Open the markdown file
2. Press `Ctrl + K`, release, then press `V` — this opens preview to the right
3. The Outline in the sidebar still tracks your active file
4. You now have: sidebar (outline) | editor (left) | preview (right)

**Option B — Markdown Preview Enhanced (if you want TOC inside preview)**

1. In VS Code, click the Extensions icon in the left sidebar (or `Ctrl + Shift + X`)
2. Search for **Markdown Preview Enhanced** (by Yiyi Wang)
3. Click *Install*
4. Open a markdown file
5. `Ctrl + Shift + P` → type *"Markdown Preview Enhanced: Open Preview to the Side"* → enter
6. The preview now includes a floating TOC button (top-right of the preview pane)

**Option C — GitHub web view (after Session 0.2)**

1. Push your repo
2. Navigate to any `.md` file on github.com
3. The outline panel appears on the right side, automatically, with sticky scrolling

---

### Recipe 3 — Where to put files on Windows (and why not OneDrive)

**Problem**
You need a folder for your repository on Windows. Common defaults like Desktop or Documents are often *inside* OneDrive, which causes issues with Git.

**Alternatives considered**

| Location | Pros | Cons | Verdict |
|----------|------|------|---------|
| **`Documents\` inside OneDrive** (Windows default for many) | Auto-backup; sync across devices | OneDrive's sync conflicts with Git's; mysterious bugs, file lock errors | ❌ Avoid |
| **`C:\Users\<you>\Documents\` outside OneDrive** | No sync conflicts; standard location; not in OneDrive even if other folders are | Have to verify OneDrive isn't syncing this folder | ⚠️ Works if Documents isn't OneDrive-managed |
| **`C:\Users\<you>\projects\` or similar** (root of user folder) | Clearly outside OneDrive; clean home for code | Not a standard Windows folder | ✅ Recommended |
| **`C:\code\` or `D:\code\`** (drive root) | Short paths; clearly project space | Requires admin rights in some cases | ✅ Also good if you have a second drive |
| **Desktop** | Easy to find | Often OneDrive-synced; clutters visual workspace | ❌ Avoid |

**Recommended approach: a dedicated `projects/` folder in your user home**

Put your repo at `C:\Users\<YourName>\projects\r-data-science-journey\`. Create the `projects` folder if it doesn't exist. This becomes the home for all your code-based projects.

**How to do it**

1. **Check whether your Documents folder is OneDrive-synced:**
   - Open File Explorer
   - Click *This PC* → *Documents*
   - Look at the top of the window — does the address bar show `OneDrive` in the path? If yes, your Documents is inside OneDrive.

2. **Create a clean projects folder outside OneDrive:**
   - Open File Explorer
   - Navigate to `C:\Users\<YourName>\`
   - Right-click empty space → *New* → *Folder*
   - Name it `projects`
   - This folder is outside OneDrive (OneDrive only syncs specific folders, not the whole user directory)

3. **Move (or create) your repo folder inside it:**
   - Inside `projects`, create `r-data-science-journey`
   - Place your `README.md`, `COURSE-MAP.md`, `DECISION-LOG.md`, `LOGISTICS-HANDBOOK.md`, `RESOURCE-ATLAS.md` here
   - Subfolders for each phase as you go

4. **Verify the path:**
   - Open the folder
   - Right-click an empty area → *Open in Terminal* (or *Open Git Bash here* once Git is installed)
   - In the terminal, type `pwd` and press Enter
   - You should see something like `/c/Users/YourName/projects/r-data-science-journey` (no `OneDrive` anywhere)

**Why this matters**

OneDrive locks files briefly while syncing. Git also locks files briefly while committing. When they collide, you get errors like *"unable to write file"* or *"file is in use by another process"*. They're not catastrophic but they're recurring and confusing. Avoiding the overlap entirely is much cleaner than debugging it later.

---

### Recipe 4 — VS Code setup for this course

**Problem**
VS Code has thousands of extensions and dozens of settings. You need a minimal, intentional setup that suits markdown writing, GitHub workflow, and (later) R coding.

**Alternatives considered**

| Approach | Pros | Cons | Verdict |
|----------|------|------|---------|
| **Install everything that sounds relevant** | Comprehensive | Slow, cluttered, hard to debug when something breaks | ❌ Avoid |
| **Install only what's needed for the current phase** | Lean, fast | Have to revisit later for new tools | ✅ Chosen |
| **Use defaults, no extensions** | Zero setup | Misses 80% of VS Code's value for markdown/code | ❌ Suboptimal |

**Recommended approach: minimal install for now, add as needed**

Install only the extensions and tweaks you'll use immediately. Add more when a session demands them.

**How to do it**

**Step 1 — Sign in**

- Click the person icon in the bottom-left corner of VS Code
- Choose *"Sign in to Sync Settings"*
- Pick *"Sign in with GitHub"*
- Authorise in the browser when prompted

This signs you in to both Settings Sync and GitHub integration.

**Step 2 — Install the two essential extensions**

Click the Extensions icon in the left sidebar (or `Ctrl + Shift + X`). For each:

- **Markdown All in One** by *yzhang* (publisher: `yzhang`, identifier: `yzhang.markdown-all-in-one`) — keyboard shortcuts, auto-formatting, TOC generation
- **markdownlint** by *David Anson* — flags style issues as you type

Search by name, verify the publisher matches, click *Install*.

**Step 3 — Optional: install Markdown Preview Enhanced**

Only if you want a TOC visible inside the preview pane (see [Recipe 2](#recipe-2--reading-markdown-with-an-outline--toc-visible)).

**Step 4 — Apply these settings**

Open settings (`Ctrl + ,`), search for each setting, and change:

- `editor.wordWrap` → `on` (long lines wrap, no horizontal scroll)
- `files.autoSave` → `afterDelay` (auto-saves after a short pause)
- `editor.minimap.enabled` → `false` (optional — removes the tiny code preview on the right, more room for content)

**Step 5 — Keyboard shortcuts worth knowing**

| Shortcut | Effect |
|----------|--------|
| `Ctrl + Shift + V` | Open preview in same tab |
| `Ctrl + K, V` | Open preview to the side (release Ctrl+K, then press V) |
| `Ctrl + \` | Split editor (side-by-side files) |
| `Ctrl + Shift + E` | Toggle Explorer sidebar (with Outline at bottom) |
| `Ctrl + Shift + F` | Search across all open files / project |
| `Ctrl + P` | Quick-open any file by name |
| `Ctrl + ,` | Open settings |
| `Ctrl + Shift + P` | Command palette (find any VS Code command) |

These eight cover ~90% of your daily VS Code interactions.

**Step 6 — When you'll add more later**

- Phase 0.2 (Git): VS Code has built-in Git support, no extension needed
- Phase 1 onward (R): install the *R extension* by REditorSupport when we get there
- Phase 4 (Quarto): install the *Quarto* extension when we get there
- Phase 8 (AI): we'll discuss AI coding extensions then

---

### Recipe 5 — Capturing clarifications as we go

**Problem**
Throughout the course, you'll ask clarifying questions in chat — "what does X mean," "elaborate on Y," "explain Z in plain language." The answers are useful reference material, but if they only live in chat history they're hard to find again three weeks later. Some questions become reusable mini-explainers; others become recipes here in the handbook; others should just be captured tidily for future reference.

**Alternatives considered**

| Option | Pros | Cons | Verdict |
|--------|------|------|---------|
| **A. Leave them in chat history** | Zero overhead in the moment | Unsearchable, lost in noise; recovery painful 3 weeks later | ❌ Current default — failing |
| **B. Per-session "Clarifications" subsection** at the bottom of each session file | Lives with the session that prompted it; in context | Same clarification often applies across sessions; risks duplication; hard to search across sessions | ⚠️ Limited |
| **C. Standalone `clarifications.md`** at repo root, topic-organised | One searchable home; chronologically appendable; topic structure scales | Yet another file to maintain | ✅ Chosen |
| **D. Topic-specific cheatsheets in `cheatsheets/`** | Aligned with how you'll use them later (reference, not narrative) | Premature organisation; not yet clear which topics will accumulate | ⏸ Future state — when topics mature |

**Recommended approach: clarifications.md now, spin out cheatsheets later**

A single `clarifications.md` at the repo root is the holding place. Entries are organised by topic section. When a topic accumulates ~3-4 entries, we spin it out into a dedicated cheatsheet at `cheatsheets/<topic>.md` (e.g. `cheatsheets/git-essentials.md`).

**How to do it**

**Format of an entry:**

```markdown
### [Question phrased the way you'd search for it]

**Asked during:** Session X.Y
**Tags:** #topic1 #topic2

**Short answer**
[Gist in 1-2 sentences]

**Why it matters / longer explanation**
[Context when the short answer isn't enough]

**See also**
- [Pointers to related material]
```

**The workflow in practice:**

1. You ask a clarifying question in chat
2. Claude answers in chat as usual
3. If the clarification is worth keeping, Claude appends *"Draft entry for clarifications.md:"* followed by a formatted entry
4. You copy the entry, paste it into `clarifications.md` under the right topic section (or create a new section)
5. Commit when convenient

**What's worth capturing**
- Concept clarifications ("what does X mean")
- Conventions ("which version / which option / why this one")
- Mental-model corrections ("I thought it worked like A, but it's actually B")
- Useful analogies that clicked for you

**What's not worth capturing**
- One-off "where did I put this file" questions
- Quick syntax lookups (those go in cheatsheets or are handled by `?function` in R)
- Personal-progress check-ins

**When to spin out a cheatsheet**

Watch the topic sections in `clarifications.md`. When one accumulates ~3-4 entries:

1. Create `cheatsheets/<topic>.md`
2. Move the entries from `clarifications.md` into the new cheatsheet
3. Reorganise into a reference structure (cheatsheets are looked up, not read linearly)
4. Leave a stub in `clarifications.md` pointing to the cheatsheet

**Why this works**
The entries are short. Searching one file is fast (`Ctrl + F`). Tags make filtering possible. Spinning out only when needed avoids premature organisation. And the *whole system* is just two files (`clarifications.md` + maybe a few cheatsheets later) — small enough that you'll actually maintain it.

---

*End of handbook.*
