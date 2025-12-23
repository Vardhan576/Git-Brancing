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

## Level-wise Screenshots and Diagrams

### Level 1: Introduction to Git Commits

**Problem Statement:**
Learn how Git commits work by making two commits. Understand that commits are lightweight snapshots of your project that maintain history.

**Visual Diagram (Current State):**
```
C0 (Initial Commit)
  |
  v
C1 (Starting Point)
with main* pointing here
```

**Solution Diagram (Answer State):**
```
C0
  |
  v
C1
  |
  v
C2 (After: git commit)
  |
  v
C3 (After: git commit)
with main* pointing here
```

---

### Level 2: Branching in Git

**Problem Statement:**
Create a new branch named 'bugFix' and check it out. Understand that branches are lightweight pointers that allow parallel development.

**Visual Diagram (Current State):**
```
C0 - C1 (C2)
main* pointing at C2
```

**Solution Diagram (Answer State):**
```
C0 - C1 (C2)
     with main and bugFix* both pointing here
```

---

### Level 3: Branching and Merging

**Problem Statement:**
Create diverging branches on main and bugFix, make commits on each, then merge bugFix into main. Learn about merge commits with two parents.

**Visual Diagram (Current State - Diverged Branches):**
```
      C2 (main)
     /
C0-C1
     \\
      C3 (bugFix*)
```

**Solution Diagram (Answer State - After Merge):**
```
      C2
     / \\
    /   \\
   C1   C3
    \\   /
     \\ /
      C4 (Merge Commit)
   main* pointing here
   bugFix also pointing at C3
```

---

### Level 4: Git Rebase

**Problem Statement:**
Create diverging branches and rebase bugFix onto main to linearize the history. Understand that rebase replays commits on top of another branch.

**Visual Diagram (Current State - Diverged):**
```
     C2 (main*)
    /
C0-C1
    \\
     C3 (bugFix*)
```

**Solution Diagram (Answer State - After Rebase):**
```
C0 - C1 - C2 - C3 (bugFix*, C3 is rebased)
   main pointing at C2
   (Linear history instead of branched)
```

---

### Level 5: Detach yo' HEAD

**Problem Statement:**
Detach HEAD from the bugFix branch and attach it directly to commit C4. Understand that HEAD can point directly to a commit instead of a branch.

**Visual Diagram (Current State - HEAD attached to branch):**
```
C0 - C1 - C2 - C3 - C4
              bugFix*
   (HEAD -> bugFix)
```

**Solution Diagram (Answer State - HEAD detached):**
```
C0 - C1 - C2 - C3 - C4
              bugFix
   (HEAD -> C4, detached)
```

---

## How to View Screenshots

To view the actual interactive screenshots and complete visualizations of each level:
1. Visit [Learn Git Branching](https://learngitbranching.js.org/)
2. Navigate through each level in the Introduction Sequence
3. Observe the real-time visualization on the right side as you execute commands
4. Compare your solution with the goal visualization shown in the pink panel

## Resources

- **Official Learn Git Branching**: https://learngitbranching.js.org/
- **Git Documentation**: https://git-scm.com/doc
- **Branching Model**: https://nvie.com/posts/a-successful-git-branching-model/
