# git-tutorial  

Basic Configuration:
- `git config --global user.name "<first last name>"`  
- `git config --global user.email "<email>"`
- `git config --global color.ui true`
- `git config --list`  

Add local repo to github  
- Initialize local folder:  `git init -b main`  
- Prep for push:  `git add . && git commit -m "<add message>"`  
- Push to remote address:  `git remote add origin <remote url>`
- Verify address:  `git remote -v`  
- Push new files/updates:  `git push origin main`

Check status: `git status`  

Common remote updates:  
- `git add .`   
- `git commit -m "<message>"`  
- `git push origin main`  

Common local updates:  
- `git pull origin <branch>`  

Update local and review merge conflicts:
- `git stash`
- `git pull origin <branch>`
- `git stash pop`
- Review conflicts and save files with final edits.  Add and Commit changes to complete merge.  This is a similar process as if we had already committed changes to the repo and then pulled - we would need to resolve conflicts before the merge would complete.   

Change remote address:  `git remote set-url origin <remote_url>`  

> For more information about general git operations, review [these instructions for github](./github-class-instructions.md) and [these instructions for gitlab](./gitlab-class-instructions.md).  

General Instructions:
- Do not add an individual file that is more than 100MB.  You can have multiple files that are less than 100MB without causing any issues.
- I would not track changes in git for binary files.  Excel files were formerly binary files (.xls) but more recent versions (.xlsx) are of zipped .xml type.  I would add these files when few or no changes are needed due to the way that git makes full copies of the documents instead of just the changes.  
- Clear jupyter notebook outputs if working with others collaboratively.  The jupyter notebook output cells contain an id key-value pair that often is different for each user who runs the notebook - this causes a merge conflict.  
- When working with a group then it is beneficial to make changes from within a branch.  Even when adding in new features to an existing repo, using a branch can be very beneficial especially when working on multiple features - each feature should have it's own branch.  

View branches and current checked out branch:  `git branch --all`




## References

[Creating a Github Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) 

[How to Write a Commit Message](https://cbea.ms/git-commit/)

[Github Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams)
[Working as a Team](https://blog.hipolabs.com/how-to-work-in-a-team-version-control-and-git-923dfec2ac3b)
[How to Fork a Repo](https://docs.github.com/en/enterprise/2.13/user/articles/fork-a-repo#)



