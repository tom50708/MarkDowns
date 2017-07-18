# Installation
```
brew install git
```
# Basic command
```ruby
git init
git status
git add file name
git commit -m "the words"
git log
git branch name
```
# Merge
```ruby
git checkout master
git merge branch name
```
# Change the branch name
```ruby
git branch -m old_name new_name
```
# Delete branch
```ruby
git branch -d new_feature 
```
# Compare the difference
```ruby
git diff 
git diff --cached
```
# Clean untracked file
```ruby
git clean -f file name
```
# Adding a remote
```ruby
git remote add origin https://github.com/tom50708/repo_name.git
git remote -v
```
# remove the remote repo
```ruby
git remote rm origin
```
# Cloning a repo
```ruby
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```
# PUSH
```ruby
git push origin master
```