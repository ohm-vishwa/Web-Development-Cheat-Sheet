## Configuring Git

> ## see configuration
```sh
git config --list
```

> ## set user name
```sh
git config --global user.name "ohm_vishwa"
```

> ## set email
```sh
git config --global user.email "example@email.com"
```

## Basic Commands

> ## initialize git
```sh
git init
```

> ## clone github repo
```sh
git clone <url>
```

> ## view files
```sh
ls
```

> ## view hidden files
```sh
ls -la
```

> ## check status
```sh
git status
```

> ## staging single file
```sh
git add <file name>
```

> ## staging all files
```sh
git add .
```

> ## commit on git
```sh
git commit -m "message"
```

> ## add & commit togther 
```sh
git commit -am "message"
```

> ## push code on github repo (Once)
```sh
git push -u origin main
```

> ## after `-u origin main` 
```sh
git push
```

> ## verify remote
```sh
git remote -v
```

> ## add remote repo 
```sh
git remote add origin <url>
```

> ## set new url
```sh
git remote set-url origin <url> 
```

> ## check branch
```sh
git branch
```

> ## rename branch
```sh
git branch -M main
```

> ## navigate
```sh
git checkout <branch_name>
```

> ## create new branch
```sh
git checkout -b <new_branch_name> 
```

> ## delete branch
```sh
git branch -d <branch_name>
```

> ## push other branch
```sh
git push --set-upstream origin <branch_name>
```

> ## compare commits, branches, files & more
```sh
git diff <branch_name>
```

> ## merge 2 branches or create pull request
```sh
git merge <branch_name>
```

> ## feth & dawnload content from a remote repo local repo
```sh
git pull origin main
```

> ## view all commit 
```sh
git log
```

> ## remove staged changes
```sh
git reset <file_name>
```

or,
```sh
git reset
```

> ## restore commited changes (for one commit)
```sh
git reset HEAD~1
```

> ## restore commited changes (for many commits) using `git log`
```sh
git reset <commit_hash>
```

or,
```sh
git commit --hard <commit_hash> 
```