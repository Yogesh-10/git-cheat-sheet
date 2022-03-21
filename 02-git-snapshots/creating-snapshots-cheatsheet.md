### Creating Snapshots

Initializing a repository

```bash
git init
```

Staging files

```bash
git add file1.js # Stages a single file

git add file1.js file2.js # Stages multiple files

git add *.js # Stages with a pattern

git add . # Stages the current directory and all its content
```

Viewing the status

```bash
git status # Full status
git status -s # Short status
```

Committing the staged files

```bash
git commit -m “Message” # Commits with a one-line message
git commit # Opens the default editor to type a long message
```

Skipping the staging area

```bash
git commit -am “Message”
```

Removing files

```bash
git rm file1.js # Removes from working directory and staging area

git rm --cached file1.js # Removes from staging area only
```

Renaming or moving files

```bash
git mv file1.js file1.txt
```

Viewing the staged/unstaged changes

```bash
git diff # Shows unstaged changes

git diff --staged # Shows staged changes

git diff --cached # Same as the above
```

Viewing the history

```bash
git log # Full history

git log --oneline # Summary

git log --reverse # Lists the commits from the oldest to the newest
```

Viewing a commit

```bash
git show 921a2ff # Shows the given commit

git show HEAD # Shows the last commit

git show HEAD~2 # Two steps before the last commit

git show HEAD:file.js # Shows the version of file.js stored in the last commit
```

Unstaging files (undoing git add)

```bash
git restore --staged file.js # Copies the last version of file.js from repo to index
```

Discarding local changes

```bash
git restore file.js # Copies file.js from index to working directory

git restore file1.js file2.js # Restores multiple files in working directory

git restore . # Discards all local changes (except untracked files)

git clean -fd # Removes all untracked files
```

Restoring an earlier version of a file

```bash
git restore --source=HEAD~2 file.js
```
