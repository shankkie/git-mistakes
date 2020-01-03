# GIT-Mistakes

### Change the commit message before pushing it
`git commit --amend -m 'changing the message'`

### logging it in oneline
`git log --oneline`

### Add more files and changes to the same commit before pushing
```
git add -A
git commit --amend -m 'added new files and commited'
```

### Remove files from staging before commiting 
`git reset HEAD lib.js` <br>

### Remove changes from commit before commiting 
get the logs using `git log --oneline`, get the commit hash. 
Then, using `git reset HEAD~1` or `git reset d34fd45` this will put the files back to local.

### use and compare the different git reset options: --hard , --soft. --mixed
* Using soft reset, `git reset --soft HEAD~1`, this will put back those files into staging area(meaning ready to commit).
* Using mixed reset. `git reset --mixed HEAD~1`, this will put back those files into unstaged area(meaning needs to get added to staging).
* Using hard reset. `git reset --hard HEAD~1`, this will git remove the commit, unstaged the changes, remoed from working directory.

### Recover local changes from git reset hard using reflog
* `git reflog` powerfule way to look at the different things in our git repo, get the commit has we want and then,
`git reset --hard 2a5df7d` to get back the files.