#### Push, pull, and sync your work with remote repositories.

Merge/Fuse the changes of 1 branch
```
git merge <rama>
```

Adds external repo
```
git remote add <name> <url>
```

Send changes to external repo
```
git push <external> <branch>
```

Gets and fuses the changes from the external repo
```
git pull <external> <branch>
```

Rebase instead of merge (common practice):
```
git pull --rebase <remote> <branch>
```