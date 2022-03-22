### **Rewriting History**

Undoing commits

```bash
git reset --soft HEAD^ # Removes the last commit, keeps changed staged

git reset --mixed HEAD^ # Unstages the changes as well

git reset --hard HEAD^ # Discards local changes
```

Reverting commits

```bash
git revert 72856ea # Reverts the given commit

git revert HEAD~3.. # Reverts the last three commits

git revert --no-commit HEAD~3..
```

Recovering lost commits

```bash
git reflog # Shows the history of HEAD

git reflog show bugfix # Shows the history of bugfix pointer
```

Amending the last commit

```bash
git commit --amend
```

Interactive rebasing

```bash
git rebase -i HEAD~5
```
