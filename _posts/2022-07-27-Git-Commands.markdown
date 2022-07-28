---
layout: post
title:  "Git Commands"
date:   2022-07-27 07:14:30 -0500
categories: Technology
---

# Clone a repository

```
git clone <repository-url>
```

# Branch

## Find current branch

```
git branch
```

## Switch from current branch to develop branch

```
git checkout develop
```

## Get the latest code for develop branch

```
git pull
```

## Create new branch feature/abc from the current (develop) branch

```
git checkout -b feature/abc
```

## Pull the latest code in develop branch (remote) to current (feature/abc) branch

```
git pull origin develop
```

## Delete a local branch

```
git branch -D feature/abc
```

# Push your code changes

## See what has changed

```
git status
```

## Stage file myupdatedfile.txt

```
git add myupdatedfile.txt
```

If all the updated files from `git status` command need to be commited, then use the following command

```
git add .
```

## Commit files

```
git commit -m "Commit message text"
```

## Push changes

```
git push
```