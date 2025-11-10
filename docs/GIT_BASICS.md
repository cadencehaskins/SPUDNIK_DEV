# Git Basics - Quick Reference

## The 4 Commands You'll Use Most

### 1. Check what's changed
```bash
git status
```
Shows what files you've modified, added, or deleted.

### 2. Save your changes locally
```bash
git add .
git commit -m "Describe what you changed"
```
- `git add .` = stage all changes
- `git commit` = save a snapshot with a message

### 3. Push to GitHub (backup online)
```bash
git push
```
Uploads your commits to GitHub.

### 4. Pull from GitHub (get latest)
```bash
git pull
```
Downloads any changes from GitHub (useful if working from multiple computers).

---

## Typical Workflow

Every time you finish working on something:

```bash
# 1. See what changed
git status

# 2. Save it
git add .
git commit -m "Added power unit model"

# 3. Backup to GitHub
git push
```

**That's it!** Do this frequently (every 30 mins to 1 hour of work).

---

## Good Commit Messages

✅ **Good:**
- "Add Pump model with flow validation"
- "Fix BOM export formatting issue"
- "Update rules engine to handle flow dividers"

❌ **Bad:**
- "updates"
- "stuff"
- "asdfasdf"

**Why it matters:** You'll thank yourself later when you need to find when something broke!

---

## View Your History

```bash
git log --oneline
```
Shows all your commits in a simple list.

---

## Oh No, I Messed Up!

### Undo changes to a file (before commit)
```bash
git checkout -- filename.js
```

### Undo last commit (keep the changes)
```bash
git reset --soft HEAD~1
```

### See what changed in a file
```bash
git diff filename.js
```

---

## Your Repository

**GitHub URL:** https://github.com/cadencehaskins/SPUDNIK_DEV

**Local Path:** `/home/cadence/DEV/SPUDNIK_TEST/`

---

## Tips

1. **Commit often** - Small, frequent commits are better than huge ones
2. **Push to GitHub daily** - Protects against computer crashes
3. **Don't commit sensitive data** - No passwords, API keys, etc.
4. **`.gitignore` protects you** - It prevents committing junk files

---

## Need Help?

Just ask me! I can help with:
- "Show me what I changed"
- "Save my work and push to GitHub"
- "Undo my last commit"
- "Create a new branch for testing"

---

*Pro tip: Get in the habit of running `git status` constantly. It's like checking your mirrors while driving!*
