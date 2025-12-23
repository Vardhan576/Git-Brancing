# Git-Brancing
Learning Git Branching

## Completed Levels (5/5)

Successfully completed all 5 introductory levels of Learn Git Branching tutorial on December 23, 2025.

### Level 1: Introduction to Git Commits
**Objective**: Make two commits to understand how Git commits work.

**Commands Used**:
git commit
git commit

**Concepts Learned**:
- Commits are snapshots of your project
- Each commit has a parent reference
- HEAD points to the current commit
- Commits are lightweight and efficient

**Status**: COMPLETED (2 commands, matched solution)

---

### Level 2: Branching in Git
**Objective**: Create a new branch named bugFix and switch to it.

**Commands Used**:
git checkout -b bugFix

**Concepts Learned**:
- Branches are lightweight pointers to commits
- git checkout -b creates and switches to a branch in one command
- Branch names appear with asterisk when checked out
- Multiple branches can point to the same commit

**Status**: COMPLETED (1 command, exceeded solution efficiency)

---

### Level 3: Branching and Merging
**Objective**: Create branches, make commits on each, then merge them together.

**Commands Used**:
git checkout -b bugFix
git commit
git checkout main
git commit
git merge bugFix

**Concepts Learned**:
- Merge commits combine two branch histories
- A merge commit has two parents (both branch histories)
- git merge integrates changes from another branch
- Merging maintains the complete history

**Status**: COMPLETED (5 commands, matched solution)

### Level 4: Git Rebase
**Objective**: Create parallel branches and rebase to linearize history.

**Commands Used**:
git checkout -b bugFix
git commit
git checkout main
git commit
git checkout bugFix
git rebase main

**Concepts Learned**:
- Rebasing replays commits on top of another branch
- Creates a linear history (unlike merge which creates a commit)
- Original commits are replaced with rebased versions (with different hashes)
- Useful for maintaining clean, linear project history
- Both approaches (merge vs rebase) achieve the same end state but with different histories

**Status**: COMPLETED (6 commands, matched solution)

---

### Level 5: Detach yo HEAD
**Objective**: Detach HEAD from a branch and attach it directly to a commit.

**Commands Used**:
git checkout C4

**Concepts Learned**:
- HEAD normally points to a branch reference
- HEAD can be detached to point directly to a commit
- Useful for exploring history or testing code at specific commits
- Detached HEAD allows inspecting past states
- Shown as "HEAD -> C4" instead of "HEAD -> main"

**Status**: COMPLETED (1 command, perfectly matched solution)

---

## Summary

- **Total Levels Completed**: 5/5
- **Date Completed**: December 23, 2025
- **Total Commands Executed**: 20
- **Efficiency**: Exceeded solution for 1 level, matched for 4 levels

## Key Takeaways

1. **Commits** are snapshots of your work
2. **Branches** are lightweight pointers allowing parallel development
3. **Merging** combines histories maintaining a complete record
4. **Rebasing** linearizes history by replaying commits
5. **HEAD** can point to branches OR commits directly
