# Session 0.1 — Setting the Stage: Install & Configure

**Phase:** 0 — Setting the Stage
**Estimated time:** 45 minutes
**Format:** Concept → commented walkthrough → your turn
**Prerequisites:** A Windows 11 machine, admin rights to install software, internet

---

## Table of Contents

- [Session 0.1 — Setting the Stage: Install \& Configure](#session-01--setting-the-stage-install--configure)
  - [Table of Contents](#table-of-contents)
  - [Session checklist](#session-checklist)
  - [Why this matters](#why-this-matters)
  - [Curated reading](#curated-reading)
  - [Mini-theory: what are we actually installing?](#mini-theory-what-are-we-actually-installing)
  - [Walkthrough](#walkthrough)
    - [Step 1 — Install R](#step-1--install-r)
    - [Step 2 — Install RStudio Desktop](#step-2--install-rstudio-desktop)
    - [Step 3 — Install Rtools](#step-3--install-rtools)
    - [Step 4 — Install Git](#step-4--install-git)
    - [Step 5 — Tell Git who you are](#step-5--tell-git-who-you-are)
    - [Step 6 — Create a GitHub account](#step-6--create-a-github-account)
  - [Your turn — small checks](#your-turn--small-checks)
    - [Check 1 — R speaks](#check-1--r-speaks)
    - [Check 2 — RStudio knows where R is](#check-2--rstudio-knows-where-r-is)
    - [Check 3 — Rtools is reachable](#check-3--rtools-is-reachable)
  - [Going deeper *(optional rabbit holes)*](#going-deeper-optional-rabbit-holes)
  - [Stay-current corner](#stay-current-corner)
  - [Commit message suggestion](#commit-message-suggestion)
  - [Cross-references](#cross-references)
  - [How I'd ask Claude this *(meta-skill preview — full version starts Phase 1)*](#how-id-ask-claude-this-meta-skill-preview--full-version-starts-phase-1)
  - [My notes](#my-notes)

---

## Session checklist

**Pre-session**
- [x] Skim the [*Happy Git with R*](https://happygitwithr.com) installation chapters (4-7) — 5 min skim, not detailed read
- [x] Confirm you have admin rights on your Windows machine
- [x] Decide where your repo will live (see Recipe 3 in LOGISTICS-HANDBOOK if undecided)

**During session**
- [x] Step 1 — Install R from CRAN
- [x] Step 2 — Install RStudio Desktop
- [x] Step 3 — Install Rtools
- [x] Step 4 — Install Git for Windows
- [x] Step 5 — Configure Git with your name and email
- [x] Step 6 — Create a GitHub account (if you don't have one)
- [x] Run the three small verification checks in RStudio

**Post-session**
- [x] Save this notes file at `00-setting-the-stage/session-01-install/session-01-notes.md`
- [x] Add reflection line to COURSE-MAP (under Reflections)
- [x] *(No Git commit yet — we set up the repo in Session 0.2)*

---

## Why this matters

Most R tutorials start with `library(tidyverse)` and skip the foundational decisions: *what are you actually installing, why these tools, and what alternatives exist?* That's the gap I want to close before we write a single line of code.

You'll come out of this session with:

- A working R + RStudio install
- Git installed and identified as you
- A GitHub account ready to receive your first repo (in Session 0.2)
- A clear mental model of how these pieces talk to each other

---

## Curated reading

> - **Should-read:** [*Happy Git with R*](https://happygitwithr.com) — Bryan, chapters 4-7 `[ONLINE]`
> - **Reference-only:** MATI: *Notes - AI in Meta-Analysis.docx* `[DOCX]` (not for this session, just so you know it's there)

---

## Mini-theory: what are we actually installing?

Think of your R setup as a **three-layer cake**, plus a **delivery van**.

**Layer 1 — R itself (the engine).**
R is a programming language and a computing environment. When you install R, you're installing an interpreter that reads R code and runs it. By itself, R has a primitive interface — a console window. Few people use it that way.

**Layer 2 — RStudio (the dashboard).**
RStudio is an **IDE** (Integrated Development Environment): a comfortable cockpit around R. It gives you a code editor, a console, a plot pane, a file browser, a help pane, and a hundred other niceties. *RStudio is not R.* You can have RStudio without R (it won't work), and R without RStudio (it works, but austerely). The relationship is like a car engine (R) and a car dashboard with seats (RStudio).

> **Worth knowing — alternatives:**
> - **Positron** is a brand-new IDE from Posit (the company that makes RStudio). It's based on VS Code and supports R *and* Python natively. We'll touch it in Phase 8. For now: RStudio is the safer, more mature choice.
> - **VS Code with the R extension** is popular if you already live in VS Code.
> - **Jupyter** can run R kernels, but it's not the typical R workflow.

**Layer 3 — Rtools (the workshop).**
Some R packages contain code in C or C++ that needs to be **compiled** on your machine. On macOS and Linux, the system has compilers built in. On **Windows**, you have to install them separately, and Posit packages them up as **Rtools**. Without Rtools, some package installs will mysteriously fail. So we install it pre-emptively.

**The delivery van — Git + GitHub.**

- **Git** is version-control software that lives on your computer. It tracks every change you make to your code and lets you rewind, branch, and merge.
- **GitHub** is a website that hosts Git repositories online so others (and future-you) can see and collaborate on your code.

Git and GitHub are **not the same thing**. Git is the tool; GitHub is one (popular) hosting service. Alternatives: GitLab, Bitbucket, Codeberg. We'll use GitHub because it's the default and it integrates with everything.

> **A note on order.** We install all four pieces before doing anything with them. Installation is boring but worth a careful 30 minutes. Reinstalling later because something was missed costs more time than getting it right now.

---

## Walkthrough

### Step 1 — Install R

1. Go to **https://cran.r-project.org**
2. Click *Download R for Windows*
3. Click *base* → *Download R-X.X.X for Windows* (where X.X.X is the current version)
4. Run the installer. Accept all defaults.

> 💡 **CRAN** stands for the *Comprehensive R Archive Network*. It's the official source for R and most R packages. You'll see "CRAN" mentioned a lot.

To verify: open the Start menu, type `R x64`, click it. A primitive console window opens with text like `R version 4.x.x ...`. Close it. We won't use this directly again.

### Step 2 — Install RStudio Desktop

1. Go to **https://posit.co/download/rstudio-desktop/**
2. The page detects your OS — click the download for **Windows**
3. Run the installer. Defaults are fine.

To verify: open the Start menu, type `RStudio`, launch it. You'll see a four-pane interface. RStudio finds R automatically; if it asks, point it to your R installation.

### Step 3 — Install Rtools

1. Go to **https://cran.r-project.org/bin/windows/Rtools/**
2. Click the version matching your R (e.g. *Rtools45* if you installed R 4.5.x)
3. Download the **installer** (the file ending `.exe`)
4. Run it, accept defaults

You won't interact with Rtools directly — R uses it behind the scenes when it needs to compile packages.

### Step 4 — Install Git

1. Go to **https://git-scm.com/download/win**
2. The download starts automatically
3. Run the installer
4. On the many config screens, accept defaults *except* for:
   - **Default editor**: choose **"Use Visual Studio Code as Git's default editor"** if you have VS Code, otherwise **"Use the Nano editor by default"** (avoid Vim unless you know it)
   - **Adjusting line endings**: choose **"Checkout Windows-style, commit Unix-style"** (the recommended option). This avoids a classic Windows headache.

To verify: open **Git Bash** from the Start menu (it gets installed with Git). Type:

```bash
git --version
```

You should see something like `git version 2.45.x`.

### Step 5 — Tell Git who you are

In the Git Bash window, run these two commands (replace with your real info):

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Use the **same email** you'll use for GitHub. This is how commits get attributed to you.

> 💡 **Why `--global`?** It sets these for *all* repos on your machine, not just one. You can override per-repo later if needed.

### Step 6 — Create a GitHub account

1. Go to **https://github.com**
2. Sign up with the **same email** you used above
3. Pick a username you wouldn't mind being public — this is your professional handle
4. Verify your email

We won't connect GitHub to your machine yet — that's Session 0.2.

---

## Your turn — small checks

Three tiny checks to confirm everything's working. Open **RStudio** for these.

### Check 1 — R speaks

In the Console pane (bottom-left), type:

```r
2 + 2
```

You should see `[1] 4`. If yes, R works.

### Check 2 — RStudio knows where R is

In the Console:

```r
R.version.string
```

You should see something like `"R version 4.5.0 (2025-04-11)"`. (Your version may be slightly different — that's fine.)

### Check 3 — Rtools is reachable

In the Console:

```r
Sys.which("make")
```

You should see a path containing `rtools`, e.g. `"C:\\rtools45\\usr\\bin\\make.exe"`. If you see an empty string `""`, Rtools is installed but R can't find it — *don't worry about this right now*, we'll handle it if it bites us later.

> my_note: all three tests returned correct results.
---

## Going deeper *(optional rabbit holes)*

- **R's history**: R is an open-source descendant of S, a language designed at Bell Labs in the 1970s for statistical computing. The name "R" is partly a nod to S, partly a reference to the first names of its creators, Ross Ihaka and Robert Gentleman. This heritage is why R feels *statistical* in places that other languages don't.
- **Posit vs RStudio (the company name change)**: In 2022, RStudio the company rebranded to *Posit*. The IDE is still called RStudio. So *Posit makes RStudio* — and now also Quarto, Positron, the `tidymodels` ecosystem, and a lot more. Knowing this saves confusion when you see both names.

---

## Stay-current corner

This session's "one thing": follow **R-Weekly** at **https://rweekly.org**. It's a curated weekly newsletter of new R packages, blog posts, and tutorials. Reading 5 minutes of R-Weekly each week is, alone, an excellent FOMO antidote. Bookmark it; we'll add an RSS-feed habit later.

---

## Commit message suggestion

We don't have a repo yet — that's Session 0.2. But for your local note-taking, save the markdown notes from this session as:

```
00-setting-the-stage/session-01-install/session-01-notes.md
```

In Session 0.2, your first commit message will be something like:

```
Initial commit: setup notes for sessions 0.1 and 0.2
```

---

## Cross-references

- **Next:** Session 0.2 — Project structure, the `here` package, your first repo & commit
- **Stats course parallel:** none yet — these toolchain sessions are R-course specific
- **Logistics:** Recipes 3 (Windows folders) and 4 (VS Code setup) are relevant background

---

## How I'd ask Claude this *(meta-skill preview — full version starts Phase 1)*

If you got stuck on any step, a useful prompt pattern is:

> "I'm on Windows 11. I just ran `[exact command]` in `[where]` and got `[exact output / error]`. What does this mean and how do I fix it?"

Giving the **exact command** and the **exact output** (copy-paste, not paraphrased) makes Claude's answer 10× more useful. We'll formalise this pattern in Phase 8.

---

## My notes

*Your space. Annotate freely. See Recipe 1 in LOGISTICS-HANDBOOK for note-taking patterns.*

<!-- Example format:
- *(2026-05-22)* Surprised by how many windows RStudio has on first launch.
- *(2026-05-22)* Rtools install was slower than expected.
- **Q:** Why does R use `<-` instead of `=`?
-->

---

*End of Session 0.1. Reflect briefly: what surprised you? What felt obvious that you didn't expect to be obvious? Note it in your COURSE-MAP reflections section.*
