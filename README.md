# Master Git: Branch Comparisons & Stash Workflows

Comparing file changes across branches or managing temporary uncommitted work can slow down your velocity if you don't know the exact flags. Here is a concise guide to navigating cross-branch diffs and managing your stash effectively.

---

## 1. Compare Specific Folders Across Branches

```bash
git diff --stat branch_A..branch_B -- relative/folder/path

```

## 2. Essential Git Stash Commands

When you need to context-switch without polluting your commit history, use `git stash`.

### Save Uncommitted Work with a Message

Avoid mystery stashes. Always tag your stashed work with a clear description:

```bash
git stash push -m "WIP: refactor auth middleware"

```

### View All Stashes

```bash
git stash list

```

### Apply and Drop a Specific Stash

Pop a specific entry by index (drops it from the list after applying):

```bash
git stash pop stash@{1}

```

### Apply and Drop the Latest Stash

Quickly restore and delete the most recent stash entry:

```bash
git stash pop

```
