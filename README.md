**Personal GitHub Workflow (Detailed Flowchart with Commands, Comments & Sample Project)**

## **Flowchart Steps:**

1. **Start**
   - User decides to work on a new project or contribute to an existing one.

2. **Initialize Repository**
   - Clone an existing repository → `git clone <repo-url>`
   - OR create a new repository on GitHub → `git init`
   - Add a remote repository → `git remote add origin <repo-url>`
   - Check remote repository → `git remote -v`

3. **Create a New Feature Branch**
   - `git checkout -b feature-branch` (Creates and switches to the branch)
   - View all branches → `git branch -a`
   - Switch between branches → `git checkout <branch-name>`
   - Fetch latest changes from remote → `git fetch origin`
   - Rebase with main branch if necessary → `git rebase main`

4. **Make Changes**
   - Modify or add new files.
   - Check status using `git status`.
   - Discard unwanted changes → `git checkout -- <file>`
   - View changes before committing → `git diff`

5. **Stage and Commit Changes**
   - Stage all changes → `git add .`
   - Stage a specific file → `git add <file>`
   - Commit changes → `git commit -m "Description of changes"`
   - Amend last commit (if needed) → `git commit --amend`

6. **Push Changes to GitHub**
   - If on a new branch: `git push -u origin feature-branch`
   - If working on `main`: `git push origin main`
   - View remote branches → `git branch -r`
   - Rename a branch → `git branch -m <new-branch-name>`
   - Resolve conflicts if necessary → `git merge main` or `git rebase main`

7. **Open a Pull Request (PR) on GitHub**
   - Compare changes with `main`.
   - Assign reviewers for code review.
   - Edit or close PR if needed.

8. **Code Review Process**
   - If approved → Proceed to merge.
   - If changes requested → Modify, commit, and push again.
   - If necessary, abandon PR.
   - Sync with latest main changes → `git pull --rebase origin main`

9. **Merge PR into Main Branch**
   - Via GitHub UI or `git merge feature-branch`.
   - Optional: Delete `feature-branch` locally (`git branch -d feature-branch`).
   - Delete remote branch → `git push origin --delete feature-branch`
   - Sync local main branch → `git pull origin main`

10. **Deploy & Maintain**
    - Deploy changes manually or through CI/CD pipelines.
    - Monitor the application and fix any arising issues.
    - Rollback to a previous commit → `git revert <commit-hash>`
    - Reset to a previous state → `git reset --hard <commit-hash>`

11. **End**
    - Workflow resets for new features or updates.

---
### **Detailed Flowchart Representation with Comments & Sample Data:**

```
     [Start]  # Begin Git workflow
        |
        v
  [Initialize Repo]  # Clone or create a repository (git clone/git init)
        |
        v
  [Create Branch]  # Create and switch to a feature branch (git checkout -b feature-branch)
        |
        v
  [Fetch Latest Changes]  # Sync latest updates from the main branch (git fetch origin)
        |
        v
  [Make Changes]  # Modify files, add new features (git status, git diff)
        |
        v
  [Stage & Commit]  # Stage and save changes (git add, git commit -m "message")
        |
        v
  [Resolve Conflicts?]  # If conflicts exist, resolve them (git merge, git rebase)
        |
        v
  [Push to GitHub]  # Push branch to remote repository (git push origin feature-branch)
        |
        v
  [Open PR]  # Open a pull request on GitHub
        |
        v
  [Code Review]  # Review by team members
        |
        v
  [Requested Changes?]  # If changes are requested, update and push again
        |
        v
  [Update PR]  # Modify and update pull request
        |
        v
  [Merge PR]  # Merge changes into the main branch (git merge feature-branch)
        |
        v
  [Deploy & Monitor]  # Deploy updates and monitor performance
        |
        v
      [End]  # Workflow complete, ready for the next feature
```

---
### **Sample Project Example:**
**Project:** `My-Personal-Blog`
- **Repository Name:** `my-personal-blog`
- **Feature Branch:** `feature-add-dark-mode`
- **Main Branch:** `main`

**Example Commands for Workflow:**
```sh
# Clone the repository
$ git clone https://github.com/username/my-personal-blog.git
$ cd my-personal-blog

# Create a new feature branch
$ git checkout -b feature-add-dark-mode

# Make changes and stage them
$ git add .
$ git commit -m "Added dark mode support"

# Push changes and open PR
$ git push -u origin feature-add-dark-mode
```


