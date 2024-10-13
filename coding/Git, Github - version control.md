24.10.11  23.41
tags: [[web]] [[git,github]] 

# Git, Github - version control

![[Pasted image 20241013021500.png|400]]
- commit messages are written in present tense
- git status
- git log

## gitignore
- choose which files not to track
- os generated files
- DS store files

### wild cards
- `\*.log`  don't track everything that has .log extension

### git rm --cached -r
- remove from staging area.

### view current remote repo
- `git remote -v`
### remove current remote repo
- `git remote rm origin`
### add a remote repo
- `git remote add origin <repo>`

### add to staging area, to the local git repo and the remote repo with one command line
- `git commit -am 'commit message' -u origin  // isn't working for me ` or
- `git add . ; git commit -m 'commit message' ; git push  // worked`

## cloning
- `git clone repository`  copy's from remote to working directory

## Branching and merging
![[Pasted image 20241013023104.png|400]]

- `git branch branch-name   // create a new branch`
- `git checkout branch-name2  // switch to another branch`
- `git branch  // see which branch you're working on`

### merge to a certain branch
- first checkout to main
- `git merge branch-name`
- `:q!`   exit out of the terminal

## Forking and pull requests
![[Pasted image 20241013024548.png|500]]
### Pull request
- if approved, merge person 2 repository or changes will be reflected on person 1.


# Reference

[[The Complete 2023 Web Development Bootcamp]]