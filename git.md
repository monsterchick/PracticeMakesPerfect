# Git 

## WORKFLOW

1. Working Directory
   - write codes & add
2. Stage / Index
   - rm / commit
3. Commit History
   - push / reset
4. Remote Repository

## SETUP

```python
# check account
git config --global user.name
git config --global user.email

# setup account
git config --global user.name "<username>"
git config --global user.email "<github_email>"
```

## STAGE & SNAPSHOT

```python
# show modified files in working directory
git status

# add a file as it looks now to the stage for next commit
git add <file>

# unstage a file while retaining the changes in working directory
git reset <file>

# commit the staged content as a new commit snapshot
git commit -m "<descriptive message>"

# back to a specific commit and keep files in Working Directory and Stage
git reset --soft HEAD~<number_back>

# back to a specific commit and reset Working Directory and Stage
git reset --hard HEAD~<number_back>
```

## BRANCH & MERGE

```python
# list all branches
git branch

# create a new branch at the current commit
git branch <branch_name>

# switch to another branch and check it out into the working directory
git checkout <branch_name>

# 1. create an empty branch without commit history
git checkout --orphan <empty_branch>
# 2. remove all files
git rm -rf .
# 3. push the empty branch to remote
git push -u origin <empty_branch>

# merge the specified branch’s history into the current one
git merge <alias>/<branch>
```

## SHARE & UPDATE

```python
# add a git URL as an alias; <alias> is usually "origin"
git remote add <alias> <url>

# fetch down all the branches from that Git remote
get fetch <alias>/<branch>

# Transmit local branch commits to the remote repository branch
git push <alias>/<branch>

# fetch and merge any commits from the tracking remote branch
git pull
```

## TRACKING PATH CHANGES

```python
# delete the file from project and stage the removal for commit
git rm <file>

# remove a file from the index(staging area)
git rm --cache <file>
```

