# Session 0.2 — Your First R Project, the `here` Package, and Your First Commit

**Phase:** 0 — Setting the Stage
**Estimated time:** 60 minutes (could go to 90 if you've never used Git before — give it the time)
**Format:** Concept → commented walkthrough → your turn
**Prerequisites:** Session 0.1 complete — R, RStudio, Rtools, Git, and a GitHub account all set up

---

## Table of Contents

- [Session 0.2 — Your First R Project, the `here` Package, and Your First Commit](#session-02--your-first-r-project-the-here-package-and-your-first-commit)
  - [Table of Contents](#table-of-contents)
  - [Session checklist](#session-checklist)
  - [Why this matters](#why-this-matters)
  - [Curated reading](#curated-reading)
  - [Mini-theory 1: What is an R Project?](#mini-theory-1-what-is-an-r-project)
  - [Mini-theory 2: What is `here` and why do you need it?](#mini-theory-2-what-is-here-and-why-do-you-need-it)
  - [Mini-theory 3: How Git, GitHub, and RStudio talk to each other](#mini-theory-3-how-git-github-and-rstudio-talk-to-each-other)
  - [Walkthrough](#walkthrough)
    - [Part 1 — Create an R Project](#part-1--create-an-r-project)
    - [Part 2 — Install and test the `here` package](#part-2--install-and-test-the-here-package)
    - [Part 3 — A first look at the Git pane](#part-3--a-first-look-at-the-git-pane)
    - [Part 4 — Create the matching GitHub repository](#part-4--create-the-matching-github-repository)
    - [Part 5 — Connect local repo to GitHub](#part-5--connect-local-repo-to-github)
    - [Part 6 — Make your first commit](#part-6--make-your-first-commit)
    - [Part 7 — Push to GitHub](#part-7--push-to-github)
  - [Your turn — small checks](#your-turn--small-checks)
    - [Check 1 — `here()` does what you expect](#check-1--here-does-what-you-expect)
    - [Check 2 — Make a tiny change and commit it](#check-2--make-a-tiny-change-and-commit-it)
    - [Check 3 — Find your repo URL](#check-3--find-your-repo-url)
    - [Check 4 — Confirm `.gitignore` exists and is doing something useful](#check-4--confirm-gitignore-exists-and-is-doing-something-useful)
  - [Going deeper *(optional rabbit holes)*](#going-deeper-optional-rabbit-holes)
  - [Stay-current corner](#stay-current-corner)
  - [Commit message suggestion](#commit-message-suggestion)
  - [Cross-references](#cross-references)
  - [How I'd ask Claude this *(meta-skill preview)*](#how-id-ask-claude-this-meta-skill-preview)
  - [My notes](#my-notes)

---

## Session checklist

**Pre-session**
- [x] Confirm Session 0.1 fully complete (R, RStudio, Rtools, Git, GitHub account)
- [x] Decide where your repo folder will live on disk (see Recipe 3 in LOGISTICS-HANDBOOK if undecided)
- [x] Have your four operating documents downloaded and ready: COURSE-MAP, DECISION-LOG, LOGISTICS-HANDBOOK, RESOURCE-ATLAS, README

**During session**
- [x] Part 1 — Create an R Project for `r-data-science-journey`
- [x] Part 2 — Install and test the `here` package
- [x] Part 3 — Initialise Git in the project (RStudio's New Project dialog can do this)
- [x] Part 4 — Create a matching empty repo on GitHub
- [x] Part 5 — Connect local repo to GitHub
- [x] Part 6 — Make your first commit
- [x] Part 7 — Push to GitHub and verify

**Post-session**
- [x] Bookmark your repo URL — you'll share this with me from Session 1.1 onward
- [x] Save these notes at `00-setting-the-stage/session-02-project-and-git/session-02-notes.md`
- [x] Add reflection line to COURSE-MAP under Reflections
- [x] Tick Session 0.2 done in COURSE-MAP

---

## Why this matters

Three small concepts in this session compound into something large. After today:

- You'll write R code that runs on any machine because you never hard-code file paths again
- You'll have a workflow that auto-saves a permanent history of every change you make
- You'll have a public-facing portfolio of your learning that grows session by session
- I'll be able to fetch your files directly when you give me a URL — no more uploading

For evidence synthesis specifically: living systematic reviews demand reproducibility on a scale that overwhelms any non-versioned workflow. The habits you build today are not abstract good practice — they're how your team will eventually trust your living-review outputs.

---

## Curated reading

> - **Must-read** (alongside / right after this session): [*Happy Git with R*](https://happygitwithr.com) — Bryan, chapters 9-15 `[ONLINE]`. Especially "Connect to GitHub" and "Clone the test GitHub repository to your computer."
> - **Reference-only:** [*R for Data Science (2e)* — Ch 8: Workflow: scripts and projects](https://r4ds.hadley.nz/workflow-scripts) `[ONLINE]`

Bryan's book is the gold standard for everything in Part 3 onwards of this session. If anything I describe feels too thin, her chapters fill in the detail.

---

## Mini-theory 1: What is an R Project?

An **R Project** is RStudio's name for a folder that knows it is the home of a piece of work. Mechanically, it's just a folder with a small file inside it called `<name>.Rproj`. That file tells RStudio: "when you open me, set this folder as the working directory, remember the open scripts, remember the state of the environment."

That sounds trivial. Three things make it transformative.

**1. The working directory problem.**

When you run R code, R has a notion of "where am I right now?" — the **working directory**. By default, when you open RStudio fresh, the working directory is somewhere you didn't choose (often your user home folder). So when you write `read.csv("data.csv")`, R looks for `data.csv` *there*, not where your actual data is.

Newcomers solve this by writing things like `read.csv("C:/Users/Zinnat/Documents/projects/some-thing/data/data.csv")`. This works on their machine and breaks the moment anyone else (or future-you on a different laptop) tries to run it.

R Projects solve this by **automatically setting the working directory to the project folder when you open the project.** So if you're inside `r-data-science-journey.Rproj`, then `read.csv("data/study-counts.csv")` always works, no matter where on disk the folder is.

**2. The "many things at once" problem.**

You'll often have multiple pieces of work in flight. R Projects isolate each one. You can have your R course project open in one RStudio window, your stats course project open in another, your real evidence synthesis project open in a third. Each has its own working directory, its own command history, its own environment. They don't trample each other.

**3. The "where did I leave off?" problem.**

When you close and reopen an R Project, RStudio remembers what scripts you had open, where the cursor was, what was in the console. You pick up exactly where you stopped.

> 💡 **The rule of thumb you'll hear in the R community:** *if you're writing R code, you should be in an R Project. Every time.* Treating "no project" as the default is a sign of someone who hasn't learned this yet.

---

## Mini-theory 2: What is `here` and why do you need it?

R Projects fix the working directory problem at the *project root* level. But what happens when your script is deep in a subfolder?

Say your project looks like:

```
r-data-science-journey/
├── 01-r-fluency/
│   └── session-04-mini-project/
│       └── analysis.R     ← you're writing code here
└── datasets/
    └── study-counts.csv
```

Inside `analysis.R`, you want to read the CSV. Naively you'd write:

```r
read.csv("../../datasets/study-counts.csv")   # ".." means "go up one folder"
```

This works! But:

- It's ugly
- It breaks if you move the script
- It uses `/` separators (fine on Mac/Linux, fine in R, but Windows file dialogs show `\` — confusing)
- It's brittle to refactoring

**The `here` package solves this elegantly.** It looks for your project root (the folder with the `.Rproj` file) and builds paths from there:

```r
library(here)
read.csv(here("datasets", "study-counts.csv"))
```

`here("datasets", "study-counts.csv")` resolves to the full path from your project root, regardless of where the script lives. Move the script anywhere in the project — the code still works.

> 💡 The `here` package is what makes the *promise* of R Projects (machine-portable code) actually true in practice.

Tiny package, deep impact. We install it today and you'll use it forever.

---

## Mini-theory 3: How Git, GitHub, and RStudio talk to each other

Three tools, three roles. Easier to keep straight if you have an analogy.

- **Git** = the recording system in a TV studio. It captures everything that happens locally on your machine. Every "take" is a *commit*. You can rewind, branch, or replay.
- **GitHub** = a public broadcast channel. Once you've recorded something with Git, you can *push* it to GitHub for anyone to watch. Or pull from GitHub onto another machine.
- **RStudio** = the control room. It has buttons that trigger Git's recording and GitHub's broadcasting without you having to know all the command-line incantations.

You can do everything in this session via the command line (Git Bash). But RStudio's Git pane makes it visual and forgiving. We'll use RStudio for the common operations and command line only when needed.

**The core Git vocabulary** — five words you'll use forever:

| Word | What it means |
|------|--------------|
| **Repository (repo)** | A folder under Git's tracking, with history |
| **Commit** | A saved snapshot of all your tracked files at a moment in time, with a message |
| **Stage** | "Get this file ready to be included in the next commit" |
| **Push** | Send your local commits up to GitHub |
| **Pull** | Bring down GitHub commits to your local machine |

> 💡 **A common confusion:** a commit lives *only on your local machine* until you push it. GitHub doesn't know about your commits until you push. Commits are not auto-synced.

---

## Walkthrough

### Part 1 — Create an R Project

We'll create the R Project *and* initialise Git in the same step, because RStudio offers this in one dialog.

1. Open RStudio
2. Top-right corner, click the project dropdown (shows "Project: (None)" right now) → *New Project...*
3. Choose **Existing Directory** *(if you already have the folder with your operating documents)* or **New Directory** *(if you want RStudio to create it)*
   - **If you already created the folder** (e.g. `C:\Users\<you>\projects\r-data-science-journey\`) and dropped the markdown files in: choose *Existing Directory* and browse to it
   - **If you haven't created it yet**: choose *New Directory* → *New Project* → name it `r-data-science-journey` and pick the parent location (e.g. `C:\Users\<you>\projects\`)
4. On the project options screen, **tick "Create a git repository"** ← *important; this is the Git init step*
5. Click *Create Project*

RStudio reopens with the new project loaded. You'll see:

- A new file `r-data-science-journey.Rproj` in your folder
- A `.gitignore` file (Git's "ignore these files" list — we'll touch it later)
- The top-right corner now shows the project name
- A new **Git pane** in the top-right (Environment / History / Git / Connections tabs)

> 💡 If you chose *New Directory*, **stop here and move your operating documents into the folder now**: COURSE-MAP.md, DECISION-LOG.md, LOGISTICS-HANDBOOK.md, RESOURCE-ATLAS.md, README.md, and the `00-setting-the-stage/` folder with your session notes.

### Part 2 — Install and test the `here` package

In the RStudio Console (bottom-left), type:

```r
install.packages("here")
```

Press Enter. R downloads and installs the package. Should take 5-15 seconds. You'll see output ending in `* DONE (here)`.

Now load and test it:

```r
library(here)
here()
```

The second command should print the full path to your project folder, something like:

```
[1] "C:/Users/<you>/projects/r-data-science-journey"
```

When the package loads, it prints a message like `here() starts at C:/Users/...`. That's normal — it's telling you which folder it identified as the project root.

> 💡 **What just happened.** `here()` looked at your current location, walked up the folder tree until it found the `.Rproj` file, and reported that location as the project root. Every future call to `here("subfolder", "file.csv")` will build a path starting from there.

### Part 3 — A first look at the Git pane

Click the **Git** tab in the top-right pane.

You should see a list of files with **yellow `?` icons** next to them. The `?` means *"Git sees these files but isn't tracking them yet."*

This is normal! In Git, files are not auto-tracked just because they're in the folder. You explicitly tell Git which files matter (via the *stage* step), and only staged files get included in commits.

Files you'll likely see listed:

- `.gitignore`
- `r-data-science-journey.Rproj`
- `COURSE-MAP.md`
- `DECISION-LOG.md`
- `LOGISTICS-HANDBOOK.md`
- `README.md`
- `RESOURCE-ATLAS.md`
- `00-setting-the-stage/` (folder)

### Part 4 — Create the matching GitHub repository

Now we make an empty home on GitHub for these files to be pushed to.

1. Open your browser and go to **https://github.com**
2. Sign in if you're not already
3. Top-right, click the **`+`** icon → *New repository*
4. Fill in:
   - **Repository name:** `r-data-science-journey` *(use the exact same name as your local folder — saves confusion)*
   - **Description:** (optional, e.g. "My R, data science, and evidence synthesis learning journey")
   - **Public or Private:** *Public* is fine and lets the world see your portfolio. *Private* if you'd rather keep it to yourself for now (you can always make it public later).
   - **Initialize this repository:** ⚠️ *leave ALL three boxes UNCHECKED* (no README, no .gitignore, no licence). Your local folder already has these — adding them here would create a conflict.
5. Click *Create repository*

GitHub shows you a setup page with several command options. The one you want is under **"...or push an existing repository from the command line"**. Copy those commands aside — we'll use them in the next step.

### Part 5 — Connect local repo to GitHub

GitHub's setup page shows three commands. They look like this (yours will have your actual username):

```bash
git remote add origin https://github.com/<your-username>/r-data-science-journey.git
git branch -M main
git push -u origin main
```

We'll run the **first two** now and the third in Part 7 (after we've made a commit, since you can't push an empty repo).

In RStudio, go to *Tools* → *Terminal* → *New Terminal*. A terminal pane opens at the bottom. It opens in your project folder automatically.

> 💡 **Note for Windows:** RStudio's built-in terminal uses Git Bash on Windows by default, which is what we want. Confirm the prompt looks like `MINGW64` or has `~/projects/r-data-science-journey$` style — that's Git Bash. If it looks like PowerShell, that's also fine for these commands.

Paste in the first command (replace `<your-username>`):

```bash
git remote add origin https://github.com/<your-username>/r-data-science-journey.git
```

Press Enter. No output means success.

Then the second:

```bash
git branch -M main
```

This ensures your branch is called `main` (the modern default; GitHub stopped using `master` as the default years ago). No output = success.

> 💡 **What `origin` is.** `origin` is just a *nickname* Git uses for "the remote location I'm syncing with." You could call it anything (`github`, `cloud`, etc.) but `origin` is the convention.

### Part 6 — Make your first commit

Switch back to the Git pane in RStudio (top-right).

**Step 6a — Stage everything**

The files with yellow `?` need to be staged. Click the *checkbox* next to each file (or use the master checkbox to select all). The `?` icons become green `A` icons — *"Added, ready to commit."*

**Step 6b — Open the commit dialog**

Click the **Commit** button at the top of the Git pane. A new window opens showing:

- Top-left: list of staged files
- Top-right: a *Commit message* box
- Bottom: a *diff view* showing exactly what changed

**Step 6c — Write a commit message**

In the message box, type:

```
Initial commit: course-spine documents and Session 0.1 notes
```

Good commit messages start with a verb in imperative mood ("Add", "Fix", "Update", "Initial commit"), are short (50 chars or less for the first line ideally), and describe *what* changed. We'll develop this habit through the course.

**Step 6d — Click Commit**

Click the *Commit* button. RStudio shows the commit output and returns you to the Git pane. The yellow `?` icons are gone — your commit is captured locally.

Run this in the terminal to see what just happened:

```bash
git log --oneline
```

You'll see one line — your first commit, with a short hash and the message.

> 🎉 You just did something real. That snapshot is now permanent (unless you go out of your way to delete it). You could mess up every file in this folder, and rolling back to this state is one command away.

### Part 7 — Push to GitHub

Time for the final command from Part 5:

```bash
git push -u origin main
```

A browser window may pop up asking you to authorise — GitHub uses **personal access tokens** rather than passwords. If you signed VS Code into GitHub already (handbook Recipe 4), the credentials may flow automatically. If not, follow the prompts to authenticate. (Bryan's *Happy Git with R* chapter on credentials walks through this if you get stuck.)

After authentication, you'll see output like:

```
Enumerating objects: ...
Counting objects: ...
Writing objects: ...
To https://github.com/<your-username>/r-data-science-journey.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

**Refresh your GitHub repo page in the browser** — you should now see all your files there. README displays at the bottom of the file list as a rendered page.

🎉 **Your work is live.**

The `-u` flag in `git push -u origin main` set up tracking — from now on, you can just type `git push` (no flags) and it knows where to send things.

---

## Your turn — small checks

Four small things to confirm everything's connected.

### Check 1 — `here()` does what you expect

In the RStudio Console:

```r
library(here)
here("COURSE-MAP.md")
```

Should print the full path to your COURSE-MAP file. Try it with a non-existent file too:

```r
here("foo", "bar", "baz.csv")
```

It builds the path even though the file doesn't exist — useful for *constructing* paths to files you're about to write.

### Check 2 — Make a tiny change and commit it

Add one line to your COURSE-MAP.md under the Reflections section at the bottom:

```
- 2026-05-27 | S0.1 + S0.2 | Toolchain installed and first commit pushed. The Git pane is less scary than I expected.
```

(Adjust the date and feel free to be honest about the experience.)

Save the file (`Ctrl + S` in any editor). Switch to the RStudio Git pane. You should see COURSE-MAP.md now shows a blue `M` icon (Modified).

Stage it (click checkbox) → Commit → message: `Add reflection for sessions 0.1 and 0.2` → Commit → Push.

Refresh GitHub. The reflection line is now visible there.

### Check 3 — Find your repo URL

In your browser, at the top of your GitHub repo, copy the URL. It'll look like:

```
https://github.com/<your-username>/r-data-science-journey
```

Save this somewhere accessible. From Session 1.1 onward, you can paste this URL in chat instead of uploading files. I'll fetch them.

### Check 4 — Confirm `.gitignore` exists and is doing something useful

Open the `.gitignore` file in RStudio (just click it in the Files pane). It should already contain things like:

```
.Rproj.user
.Rhistory
.RData
.Ruserdata
```

These are RStudio's internal session files — Git ignores them so they don't clutter your commits. You can add patterns here later (like `data/secret/*` if you ever have private data in a public repo).

---

## Going deeper *(optional rabbit holes)*

- **Why "main" and not "master"?** Until 2020, Git's default branch was called `master` (an old technical convention from a different domain). GitHub, GitLab, and the Git project itself renamed the default to `main` in 2020, citing both inclusivity and "main" being more semantically accurate. You'll still encounter `master` in older repos — they work identically.

- **Personal access tokens (PATs).** GitHub stopped accepting passwords for Git operations in 2021. Now you authenticate via PATs (tokens that act like API keys) or SSH keys. RStudio handles PAT setup pretty smoothly; SSH is more powerful but more setup. Bryan's *Happy Git with R* covers both — read her chapter when you're curious.

- **What `git init` actually creates.** When RStudio "initialised a Git repository" for you, it created a hidden `.git` folder inside your project. That folder contains *everything* — every commit, every change, every branch. The visible files in your folder are just the "current state"; the history lives in `.git`. If you ever delete `.git` by accident, all version history is gone. Don't.

- **The `.Rproj.user` folder.** You may see this appear in your project. It's RStudio's session state (open files, cursor positions, plot history). The `.gitignore` already excludes it — never commit it. If you ever clone the repo on a different machine, RStudio creates a fresh one.

---

## Stay-current corner

This session's one thing: **bookmark [Jenny Bryan's *Happy Git with R*](https://happygitwithr.com)**. It's the single best resource on Git for R users. She updates it. When you hit a Git problem you can't solve (you will, eventually — everyone does), this is the first place to look. Her chapter on "Dealing with push rejection" alone has saved more PhDs than any other text in the field.

---

## Commit message suggestion

For this session, you'll have made multiple commits during the walkthrough. The first one was probably:

```
Initial commit: course-spine documents and Session 0.1 notes
```

If you make more commits as part of the post-session checklist (adding session 0.2 notes, updating COURSE-MAP), a reasonable next message:

```
Add Session 0.2 notes; mark sessions 0.1 and 0.2 complete in COURSE-MAP
```

---

## Cross-references

- **Previous:** Session 0.1 — Install & configure
- **Next:** Session 1.1 — R as a calculator, vectors, types, the assignment ritual
- **Stats course parallel:** none — toolchain sessions are R-course specific
- **Logistics:** [Recipe 3](../../LOGISTICS-HANDBOOK.md#recipe-3--where-to-put-files-on-windows-and-why-not-onedrive) (Windows folders), [Recipe 4](../../LOGISTICS-HANDBOOK.md#recipe-4--vs-code-setup-for-this-course) (VS Code setup)

---

## How I'd ask Claude this *(meta-skill preview)*

When you encounter a Git error during a push, the high-value prompt pattern is:

> "I tried to push my first commit and got this error:
>
> ```
> [paste the entire error output verbatim]
> ```
>
> Here's what I did just before:
> [list the commands you ran]
>
> What does this error mean and how do I fix it?"

Git errors look terrifying but they're usually informative once you know how to read them. Quoting them verbatim (rather than describing them) is what makes them debuggable. We'll formalise this pattern in Phase 8.

---

## My notes

*Your space. Annotate freely. See Recipe 1 in LOGISTICS-HANDBOOK.*


- *(2026-05-27)* The Git pane is intuitive once you realise stage = checkbox.
- *(2026-05-27)* The projects are game changer. The here package — I get it. Solves a problem I didn't know I had.
- **Q:** What's the difference between staging and committing again?


---

*End of Session 0.2. By now: project created, here installed, repo on GitHub, first commit pushed. Note one moment that surprised you in your COURSE-MAP reflections. Then take a break — Phase 1 starts the actual R fluency journey.*
