# Github Best Practices - Cheatsheet
- Commit early and often
- Don’t panic
- Useful commit messages
- Useful branch names
- Experiment
- Perform work in a feature branch 
- Delete local and remote feature branch after merging
- Use .gitignorefiles to exclude files that you do not want to commit

# Gitbasics
1. Firstly create the repo manaully on the Github website 

2. Clone the repo to your local pc
- `git clone <repoLink>`

3. Navigate into the repo on your local pc
- `cd <folderName>`

4. Create a new Branch:
- `git checkout -b <newBranchName>`


5. Once you've made your code changes, you can push the changes to github by 
- `git add .`
- `git commit -m "message"`

6. Push the newbranch to the remote(website version) for the firsttime:
- `git push -u origin <newBranchName>`

7. Note: Next time you, want to push to your changes up on this branch, you can then just do a `git push` command

8. Once you've created a pull request and the change has been merged into the main/master branch - delete the new branch through the github website. Then 

9. On your local PC, checkout the main/master branch 
- `git checkout <main or master>` 

10. Fetch the updated changes from a remote main/master branch: 
- `git pull`

11. To begin working on new feature, then create a new branch by repeating `step 4 - step 7 above `

Checking the status of changes in your local workspace:
- `git status`

Temporary storing somechangeset so that they are not lost:
- `git stash`



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
git checkout <yourBranchName> 
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