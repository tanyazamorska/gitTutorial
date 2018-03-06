### GIT COMMANDS
`git fetch` - download updates from github
`git merge [{from_where}]` - merge {from_where} to current branch
    ex: `git mege origin/master`
`git pull` -> `git fetch` + `git merge`
`git pull --rebase`  -> `git fetch` + `git rebase`
`git status` - see if has changes
`git log` - to see all commits with hash codes
`git reset {hash_from_git_log}` - reset commit.
`git reset --hard HEAD` - remove all changes.
`git reset --hard {hash_from_git_log}` - reset commit + remove changes
`git add {filename |-A | .}` - add files to commit or to reset
`git commit -m "comment"` - create commit
`git push` - push changes to github
`git branch` - show local branches
`git branch --all` - show all branches(including remote)
`git branch {branch_name}` - create branch
`git checkout {branch_name}` - switch to branch if it is exists locally or remotely 
`git checkout -b {branch_name}` -> `git branch {branch_name}` + `git checkout {branch_name}`
`git branch -D myNewBranch` - delete local branch
`git push origin :{branchName}` - delete remote branch from github
`git rebase --continue` - continue rebasing, after conflicts resolved

### STANDARD FLOW
```
git pull --rebase
git checkout -b myBranch
// do some
git add -A
git commit -m "???"
git push
```
### CONFLICT FLOW
```
git pull --rebase (and see conflicts)
// open intelliji idea -> RMC on root folder -> GIT -> resolve Conflicts
git add -A
git rebase --continue (or --abort)
```
