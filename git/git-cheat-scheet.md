# GIT CHEAT SHEET

## BASICS
### Init / Clone

```
//Initialize git in the current directory
git init


//Clone an existing repo into current directory
git clone <url>


//Clone an existing repo into a new folder 
git clone <url> 'new folder name'

```
### Status
```
//This gives you an overview over the files that have been changed - and if they are tracked or not
git status
```
### Adding files to staging-area
```
//Add a specific (updated) file
git add <file-path/filename>

//Add all updated files
git add .

```
### Commit
_There are some resources on writing good commit messages in the ["Git resources overview"](./git-resources.md)_
```
//Create a commit for the changes in the staging area
git commit -m "write your descriptive commit message here"


//Update latest commit
git commit --amend -m "new message"
```

## BRANCHING
```
//Create new branch
git branch <branch name>


//Switch branch
git chekout <branch name>


//Create new branch (branch-B) based on existing branch(branch-A) and switch to it
git checkout -b <branch-B-name> <branch-A-name>


//Merge branch (branch-A) into other branch (branch-B)
git chekout <branch-B-name>
git merge <branch-A-name>


//Delete branch
git branch -d <branch name>

```

## UPDATE

```
//fetch latest changes from origin (this does not merge them)
git fetch


//pull latest changes from origin (does a fetch followed by a merge)
git pull

```
## REVERT 
```
//Return to latest commit state (NOTE! THIS CANNOT BE UNDONE)
git reset --hard

//revert to a specific commit
git revert <ID>

//revert the last commit
git revert HEAD
```

## MERGE CONFLICTS
_There are a lot of great tools for viewing merge conflicts, and if you are new to git I especially reccomend using such a tool (I prefer that myselfe, even though I have used git for years)_
```
//View the difference that creates the conflict
git diff


```
