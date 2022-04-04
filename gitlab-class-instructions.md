# GitLab  
I will update this page occasionally with some common procedures and I will reference locations where you will find more detailed instructions for handling git error messages and less frequently needed tasks.  


<details>
<summary>Tips for Managing Your GitLab Repo</summary>

I will refer to the `ClassRepo` as the folder that contains your actual GitLab repo.  I believe we created a folder like this when we cloned the repo.


1. Do not put one repo inside of another. Doing so creates annoying and difficult problems that can easily be prevented.
1. Do not put your homework repos inside of the `ClassRepo` (see above).
1. Do not put more than one homework assignment in a single repo. 
1. Do not try to `git add`, `git commit`, or `git push` from the `ClassRepo`. You don't have sufficient privileges to push content to GitLab anyway, and these commands will leave your `ClassRepo` in a state where you can't get new content.
</details>

<details>
<summary>How to Update Your Local Copy of the Class Repo</summary>

1. Open the `ClassRepo` folder.
1. Right-click on the `Repo Folder that Matches the GitLab Repo` folder and then open a Git Bash (Windows) or Terminal (Mac).
1. Run `git pull origin main` to pull the new files from GitLab for that week.
</details>

<details>
<summary>Git Pull Fails Due to File Conflict</summary>

![Pull Failed](./images/main-page/merge-conflict-gitlab/merge_conflict.jpg)  
This error occurs occasionally.  Here's the scenario - you have pulled files and modified one or more of them.  I then upload changes to that specific file to GitLab.  When you pull, your `git` realizes that the copy it has doesn't match the file from the remote and doesn't know which one has the correct information.  
What you can do is `stash` your files and look at the incoming updates.  Then if you want you can merge your files with the new files provided.
1. Open the `ClassRepo` folder.
1. Right-click the `Repo Folder that Matches the GitLab Repo` folder and then open a Git Bash (Windows) or Terminal (Mac).
1. Run `git stash` to stash any changes you may have made in previous lessons.  This is like hiding a copy in the background.
1. Run `git pull` to pull the new files from GitLab for that week.  At this point you can go back and review the changed files so see if your changes need to be included.
1. If you want your changes included in the files then Run `git stash pop` to merge your edits with the new edits. 
1.  When you look at the changes to the files you wil see both edits and you can modify the file to get it to its desired format/content then remember to save it.
![Pull Fixed](./images/main-page/merge-conflict-gitlab/git_pop_merge.jpg) 
1. Check to make sure you have the activities for that week. If you have any issues, ask a TA.   
## Deleted Files by Accident
There are several ways to bring back files.  The method largely depends on several factors - were you working with branches, were you working collaboratively with a group, what you have done since you deleted them, etc...  
1.  **Method 1**:  This is probably the easiest check and least likely to cause bigger problems.  In terminal, run `git status`.  There is a chance that this will list the files that have been mofidied and deleted.  The instructions on the page will describe how to undo the deletion.  Usually you run `git restore <filepath/filename>`  
![Deleted Files Fixed](./images/main-page/merge-conflict-gitlab/deleted_files_restore.jpg)
1.  **Method 2**:  To reset **everything** to the status of the previous pull, then run `git reset --hard HEAD`
![Deleted Files Fixed](./images/main-page/merge-conflict-gitlab/deleted_files_reset.jpg)  
</details>
