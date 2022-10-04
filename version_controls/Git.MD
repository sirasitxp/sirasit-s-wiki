## Repository
```
Origin -> Your local repository  
Upstream -> Official repository  
```
## Good Practice
Don't work on main. Create a branch, work on it, and then merge later.  
```
git branch [name]  
```
## Switch to another branch
```
git checkout [name]
```

## Show current status
```
git status
```

## See difference
```
git diff
```

## Combine to current version
```
git rebase [name]
```

## Push
```
git push [remote] [branch]
```

## List out remotes
```
git remote -v
```

## Cancel merge
```
git merge --abort 

OR

git reset --hard HEAD
```

## Logging each commits
```
git log
```

## Template
```bash
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin [project_link]
git push -u origin main
```
