# Git

# Log
20220930 - initial file creation
20220930 - working - notes on -- bare

# Commands

## init
- create an empty repository or reinilize an old one
- creates a hidden .git directory to store all relavent information
```
git init [-q | --quiet] [--bare] [--template=<template-directory>]
	  [--separate-git-dir <git-dir>] [--object-format=<format>]
	  [-b <branch-name> | --initial-branch=<branch-name>]
	  [--shared[=<permissions>]] [<directory>
```
- running git init in an existing repository is ok
- it will not overwrite things that are already there
- the primary reason for rerunning git init is to pick up newly added templates (or to move the repository to another place)
- --bare will create a bare repo