# Git

I want to see the cumulative changes of a branch's commits: `git diff base_branch_hash::feature_branch_hash`

TODO: I want to test the contents of a certain branch on a local temporary branch: 

```sh

```

I want to display the history visually: `git log --graph --oneline --decorate`

I staged the wrong code: `git restore --staged whatever_files`

I modified the wrong branch, but I still need the changes: stash the changes and then reset the branch to the latest commit: `git stash -m "comment"` and `git reset --hard`

I need to reset the local repo to the latest from the remote repo: `git fetch --all` and `git reset --hard origin/master` (`master` is the name of the desired branch)

I committed a wrong commit: `git revert commit_hash` and `git push origin branch_name`
I made a wrong commit: `git reset HEAD~` (?)

I need to update a branch: 

1. Merge : `git checkout main`, `git fetch`, `git pull origin main`, `git checkout branch`, `git merge main`, `git push origin branch`
2. Rebase: 
3. Squash: 

I need to pick and apply commits from another branch in the same repository: 

I need to pick and apply commits from another branch from another repository: 

I need to setup a remote: 

I need to setup another remote: 

I need to list all branches in the current repository: `git branch -a`

I need to delete a branch: 

I need to stash some code to return to later: 

I need to create and assign a tag: 
