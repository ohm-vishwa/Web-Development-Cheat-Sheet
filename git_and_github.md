## Configuring Git

> ## to see configuration
```sh
git config --list
```

> ## to set user name
```sh
git config --global user.name "ohm_vishwa"
```

> ## to set email
```sh
git config --global user.email "example@email.com"
```

## Basic Commands

> ## to initialize git
```sh
git init
```

> ## to clone github repo
```sh
git clone <url>
```

> ## to view files
```sh
ls
```

> ## to view hidden files
```sh
ls -la
```

> ## to check status
```sh
git status
```

> ## to staging single file
```sh
git add <file name>
```

> ## to staging all files
```sh
git add .
```

> ## to commit on git
```sh
git commit -m "message"
```

> ## to add & commit togther 
```sh
git commit -am "message"
```

> ## to push code on github repo (Once)
```sh
git push -u origin main
```

> ## after `-u origin main` 
```sh
git push
```

> ## to verify remote
```sh
git remote -v
```

> ## to add remote repo 
```sh
git remote add origin <url>
```

> ## to set new url
```sh
git remote set-url origin <url> 
```

> ## to check branch
```sh
git branch
```

> ## to rename branch
```sh
git branch -M main
```

> ## to navigate
```sh
git checkout <branch name>
```

> ## to create new branch
```sh
git checkout -b <new branch name> 
```

> ## to delete branch
```sh
git branch -d <branch name>
```

> ## to push other branch
```sh
git push --set-upstream origin <branch name>
```

> ## to compare commits, branches, files & more
```sh
git diff <branch name>
```

> ## to merge 2 branches or create pull request
```sh
git merge <branch name>
```

> ## to feth & dawnload content from a remote repo to local repo
```sh
git pull origin main
```

> ## to view all commit 
```sh
git log
```

> ## to remove staged changes
```sh
git reset <file name>
```

or,
```sh
git reset
```

> ## to restore commited changes (for one commit)
```sh
git reset HEAD~1
```

> ## to restore commited changes (for many commits) using `git log`
```sh
git reset <commit hash>
```

or,
```sh
git commit --hard <commit hash> 
```