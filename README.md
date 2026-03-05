# Git Version Control Practice

This repository demonstrates basic Git operations such as creating commits, resetting history, amending commits, reverting changes, and pushing to GitHub.

---

## 🚀 Git Commands Used

Here is the step-by-step workflow followed in this repository, tracking the file `script.py`:

### 1. Initial Commits (Making 4 Commits)
Initialize the repository, track the file, and make 4 initial commits:
```bash
git init
git add script.py
git commit -m "the first commit"
```
*Commit hash: `04e91ee`*

```bash
git commit -am "adding second line"
```
*Commit hash: `1db573d`*

```bash
git commit -am "adding third line"
```
*Commit hash: `df0323b`*

```bash
git commit -am "adding fourth"
```
*Commit hash: `585be39`*

### 2. Resetting History
Delete the last two commits from the local history using a hard reset, bringing the HEAD back to the second commit:
```bash
git reset --hard HEAD~2
```

### 3. Commit After Deletion
Create a new commit branching off from the reset history:
```bash
git commit -am "commit after delete"
```
*Commit hash: `cde58ef`*

### 4. Amending the Commit
Create a new commit "lab done", and then immediately amend it to change the message to "finish":
```bash
git commit -am "lab done"
git commit --amend -m "finish"
```
*Commit hash: `fd2bf49`*

### 5. Initial Push to GitHub
Rename the default branch to `main`, connect to the remote repository, and push the history:
```bash
git branch -M main
git remote add origin [https://github.com/marwantarek-eng/VC-ITI46.git](https://github.com/marwantarek-eng/VC-ITI46.git)
git push -u origin main
```

### 6. Reverting Multiple Commits
Revert the last two commits safely (creating new commits that undo the changes of "finish" and "commit after delete"):
```bash
git revert HEAD~2..HEAD
```
*Commit hashes: `2951373` and `228eebf`*

### 7. Final Push
Push the newly created revert commits to the remote repository:
```bash
git push -u origin main
```


## 📜 Final Commit History

After executing the workflow above, the final `git log --oneline` reflects the precise sequence of operations:

```text
228eebf Revert "commit after delete"
2951373 Revert "finish"
fd2bf49 finish
cde58ef commit after delete
1db573d adding second line
04e91ee the first commit
```

---

## 👨‍💻 Author

**Marwan Tarek**
* 📧 **Email:** [marwantarek75@gmail.com](mailto:marwantarek75@gmail.com)
* 🐙 **GitHub:** [@marwantarek-eng](https://github.com/marwantarek-eng)
