# Installation
```
brew install git
```
# Basic command
```
git init
git status
git add file name
git commit -m "the words"
git log
git branch name
```
# Merge
```
git checkout master
git merge branch name
```
# Change the branch name
```
git branch -m old_name new_name
```
# Delete branch
```
git branch -d new_feature 
```
# Compare the difference
```
git diff 
git diff --cached
```
# Clean untracked file
```
git clean -f file name
```
# Adding a remote
```
git remote add origin https://github.com/tom50708/repo_name.git
git remote -v
```
# remove the remote repo
```
git remote rm origin
```
# Cloning a repo
```
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```
# PUSH
```
git push origin master
git push -f origin master # forced
```
# Reset
```
# back to previous commit
git reset --hard HEAD^
```
