[UP](../index.md)

# Git 
Git is a distributed version-control system for tracking changes in source code during software development.

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Handbook](https://guides.github.com/introduction/git-handbook/)

## Getting
Initializing a Repository in an Existing Directory
`$ cd /home/user/my_project`
`$ git init` creates a new subdirectory named .git that contains all of your necessary repository files

Cloning an Existing Repository
syntax: git clone <url>
`$ git clone https://github.com/libgit2/libgit2` creates a directory named libgit2, initializes a .git directory inside it
or `$ git clone https://github.com/libgit2/libgit2 mylibgit` cloning and renaming

## Status
Checking the Status of Your Files
`$ git status`

message:
`On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean` 
clean working directory; in other words, none of your tracked files are modified

`$ git status -s` short status

## Adding and Staging
Tracking New Files `$ git add README` now tracked and staged to be committed

## Ignoring
.gitignore file: files that you don’t want Git to automatically add or even show you as being untracked

## Differences
`git diff` shows you the exact lines added and removed — the patch, as it were (unstaged changes)
`git diff --staged` or `git diff --cached` compares your staged changes to your last commit

## Commiting
`$ git commit` commit everything that is staged (opens editor)
`$ git commit -v` puts the diff of your change in the editor so you can see exactly what changes you’re committing
`$ git commit -m "Story 182: Fix benchmarks for speed"` -m arg lets you leave a message

`$ git commit -a -m 'added new benchmarks'` Adding the -a option to the git commit command makes Git automatically stage every file that is already tracked before doing the commit, letting you skip the git add part

## Removing
`$ git rm PROJECTS.md` git rm stages the file’s removal
`$ git rm PROJECTS.md -f` If you modified the file or had already added it to the staging area, you must force the removal with the -f option
`$ git rm --cached README` you may want to keep the file on your hard drive but not have Git track it anymore

## Renaming
`$ git mv README.md README` renaming 

# GitHub
GitHub is a global company that provides hosting for software development version control using Git.

- [Guides](https://guides.github.com/)