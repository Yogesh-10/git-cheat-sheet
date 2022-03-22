### Collaboration

Cloning a repository

```bash
git clone url
```

Syncing with remotes

```bash
git fetch origin master # Fetches master from origin

git fetch origin # Fetches all objects from origin

git fetch # Shortcut for “git fetch origin”

git pull # Fetch + merge

git push origin master # Pushes master to origin

git push # Shortcut for “git push origin master”
```

Sharing tags

```bash
git push origin v1.0 # Pushes tag v1.0 to origin

git push origin —delete v1.0
```

Sharing branches

```bash
git branch -r # Shows remote tracking branches

git branch -vv # Shows local & remote tracking branches

git push -u origin bugfix # Pushes bugfix to origin

git push -d origin bugfix # Removes bugfix from origin
```

Managing remotes

```bash
git remote # Shows remote repos

git remote add upstream url # Adds a new remote called upstream

git remote rm upstream # Remotes upstream
```
