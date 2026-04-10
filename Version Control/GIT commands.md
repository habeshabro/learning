```sh
git config -h
git help config
git config [--global | --system | --local ] key value

git init
git status
git add <file>  #stage
git rm --cached <file> #unstage
git restore --staged <file> #unstage
git restore <file> #undo changes
git commit -m "some message"
git commit -a -m "commit all changes even unstaged"
git diff
git log
git reset <commit id>
git branch <name of branch>
git branch
git switch <name of branch>
git merge -m "merge message" <branch to be merged>
git branch -d <branch to be deleted>
git remote add <name like origin> <url>
git push -u origin main #set upstream for current branch to main
git fetch + merge = git pull

```

.gitignore
```gitignore
#this is a comment
*.txt
```