# /setup-private-sync — Set Up Private Backup Repo

One-time setup. Claude handles everything — you just confirm once.

This creates a **private** GitHub repository for your classroom data and invites your system administrator (LOUISLEE04) as a collaborator, so they can help with support and diagnostics if needed.

**Your student data never becomes public.** Only you and LOUISLEE04 can see the private repo.

---

## What Claude does automatically

1. Checks if GitHub CLI (`gh`) is installed and you are logged in
2. Gets your GitHub username
3. Creates a private repo named `[your-username]-classroom-private`
4. Pushes all your classroom files to it
5. Invites LOUISLEE04 as collaborator
6. Saves the repo link to your teacher profile

---

## Steps for Claude to execute

### 1. Check gh is available and authenticated

```bash
gh auth status
```

- If authenticated → proceed
- If not → tell the teacher:

  > "You need a free GitHub account and the GitHub CLI to use this feature.
  > 1. Create a free account at github.com if you don't have one
  > 2. Download GitHub CLI at cli.github.com and install it
  > 3. Run this command in your terminal: `gh auth login` — follow the steps
  > 4. Come back and say 'set up private sync' again"
  >
  > Stop here until they confirm they're ready.

### 2. Get their GitHub username

```bash
gh api user --jq .login
```

Save this as `[TEACHER_GITHUB]`.

### 3. Confirm with teacher before creating anything

Tell the teacher:

> "I'll create a private GitHub repo called **[TEACHER_GITHUB]-classroom-private** and invite **LOUISLEE04** as a collaborator so they can access your classroom files for support purposes.
>
> Your student data will be private — only you and LOUISLEE04 can see it.
>
> Shall I proceed? (yes / no)"

Only proceed if they say yes.

### 4. Create the private repo

```bash
gh repo create [TEACHER_GITHUB]-classroom-private \
  --private \
  --description "Pendidikan Khas classroom data (private)"
```

### 5. Add private remote and push

```bash
git remote add private https://github.com/[TEACHER_GITHUB]/[TEACHER_GITHUB]-classroom-private.git
git push private main
```

If push fails due to auth, run `gh auth setup-git` first then retry.

### 6. Invite LOUISLEE04 as collaborator

```bash
gh api repos/[TEACHER_GITHUB]/[TEACHER_GITHUB]-classroom-private/collaborators/LOUISLEE04 \
  -X PUT \
  -f permission=push
```

### 7. Save to teacher profile

Append to `memory/teacher-profile.md`:

```markdown
## Private Sync
- Private repo: https://github.com/[TEACHER_GITHUB]/[TEACHER_GITHUB]-classroom-private
- Remote name: `private`
- Collaborator: LOUISLEE04 (system administrator)
- Set up: [today's date]
```

### 8. Confirm to teacher

> "✅ Done! Your private repo is live at:
> https://github.com/[TEACHER_GITHUB]/[TEACHER_GITHUB]-classroom-private
>
> LOUISLEE04 has been invited — they'll accept the invitation shortly.
>
> To push your latest files anytime, just say: **sync my data** or run `/sync`"

---

## Notes for Claude
- Run all shell commands via Bash tool — teacher does not need to touch the terminal
- If any step fails, explain clearly what went wrong in plain language (no technical jargon)
- If private remote already exists (`git remote -v` shows one), skip creation and just invite the collaborator
- This command is fully optional — never push the teacher to run it
