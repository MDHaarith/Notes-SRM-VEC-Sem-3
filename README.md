# Notes-SRM-VEC-Sem-3

Class notes for Sem 3, ECE (R2023) — SRM Valliammai.
For classmates, by classmates. No git experience needed. Everything you need is on this page.

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
2. **Upload notes (2 min, browser only):** see Part 1 below.
3. **Optional terminal way:** see Part 2 below.

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

### 0d. Copy-paste in the terminal (read this, it bites beginners)

Copying **commands** from this page into your terminal, and copying **files** into folders, are different things:

**Copy a command from here → paste into terminal:**

- **Windows PowerShell:** copy with `Ctrl + C` in the browser, then paste into PowerShell with `Ctrl + V` **or** right-click. Copy *out of* PowerShell with `Ctrl + Shift + C`. Warning: `Ctrl + C` *inside* a running program means "stop it" — so if something is running, use `Ctrl + Shift + C` to copy.
- **Windows Git Bash:** paste with right-click → **Paste**, or `Ctrl + Shift + V` / `Shift + Insert`.
- **Mac Terminal:** same as everywhere else — `Cmd + C` to copy, `Cmd + V` to paste.
- After pasting a command, always press **Enter** to run it. If the text wraps onto two lines, delete the stray line break first.

**Copy a notes file into the repo folder (for the terminal method):**

- **Windows:** `Win + E` opens Explorer. Copy with `Ctrl + C`, open the subject's `notes/` folder, paste with `Ctrl + V`. Or drag-drop the file.
- **Mac:** Finder → `Cmd + C`, go to the folder, `Cmd + V`. Or drag-drop.
- You don't need the terminal for files at all if you use Part 1 (browser upload).

---

## Part 1 — Upload notes (browser only, no terminal)

This is what 90% of classmates will use. You learn git by doing it.

**Step 1 — Open the folder.** On GitHub, click a subject folder, then `notes/`. To just read: click any file to view/download.

**Step 2 — Click Add file → Upload files.** Above the file list there's an **Add file** button:

![GitHub "Add file → Upload files" button, outlined in orange. Official GitHub Docs screenshot.](https://docs.github.com/assets/images/help/repository/upload-files-button.png)

Full guide: [Adding a file to a repository](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository).

**Step 3 — Drag your file in.** Drag-drop your PDF (max 25 MiB per file in browser, 100 files at once) or click **choose your files**.

**Step 4 — Write a commit message.** In the "Commit message" box type:

```
Add Unit-2 Laplace notes - MA3321
```

Verb + what + subject. That's the whole convention. More examples:

```
Add Unit-2 Laplace notes - MA3321
Fix typo in EC3362 Unit-1 diode types
Add DSD Lab Exp-3 - EC3366
```

**Step 5 — Propose it.** Below the message, select **Create a new branch**, then click **Propose changes**:

![GitHub commit screen: "Commit directly" vs "Create a new branch" options.](https://docs.github.com/assets/images/help/repository/choose-commit-branch.png)

That opens a **Pull Request** — "please add my save". Click **Create pull request**:

![GitHub yellow banner: "Compare & pull request" button.](https://docs.github.com/assets/images/help/pull_requests/pull-request-compare-pull-request.png)

Full guide: [Creating a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

**Step 6 — Done.** A maintainer clicks Merge. Your file has history forever — who added it, when, why. That's it: commit = save point, pull request = "please add my save". Second time onwards it's the same clicks.

> Screenshots above are from the official GitHub Docs (linked under each one), so they always match the current GitHub UI.

---

## Part 2 — Same thing in the terminal (only when curious)

The buttons above _are_ git. Here are the matching commands:

```bash
# 1. Get the repo once
git clone <repo-url>
cd Notes-SRM-VEC-Sem-3

# 2. Copy your PDF into the right folder, e.g.
#    EC3363-Signals-Systems/notes/Unit-2-Fourier-rahul.pdf
#    (use Explorer/Finder copy-paste, see 0d)

# 3. Save (commit) + propose (push)
git status                    # what changed? always look first
git add EC3363-Signals-Systems/notes/Unit-2-Fourier-rahul.pdf
git commit -m "Add Unit 2 Fourier notes - EC3363"
git push -u origin my-notes   # first push; afterwards just: git push

# 4. Get classmates' latest
git pull
```

Then open the repo on GitHub and click **Compare & pull request** (same screenshot as Part 1, Step 5).

Undo (why git beats Drive):

- Wrong file? Open the commit on GitHub → **Revert**. History keeps both versions.
- Overwritten? **History** button on any file shows every version. Click one to download it.
- Terminal: `git status` before every commit; `git log --oneline -5` to see recent saves.

---

## Rules (keep it usable)

- File names: `Unit-<n>-<topic>-<your-name>.pdf` (e.g. `Unit-2-Laplace-rahul.pdf`)
- One topic per file. No `final-final-v2.pdf`.
- Never upload: passwords, API keys, `client_secret*.json`, phone numbers.
- Question papers go in `question-banks/`, lab work in `lab-manuals/`, not `notes/`.

## Private repo?

This repo is private to classmates. Ask the owner to invite you (Settings → Collaborators). Accept the email invite, then follow Part 1 above.
