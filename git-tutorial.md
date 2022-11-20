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

Change remote address [[Ref](https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository) ]:  `git remote set-url origin <remote_url>`  

``` 
This is the same as 'git remote rm origin' and 'git remote add origin <remote_url>'  

On the first push you may need to include 'git push --set-upstream origin master'  
```  

To check current remote address:  `git remote -v`  
Note:  Also used to check if 'origin' is the correct remote.  I believe 'origin' is shorthand in git for the remote repo's name.

> For more information about general git operations, review [these instructions for github](./github-class-instructions.md) and [these instructions for gitlab](./gitlab-class-instructions.md).  

General Instructions:
- Do not add an individual file that is more than 100MB.  You can have multiple files that are less than 100MB without causing any issues.
- I would not track changes in git for binary files.  Excel files were formerly binary files (.xls) but more recent versions (.xlsx) are of zipped .xml type.  I would add these files when few or no changes are needed due to the way that git makes full copies of the documents instead of just the changes.  
- Clear jupyter notebook outputs if working with others collaboratively.  The jupyter notebook output cells contain an id key-value pair that often is different for each user who runs the notebook - this causes a merge conflict.  
- When working with a group then it is beneficial to make changes from within a branch.  Even when adding in new features to an existing repo, using a branch can be very beneficial especially when working on multiple features - each feature should have it's own branch.  

View branches and current checked out branch:  `git branch --all`

>  Access to an e-book can be found [here](https://git-scm.com/book/en/v2)

## Issues

[Git will not Remember Credentials on Windows](https://snede.net/git-does-not-remember-username-password/)  

[Authentication Failed - Credential Password Changes](https://stackoverflow.com/questions/47860772/gitlab-remote-http-basic-access-denied-and-fatal-authentication)  

[More about Credential Helpers](https://stackoverflow.com/questions/5343068/is-there-a-way-to-cache-https-credentials-for-pushing-commits)  

[VSCode Terminal Setup](https://www.roboleary.net/vscode/2020/09/15/vscode-git.html)  


## References

[Creating a Github Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) 

[Remote and Origin Meaning](https://stackoverflow.com/questions/38837705/what-is-the-difference-between-origin-and-remote-in-git-commands)

[Repo Setup via Terminal](https://guides.codepath.com/ios/Using-Git-with-Terminal)

[Create .gitignore File](https://www.pluralsight.com/guides/how-to-use-gitignore-file)  

[Make .gitignore Recognize Tracked Files](https://stackoverflow.com/questions/3833561/why-doesnt-git-ignore-my-specified-file).  Note:  solution could be a cache issue or remove issue.

[Git Cheat Sheet with Explanations](https://www.jrebel.com/blog/git-cheat-sheet)  

[Git Key Concepts](https://css-tricks.com/creating-the-perfect-commit-in-git/)  

[How to Write a Commit Message](https://cbea.ms/git-commit/)  

[Git for Team Collaboration](https://medium.com/anne-kerrs-blog/using-git-and-github-for-team-collaboration-e761e7c00281)

[Github Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams)  

[Working as a Team](https://blog.hipolabs.com/how-to-work-in-a-team-version-control-and-git-923dfec2ac3b)  

[How to Fork a Repo](https://docs.github.com/en/enterprise/2.13/user/articles/fork-a-repo#)  

[Delete Remote/Local Branches](https://www.freecodecamp.org/news/how-to-delete-a-git-branch-both-locally-and-remotely/)  

[Revive Deleted Branch](https://intellipaat.com/community/9164/can-i-recover-a-branch-after-its-deletion-in-git)  

[Git Pull](https://www.atlassian.com/git/tutorials/syncing/git-pull)

[Git Merge/Conflict Resolution](https://www.atlassian.com/git/tutorials/using-branches/git-merge#)  

[Tips and Tricks of Github Pages](https://stackoverflow.com/questions/8446218/how-to-see-an-html-page-on-github-as-a-normal-rendered-html-page-to-see-preview)

## Advanced 

[Using Repo Templates](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)

[Creating a Github Package](https://dev.to/dalenguyen/create-your-first-github-package-564f)  

[Splitting Repo - Keeping History](https://medium.com/@ayushya/move-directory-from-one-repository-to-another-preserving-git-history-d210fa049d4b)  

[Handling Project Dependencies](https://webmasters.stackexchange.com/questions/84378/how-can-i-create-a-git-repo-that-contains-several-other-git-repos) and [Merging Repos](https://stackoverflow.com/questions/47559855/git-move-repository-to-a-subfolder-of-another-repository)  

[Example of Git Subtree (Video)](https://www.youtube.com/watch?v=t3Qhon7burE)

[Removing Sensitive Data from Repo](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)  

[Removing a File After Several Good Commits](https://stackoverflow.com/questions/307828/how-do-you-fix-a-bad-merge-and-replay-your-good-commits-onto-a-fixed-merge)  

[Undo Commit or Revert to Last Commit](https://stackoverflow.com/questions/2845731/how-to-uncommit-my-last-commit-in-git)  

[Revert a Single File](https://dev.to/lofiandcode/git-and-github-how-to-revert-a-single-file-dha)  

[Revert Pull Request from Github](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/reverting-a-pull-request)  

## Vague Extras  

Git Msg on Pull similar to:  `fatal: bad object refs/remotes/upstream/main`  
- Solution:  Remove the object referenced in the message via:  
- `rm .git/refs/remotes/upstreams/main`
- `git fetch upstream`  


Git Msg on Merge similar to:  
`fatal: refusing to merge unrelated histories`  
- Solution:  use `--allow-unrelated-histories attribute`  
- [Link](https://www.educative.io/answers/the-fatal-refusing-to-merge-unrelated-histories-git-error)





