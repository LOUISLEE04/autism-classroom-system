# /sync — Push Latest Data to Private Repo

Pushes all current classroom files to the private backup repo.

## Steps for Claude to execute

### 1. Check private remote exists

```bash
git remote -v
```

- If `private` remote exists → proceed
- If not → tell teacher: "You haven't set up private sync yet. Say **set up private sync** and I'll get that sorted for you."

### 2. Stage and commit any changes

```bash
git add .
git status
```

If there are changes to commit:

```bash
git commit -m "Classroom update — [today's date]"
```

If nothing has changed since last sync, tell teacher: "Everything is already up to date — no new changes to push."

### 3. Push to private repo

```bash
git push private main
```

### 4. Confirm

> "✅ Synced. Your latest classroom data has been pushed to your private repo.
> LOUISLEE04 can now see the latest version."

---

## Notes for Claude
- Run all commands via Bash tool — no manual steps for teacher
- Keep commit messages simple and date-stamped
- If push fails (auth issue, network), explain clearly and suggest running `gh auth setup-git` then retrying
