# Git Tutorial

Welcome to this comprehensive Git tutorial! This README will guide you through essential and advanced Git commands, with helpful tips, examples, and best practices. Let’s get started! 🎉

---

## 1. Basic Git Configuration

Set your global username and email to identify your commits:

```bash
git config --global user.name "<username>"
git config --global user.email "<useremail>"
````

Set the default branch to `main` for new repositories:

```bash
git config --global init.defaultBranch main
```

Clear your terminal (equivalent to `cls` in Windows):

```bash
clear
```

---

## 2. Initialize and Track a Repository

Initialize a new Git repository in the current folder:

```bash
git init
```

Check the status of your repository (shows current branch, staged and unstaged changes):

```bash
git status
```

Add a file to the staging area:

```bash
git add <filename>
```

Add all modified and new files:

```bash
git add --all
# or
git add -A
# or
git add .
```

Remove a file from Git tracking (but keep it locally):

```bash
git rm --cached <filename>
```

Recursively remove a folder from tracking:

```bash
git rm --cached -r <foldername>
```

Completely remove a file from your repository:

```bash
git rm "<filename>"
```

Rename a file:

```bash
git mv "<original filename>" "<new filename>"
```

Commit your changes with a descriptive message:

```bash
git commit -m "<your commit message>"
```

Skip the staging area and commit all tracked changes:

```bash
git commit -a -m "<commit message>"
```

Amend the last commit (e.g., fix a typo in the commit message):

```bash
git commit --amend -m "<new commit message>"
```

Use relative dates to change commit timestamps (e.g., "3.days.ago"):

```bash
git commit --date="3.days.ago" -m "Cheeky backdated commit"
```

---

## 3. The `.gitignore` File

To ignore specific files or directories, create a `.gitignore` file in your repository:

```
# Example .gitignore
*.pyc
__pycache__/
logs/
*.log
.env
```

> **Pro Tip:** Use `.gitignore` to keep sensitive or unnecessary files out of your repository.

---

## 4. Inspecting and Comparing Changes

See modifications to tracked files:

```bash
git diff
```

Restore a file to its last committed state:

```bash
git restore <filename>
```

Unstage a file from the staging area:

```bash
git restore --staged <filename>
```

---

## 5. Viewing Commit History

Detailed commit logs:

```bash
git log
```

Short, one-line commit logs:

```bash
git log --oneline
```

View diffs for each commit:

```bash
git log -p
```

---

## 6. Resetting and Rebasing

Reset your repository to a specific commit (revert the working directory to that commit):

```bash
git reset <commit-id>
```

Rebase interactively from the root commit:

```bash
git rebase -i --root
# In Vim: make your changes, then press :x to save and exit.
```

---

## 7. Working with Branches

Create a new branch:

```bash
git branch <branchname>
```

View all branches:

```bash
git branch
```

Delete a branch:

```bash
git branch -d <branchname>
```

Rename the current branch to `main`:

```bash
git branch -M main
```

Switch to another branch:

```bash
git switch <branchname>
```

Create and switch to a new branch:

```bash
git switch -c <new-branch-name>
```

Another option to switch to another branch:

```bash
git checkout <another-branch-name>
```

Delete a branch:

```bash
git push -d <remote-name> <branch-name>
```

Delete a branch using --force:

```bash
git push -D <remote-name> <branch-name>
```

---

## 8. Merging Branches

Merge another branch into your current branch:

```bash
git merge -m "<merge commit message>" <branchname>
```

> **Important:** Commit your changes before merging to avoid conflicts!

---

### Resolving Merge Conflicts

If a conflict occurs during a merge:

1. Open the conflicted file.
2. Choose between `HEAD` (your current branch) or the incoming branch (`<<<<<<<`, `=======`, `>>>>>>>`).
3. Delete the conflict markers and unnecessary content.
4. Save the file.
5. Commit the resolved changes:

```bash
git commit -m "Resolved merge conflict"
```

---

## 9. Pushing to a Remote Repository

After renaming your main branch:

```bash
git push -u origin main
```

---

## 10. Additional Helpful Commands

* Display help for any Git command:

```bash
git help <command>
```

* Configure handy aliases in `.gitconfig`:

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

* View differences between branches:

```bash
git diff <branch1>..<branch2>
```

* Temporarily store uncommitted changes:

```bash
git stash
git stash apply
```

* Clone a remote repository:

```bash
git clone <repository-url>
```

* Check remote URLs:

```bash
git remote -v
```

---

## 11. Bonus Tips & Trivia

🌟 Use Git hooks (in `.git/hooks/`) to automate tasks like running tests before a commit.
🌟 Explore Git GUI tools like GitKraken, Sourcetree, or VS Code’s Git integration!
🌟 Git was created by Linus Torvalds in 2005 to manage the Linux kernel.
🌟 Collaborate using platforms like GitHub, GitLab, or Bitbucket for remote repositories and issue tracking.

---

### 🎉 Conclusion

This tutorial covers the essentials and some advanced Git commands to get you started.
Feel free to experiment, explore, and commit responsibly! 🚀

---

*If you have questions or want to expand this tutorial, open an issue or PR in this repository!*

```

Let me know if you’d like to tweak the structure, add advanced sections (like rebasing workflows, squashing, etc.), or include diagrams or images to make it even more visual. 🚀
```