# ✅ GitHub Cheatsheet
## 🚀 Create a new branch locally and Push it to GitHub

1. Navigate to your local repository in the terminal:
    ```bash
    cd /path/to/your/repo
    ```
2. Create a new branch (This will also switch you to the new branch):
    ```bash
    git checkout -b new-branch-name
    ```

3. Push the new branch to GitHub:
    ```bash
    git push -u origin new-branch-name
    ```
    > The -u flag sets the "upstream", so future git push/pull commands work without needing to specify the branch name.
        > if you don't include the -u, then on all future push and pull comamnds, you will need to specify the branch name as follows:
        ```bash
        git push origin new-branch-name
        git pull origin new-branch-name
        ```

## 🪾 Branches

*  List all branches (local and remote):
    ```bash
    git branch -a
    ```

* Switch to an existing branch:
    ```bash
    git checkout branch-name
    ```

* Create a new branch and switch to it:
    ```bash
    git checkout -b new-branch-name
    ```
    > Remember to push the new branch to GitHub after creating it:
    ```bash
    git push -u origin new-branch-name
    ```

* Check what branch you are currently on:
    ```bash
    git branch
    ```

* delete a local branch:
    ```bash
    git branch -d branch-name
    ```

* delete a remote branch:
    ```bash
    git push origin --delete branch-name
    ```


## 🔄 Check if your local repository is in sync with your remote one

1. Fetch the latest changes from the remote repository:
    ```bash
    git fetch origin
    ```

2. Compare your local repo's status with the remote repo:
    ```bash
    git status
    ```

3. If the repos are out of sync, you can see the differences by running:
    ```bash
    git diff origin/branch-name
    ```

4. If you have no local changes, and want to update your local repo to match the remote:
    ```bash
    git pull origin main
    ```

5. If you have local changes and want to merge them with the remote changes:
    First, you have to resolve any conflicts that may arise. After resolving conflicts, you can commit the changes:
    ```bash
    git add .
    git commit -m "Resolved merge conflicts"
    ```

## ❌ Fixing Mistakes

* Undo changes to a specific file:
    ```bash
    git checkout -- filename
    ```

* Unstage a file that you didn't mean to add:
    ```bash
    git reset filename
    ```

* undo the last commit (but keep the changes):
    ```bash
    git reset --soft HEAD~1
    ```

## 📝 Additional Notes & Tips

### 🧭 Main Vs. Master
* Some repositories apparently use "master" instead of "main" as the default branch name. If you encounter this, replace "main" with "master" in the commands above.

### 💡 Useful Commands
* To quickly check the status of your repository:
    ```bash
    git status
    ```

* To view the commit history:
    ```bash
    git log --oneline
    ```

### 🧠 General Tips
* Always run `git status` before committing to see what changes are staged, unstaged, or untracked.
