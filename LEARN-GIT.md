# Learn Git by Uploading Notes

You already know how to share files on WhatsApp. Git is the same idea, with history and undo.

## The 5 words you need

| Word | WhatsApp analogy | What it really is |
|---|---|---|
| repo | the group itself | folder with full history |
| commit | sending a message | one save point with a message |
| push / pull request | forwarding to group + admin approves | proposing your save to be added |
| pull | downloading new messages | getting others' latest saves |
| merge | admin allows it in | approved saves join the main copy |

## Do it once (web only)

1. **Repo**: you're in it. This page is the repo.
2. **Commit**: `Add file → Upload files` → write message `Add <what> - <subject>` → green **Commit changes** button. You just committed.
3. **Pull Request**: GitHub auto-opens "Compare & pull request" → **Create pull request**. That asks: "merge my commit?"
4. **Merge**: a maintainer clicks Merge. Done. Your file has history forever — who added it, when, why.

Second time onwards it's the same 3 clicks.

## Naming your commit (so history stays readable)

```
Add Unit-2 Laplace notes - MA3321
Fix typo in EC3362 Unit-1 diode types
Add DSD Lab Exp-3 - EC3366
```

Verb + what + subject. That's the whole convention.

## Optional: git on your laptop (only when curious)

```bash
git clone <repo-url>
cd Notes-SRM-VEC-Sem-3
# add your file into e.g. EC3363-Signals-Systems/notes/
git add .
git commit -m "Add Unit 2 notes - EC3363"
git push
```

Same words as the website buttons. The website _is_ git, just with buttons.

## Undo (why git beats Drive)

- Wrong file? Open the commit → **Revert**. History keeps both versions.
- Overwritten? **History** button on any file shows every version. Click one to download it.
