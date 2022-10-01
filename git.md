# Git

# Log
20220930 - initial file creation
20220930 - working - notes on -- bare
20221001 - working - atlassian tutorial - finished git clone

# terminology

## clone
- used to point to an existing directory and make a copy of it into a new directory
```
git clone [--template=<template-directory>]
	  [-l] [-s] [--no-hardlinks] [-q] [-n] [--bare] [--mirror]
	  [-o <name>] [-b <name>] [-u <upload-pack>] [--reference <repository>]
	  [--dissociate] [--separate-git-dir <git-dir>]
	  [--depth <depth>] [--[no-]single-branch] [--no-tags]
	  [--recurse-submodules[=<pathspec>]] [--[no-]shallow-submodules]
	  [--[no-]remote-submodules] [--jobs <n>] [--sparse] [--[no-]reject-shallow]
	  [--filter=<filter> [--also-filter-submodules]] [--] <repository>
	  [<directory>]
```
- typically a one time operation
- creates a remote connection called origin which points back to the original repository

## hooks
- scripts that automatically run every time a particular event occurs in a repository

## init
- create an empty repository or reinitialize an old one
- creates a hidden .git directory to store all relevant information
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

## bare repository
- a repository where no commits can be made
- changes cannot be tracked
- has no working tree in the folder structure
- the only possible operations are pushing or cloning
- ? can you also do a pull

## push
- uploads a local repository to a remote location

## pull
- fetches, downloads and then immediately updates a local repository from a remote connection

## remote
- a connection to another repository

## tag
- used to capture a specific reference point