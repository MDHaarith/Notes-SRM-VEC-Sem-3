# Notes-SRM-VEC-Sem-3

Class notes for Sem 3, ECE (R2023) — SRM Valliammai.
For classmates, by classmates. No git experience needed.

## Subjects

| Code | Subject | Folder |
|---|---|---|
| MA3321 | Transforms and Partial Differential Equations | `MA3321-Transforms-PDE/` |
| EC3362 | Solid State Devices and Circuits | `EC3362-Solid-State-Devices/` |
| EC3363 | Signals and Systems | `EC3363-Signals-Systems/` |
| EE3363 | Electric Circuit Analysis | `EE3363-Circuit-Analysis/` |
| EC3365 | Electromagnetic Fields | `EC3365-EM-Fields/` |
| EC3366 | Digital Systems Design | `EC3366-Digital-System-Design/` |
| EC3367 | Electronics Circuits Design Lab | `EC3367-ECD-Lab/` |
| EE3369 | Circuit Theory and Devices Lab | `EE3369-Circuit-Theory-Lab/` |

Each folder has `notes/`, `question-banks/`, and `lab-manuals/` (labs only).

## What you (classmate) need to do

1. **One-time setup (10 min):** install Python (gives you `pip`) + Git — see Part 0 below.
2. **Upload notes:** clone the repo, add your file, commit, push, open a pull request — see Part 1 below.

## Git in 5 words

You already know WhatsApp. Git is the same idea, with history and undo.

| Word | WhatsApp analogy | What it really is |
|---|---|---|
| repo | the group itself | folder with full history |
| commit | sending a message | one save point with a message |
| push / pull request | forwarding to group + admin approves | proposing your save to be added |
| pull | downloading new messages | getting others' latest saves |
| merge | admin allows it in | approved saves join the main copy |

---

## Part 0 — One-time setup (Windows + Mac)

You need two tools: **Python (gives you `pip`)** and **Git**. Do this once.

### 0a. Install Python + pip

`pip` comes bundled with Python — you don't install it separately. You just install Python and verify pip exists.

**Windows**

1. **Get the installer:** go to [python.org/downloads](https://www.python.org/downloads/) (official) **or** open the Microsoft Store and search "Python".
2. **Run it:** run the installer. Tick **"Add python.exe to PATH"** before clicking Install.
   (Store version handles PATH automatically.)
3. **Verify:** open **PowerShell** (press `Win` key, type `PowerShell`, press Enter) and check:
   ```powershell
   py -3 --version
   py -3 -m pip --version
   ```
   Both should print version numbers. If `pip` is missing: `py -3 -m ensurepip --default-pip`.

**Mac**

1. **Get the installer:** go to [python.org/downloads/macos](https://www.python.org/downloads/macos/) and run the macOS installer. (Alternatively `xcode-select --install` gives you system tools, but python.org is the predictable path.)
2. **Verify:** open **Terminal** (`Cmd + Space`, type `Terminal`, press Enter) and check:
   ```bash
   python3 --version
   python3 -m pip --version
   ```
   If `pip` is missing: `python3 -m ensurepip --default-pip`.

Source: [docs.python.org — Installing Python Modules](https://docs.python.org/3/installing/index.html) (`pip` ships with Python binary installers).

### 0b. Install Git

**Windows** — pick one:

- Easiest (official installer): go to [git-scm.com/download/win](https://git-scm.com/download/win), download starts automatically, run it, accept defaults.
- Or with winget in PowerShell:
  ```powershell
  winget install --id Git.Git -e --source winget
  ```
  Then **close and reopen** PowerShell and check: `git --version`.

**Mac** — pick one:

- Easiest: open Terminal and type `git --version`. macOS pops up an installer for the Xcode Command Line Tools — click Install.
- Or download the installer from [git-scm.com/download/mac](https://git-scm.com/download/mac).
- Or with Homebrew (if you have it): `brew install git`.

Source: [git-scm.com — Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

### 0c. Tell git who you are (once per laptop)

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
```

Check it worked: `git config --global --list`.

---

## Part 1 — Upload notes with git

**Step 1 — Get the repo once.**

```bash
git clone <repo-url>
cd Notes-SRM-VEC-Sem-3
```

**Step 2 — Put your file in the right folder.** Move your notes file into the subject folder, e.g. `EC3363-Signals-Systems/notes/Unit-2-Fourier-rahul.pdf`. PDFs or images are fine.

**Step 3 — Check what changed.**

```bash
git status
```

**Step 4 — Save your work.**

```bash
git checkout -b my-notes                          # your own branch, once per upload
git add EC3363-Signals-Systems/notes/Unit-2-Fourier-rahul.pdf
git commit -m "Add Unit 2 Fourier notes - EC3363"
```

Verb + what + subject. That's the whole convention:

```
Add Unit-2 Laplace notes - MA3321
Fix typo in EC3362 Unit-1 diode types
Add DSD Lab Exp-3 - EC3366
```

**Step 5 — Send it up.**

```bash
git push -u origin my-notes    # first push on this branch; afterwards just: git push
```

**Step 6 — Open a pull request.** On GitHub, click **Compare & pull request** → **Create pull request**:

![GitHub yellow banner: "Compare & pull request" button. Official GitHub Docs screenshot.](https://docs.github.com/assets/images/help/pull_requests/pull-request-compare-pull-request.png)

Full guide: [Creating a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

**Step 7 — Done.** A maintainer clicks Merge. Your file has history forever — who added it, when, why. That's it: commit = save point, pull request = "please add my save".

**Get classmates' latest:**

```bash
git pull
```

**Undo (why git beats Drive):**

- Wrong file? Open the commit on GitHub → **Revert**. History keeps both versions.
- Overwritten? **History** button on any file shows every version. Click one to download it.
- Terminal: `git status` before every commit; `git log --oneline -5` to see recent saves.

---

## Rules (keep it usable)

- File names: `Unit-<n>-<topic>-<your-name>.pdf` (e.g. `Unit-2-Laplace-rahul.pdf`)
- One topic per file. No `final-final-v2.pdf`.
- Question papers go in `question-banks/`, lab work in `lab-manuals/`, not `notes/`.

## Private repo?

This repo is private to classmates. Ask the owner to invite you (Settings → Collaborators). Accept the email invite, then follow Part 1 above.
