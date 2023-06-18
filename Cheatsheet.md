


# Github Best Practices
- Commit early and often
- Don’t panic
- Useful commit messages
- Useful branch names
- Experiment
- Perform work in a feature branch 
- Delete local and remote feature branch after merging
- Use .gitignorefiles to exclude files that you do not want to commit

# Gitbasics
Create a new Branch:
- git branch newBranch 

Using it:
- git checkout newBranch
- git add .
- git commit -m "message"

Push the newbranch to the remote(website version) for the firsttime:
- git push -u origin newBranch

Note: Next time you can then just do a "git push" command

Getting the list of branches in a repo:
- git branch

Checking the status of changes in your local workspace:
- git status
- git log

Merging branch A in branch B:
- git checkout B
- git merge A

Temporary storing somechangeset so that they are not lost:
- git stash 

Find the list of remote branches available:
- git remote -v 

Fetching changes from a remote branch: 
- git pull

## How to resolve merge conflicts 

Given an instance where by there are changes on github to the master branch and it conflicts with your current branch. No worries, github handles this nicely.

**Summary of process**: Ensure your local master branch is up-to-date. If so then merge your local master branch into your current branch(and not vice versa! please do not merge your current branch into master). Resolve the merge conflict manually, then add the changes to your local branch. and create a pull request(Pull request is the only allowed means for merging you branch into master).

- Firstly on your terminal log into your local master branch
```
git checkout master
```
- Then ensure that your local master branch is up to date with the remote master branch on github. To do this use the pull command
```
git pull
```
- Now that your local master is update, log into your personal branch 
```
git checkout yourBranch 
```
- Merge master into your branch 
```
git merge master
```
Manually resolve all merge conflict by looking through the highlighted files on visual studio code
- Once complete. Run the following commands
```
git add .
git commit -m “Resolved merge conflict” 
git push 
```
- Go on the github website and create a pull request. 

Note: Below you start the above process - ensure that you had committed all your current changes in your local branch
```
git add .
git commit -m “”
git push
```