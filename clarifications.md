# Clarifications

*Short, focused answers to questions that came up while learning. Searchable reference, organised by topic.*

> Living document. Entries are appended chronologically within each topic section.
> When a topic accumulates ~3-4 entries, we may spin it out into a dedicated cheatsheet at `cheatsheets/<topic>.md`.
> *For navigation: GitHub renders a sticky outline panel on the right; in VS Code use the Outline view in the Explorer sidebar; in any viewer, the TOC below is clickable.*

---

## Table of Contents

- [How to use this file](#how-to-use-this-file)
- [R installation and toolchain](#r-installation-and-toolchain)
  - [What does "compiling C/C++ in R packages" mean?](#what-does-compiling-cc-in-r-packages-mean)
- [Git and version control](#git-and-version-control)
  - [What is "staging" in Git, and why does it exist?](#what-is-staging-in-git-and-why-does-it-exist)
- [Editor setup (VS Code)](#editor-setup-vs-code)
  - [Which "Markdown All in One" extension should I install?](#which-markdown-all-in-one-extension-should-i-install)
  - [Should I sign in to VS Code? GitHub or Microsoft account?](#should-i-sign-in-to-vs-code-github-or-microsoft-account)

---

## How to use this file

Each entry has:

- **Question** — phrased the way you (or future-you) would search for it
- **Asked during** — which session prompted it
- **Tags** — keywords for searching
- **Short answer** — the gist in a sentence or two
- **Why it matters / longer explanation** — context for when the short answer isn't enough
- **See also** — pointers to related material in other documents

To search this file: `Ctrl + F` in any markdown viewer. Tags use `#` prefixes for easy filtering.

To add a new clarification: Claude will draft an entry in chat with the heading *"Draft entry for clarifications.md"*. Copy it, paste it under the right topic section (or create a new section if needed), commit.

---

## R installation and toolchain

### What does "compiling C/C++ in R packages" mean?

**Asked during:** Session 0.1
**Tags:** `#installation` `#r-internals` `#windows` `#rtools`

**Short answer**
Some R packages contain code written in C or C++ that needs to be translated into machine instructions your computer can run. That translation is called *compiling*. On macOS and Linux, the compilers come built-in. On Windows, you install them separately as Rtools.

**Why it matters**
R is an interpreted language — your code runs as you write it. But for heavy number-crunching, R is slow. Package authors get around this by writing the fast parts in C or C++ and bundling them inside the R package. When you install such a package, R needs to translate that C/C++ code for your specific machine, and that's the compile step.

Without Rtools, package installs that need compilation fail with confusing errors like *"installation of package 'xyz' had non-zero exit status"*. Pre-installing Rtools avoids the whole class of issues.

**Analogy that helps**
If R code is a recipe written in English, your computer can follow it as written. C code is a recipe in a foreign language — it has to be translated into English first. Compiling is that translation step. Rtools is the translator.

**See also**
- Session 0.1 walkthrough Step 3 (installing Rtools)
- LOGISTICS-HANDBOOK section 4.1 (toolchain explanations)

---

## Git and version control

### What is "staging" in Git, and why does it exist?

**Asked during:** Session 0.2
**Tags:** `#git` `#commits` `#workflow`

**Short answer**
Staging is telling Git *"these specific changes belong in my next commit"*. It exists so you can craft intentional commits with clear stories instead of dumping all changes into one. In RStudio, staging = ticking the checkbox next to a file in the Git pane.

**Why it matters**
Git has three "places" a file can live in:

1. **Working directory** — your folder on disk, where you edit
2. **Staging area** — a holding pen for changes ready to commit
3. **Repository** — the permanent committed history (the `.git` folder)

A change moves through these in order: edit → stage → commit. The staging area is what lets you commit *only some* of your current changes, leaving others for later or different commits.

**Concrete scenario**
Imagine you've fixed a bug, added experimental code you're unsure about, and updated a doc — all in one work session. Without staging, you'd have to commit them all together. With staging, you stage just the bug fix and commit it ("Fix typo in analysis"), then stage the doc update separately ("Add Session 1.1 reflection"), and leave the experimental code unstaged for later.

**Mechanics in RStudio**

| What you see | What it means |
|--------------|--------------|
| Yellow `?` | Untracked file Git noticed but isn't following yet |
| Blue `M` | Modified — file changed since last commit |
| Green `A` | Staged for next commit |
| (blank) | Tracked and unchanged since last commit |

Ticking the checkbox stages a file. Clicking Commit captures everything staged.

**Common confusion**
Saving a file ≠ staging it. Save updates the file on disk; staging is a separate explicit step you take in Git afterwards.

**Advanced (for later)**
You can stage *part* of a file — only some of the changed lines (called "hunks"). RStudio's commit dialog shows *Stage chunk* buttons for each block of changes. Useful when you've made unrelated changes in the same file. Not needed yet.

**See also**
- Session 0.2 walkthrough Part 6 (first commit)
- *Happy Git with R* — Bryan, chapter "Repositories"

---

## Editor setup (VS Code)

### Which "Markdown All in One" extension should I install?

**Asked during:** Session 0.1 (pre-install)
**Tags:** `#vscode` `#extensions` `#markdown`

**Short answer**
The one by **Yu Zhang**, publisher `yzhang`, identifier `yzhang.markdown-all-in-one`. Has several million downloads. Other extensions with similar names are forks or unrelated.

**How to verify before installing**
Click on the extension's detail page in VS Code's Extensions panel. The right one shows:
- Publisher: `yzhang`
- Description starts with: *"All you need for Markdown (keyboard shortcuts, table of contents, auto preview and more)."*

**See also**
- LOGISTICS-HANDBOOK Recipe 4 (VS Code setup) for the full configuration

---

### Should I sign in to VS Code? GitHub or Microsoft account?

**Asked during:** Session 0.1 (pre-install)
**Tags:** `#vscode` `#github` `#authentication`

**Short answer**
Yes, sign in. Use your **GitHub account** rather than a Microsoft account. Removes friction for the rest of the course, since everything builds on GitHub integration.

**Why GitHub over Microsoft**

| Feature | GitHub account | Microsoft account |
|---------|----------------|-------------------|
| Settings sync across machines | ✅ Works | ✅ Works |
| GitHub repo integration | ✅ Native, frictionless | ⚠️ Possible but indirect |
| Push to GitHub without password prompts | ✅ Just works | ⚠️ Extra setup needed |
| You already have it | ✅ (created in Session 0.1) | Maybe |

**Privacy considerations**
When signed in, VS Code can sync your settings and extensions to Microsoft servers (Microsoft owns GitHub). Avoid putting secrets (API keys, tokens) in `settings.json` regardless — we'll cover proper secrets management in Phase 7.

**See also**
- LOGISTICS-HANDBOOK Recipe 4 Step 1
- Session 0.2 (which uses GitHub authentication for pushing)

---

*End of clarifications. Updated by appending; entries are never deleted.*
