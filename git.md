# Git

## Log

20220930 - initial file creation  
20220930 - working - notes on -- bare  
20221001 - working - atlassian tutorial - saving changes  
20221002 - working - atlassian tutorial - inspecting a repository  

## terminology

### add

- adds a change in the working directory to the staging area
- tells git you want to include a specific file in the next commit
- can add files or directories

### aliases

- custom CLI shortcuts
- designed to be used with frequently used commands to save time
- common example would be to an alias to remove files form the staging area
- can be local or global in scope
- can be created in CLI or editing the source files directly

### branch

- #TODO

### clone

- used to point to an existing directory and make a copy of it into a new directory

``` bash
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

### commit

- safe snapshot / milestone of the current project
- best practice is to use atomic commits
- amend ca be used to edit the last commit

### config

- used to set configuration values on a local (repository), global (user) or system (all users) level
- can be used to configure colors, whitespace, diff settings etc.

### diff

- takes two input data sets and outputs the changes between them
- runs a diff command on potential data sources - commits, branches, files etc.

### hooks

- scripts that automatically run every time a particular event occurs in a repository

### init

- create an empty repository or reinitialize an old one
- creates a hidden .git directory to store all relevant information

```bash
git init [-q | --quiet] [--bare] [--template=<template-directory>]
    [--separate-git-dir <git-dir>] [--object-format=<format>]
    [-b <branch-name> | --initial-branch=<branch-name>]
    [--shared[=<permissions>]] [<directory>  
```

- running git init in an existing repository is ok
- it will not overwrite things that are already there
- the primary reason for rerunning git init is to pick up newly added templates (or to move the repository to another place)
- --bare will create a bare repo

### .gitignore

- used to ignore specific files or directories
- a specific file that stores what to ignore
- usually stored in root project folder

### bare repository

- a repository where no commits can be made
- changes cannot be tracked
- has no working tree in the folder structure
- the only possible operations are pushing or cloning
- ? can you also do a pull

### log

- displays a list of committed snapshots
- only operates on committed history, not the working directory

### origin

- shorthand for the repository location a project was initially cloned from

### push

- uploads a local repository to a remote location

### pull

- fetches, downloads and then immediately updates a local repository from a remote connection

### remote

- a connection to another repository

### stash

- temporarily shelves changes you made to the working
- useful if you need to switch tasks to work on something else and are not right ready to commit changes
- saved locally, not pushed to server with a push
- can pop a stash which will remove the changes from a stash and apply them to the working directory
- stash apply is the opposite

### status

- displays the state of the working directory
- shows what has been staged, what is being tracked

### tag

- used to capture a specific reference point
