## Configuring Git
==}> see configuration
```sh
git config --list
```
==}> set user name
```sh
git config --global user.name "ohm_vishwa"
```
==}> set email
```sh
git config --global user.email "example@email.com"
```

## Basic Commands
==}> initialzing git
```sh
git init
```
==}> clone github repo
```sh
git clone <url>
```
==}> view files
```sh
ls
```
==}> view hidden files
```sh
ls -la
```
==}> check status
```sh
git status
```
==}> staging single file
```sh
git add <file name>
```
==}> staging all files
```sh
git add .
```
==}> commit to git
```sh
git commit -m "message"
```
==}> add & commit togther 
```sh
git commit -am "message"
```
==}> push code on github repo (Once)
```sh
git push -u origin main
```
==}> after `-u origin main` 
```sh
git push
```
==}> add remote repo 
```sh
git remote add origin <url>
```
==}> verify remote
```sh
git remote -v
```
==}> check branch
```sh
git branch
```
==}> to rename branch
```sh
git branch -M main
```
==}> to navigate
```sh
git checkout <branch name>
```
==}> to create new branch
```sh
git checkout -b <new branch name>
```
==}> to delete branch
```sh
git branch -d <branch name>
```
