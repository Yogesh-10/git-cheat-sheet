### git-cheat-sheet

# Reference for git commands.

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

### **Browsing History**

Viewing the history

```bash
git log --stat # Shows the list of modified files

git log --patch # Shows the actual changes (patches)
```

Filtering the history

```bash
git log -3 # Shows the last 3 entries

git log --author=“Mosh”

git log --before=“2020-08-17”

git log --after=“one week ago”

git log --grep=“GUI” # Commits with “GUI” in their message

git log -S“GUI” # Commits with “GUI” in their patches

git log hash1..hash2 # Range of commits

git log file.txt # Commits that touched file.txt
```

Formatting the log output

```bash
git log --pretty=format:”%an committed %H”
```

Creating an alias

```bash
git config --global alias.lg “log --oneline"
```

Viewing a commit

```bash
git show HEAD~2

git show HEAD~2:file1.txt # Shows the version of file stored in this commit
```

Comparing commits

```bash
git diff HEAD~2 HEAD # Shows the changes between two commits

git diff HEAD~2 HEAD file.txt # Changes to file.txt only
```

Checking out a commit

```bash
git checkout dad47ed # Checks out the given commit

git checkout master # Checks out the master branch
```

Finding a bad commit

```bash
git bisect start

git bisect bad # Marks the current commit as a bad commit

git bisect good ca49180 # Marks the given commit as a good commit

git bisect reset # Terminates the bisect session
```

Finding contributors

```bash
git shortlog
```

Viewing the history of a file

```bash
git log file.txt # Shows the commits that touched file.txt

git log --stat file.txt # Shows statistics (the number of changes) for file.txt

git log --patch file.txt # Shows the patches (changes) applied to file.txt
```

Finding the author of lines

```bash
git blame file.txt # Shows the author of each line in file.txt
```

Tagging

```bash
git tag v1.0 # Tags the last commit as v1.0

git tag v1.0 5e7a828 # Tags an earlier commit

git tag # Lists all the tags

git tag -d v1.0 # Deletes the given tag
```
