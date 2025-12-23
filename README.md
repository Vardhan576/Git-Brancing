# Git-Brancing
Learning Git Branching

### Level 1: Introduction to Git Commits
**Objective**: Make two commits to understand how Git commits work.

**Commands Used**:
```
git commit 
git commit
```
- 
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
<img width="1051" height="600" alt="Screenshot 2025-12-23 120550" src="https://github.com/user-attachments/assets/4624eba2-14df-4d99-81d6-af64124f3b9b" />


---

### Level 2: Branching in Git
**Objective**: Create a new branch named bugFix and switch to it.

**Commands Used**:
```
git checkout -b bugFix
```
**Problem Statement:**
Create a new branch named 'bugFix' and check it out. Understand that branches are lightweight pointers that allow parallel development.


**Visual Diagram (Current State):**
```
C0 - C1 (C2)
main* pointing at C2
```

**Solution Diagram (Answer State):**


<img width="1919" height="915" alt="Screenshot 2025-12-23 121735" src="https://github.com/user-attachments/assets/d23b6f27-0bf4-42ca-b996-c8e3338cd4db" />

---

### Level 3: Branching and Merging
**Objective**: Create branches, make commits on each, then merge them together.

**Commands Used**:
```
git checkout -b bugFix
git commit
git checkout main
git commit
git merge bugFix
```
**Problem Statement:**
Create diverging branches on main and bugFix, make commits on each, then merge bugFix into main. Learn about merge commits with two parents.

**Solution Diagram (Answer State - After Merge):**


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



## Level-wise Screenshots and Diagrams




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
