# Git Commands

For more info in each of the commands you can use the manual ```man```  for each of the commands below.
Example: ```man git```
To search in the manual, make sure you are in search mode (:) and enter /<the_term_you_are_searching_for>.  To navigate between finds, press N to move forward, Shift + N to move backwards.

Terms
- Working directory is directory that contains the files of your project
- Staging area (index, file)
- Repo is the .git directory
- Untracked files are files that git does not control
- Staged files are files that are added to the staging area with the git add but not commit it yet
- Commited files are files that were in the stage area and commited with git commit command

| Description                                                                                                  | Command                                                                   |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------- |
| Creating a git repo                                                                                          | ```git init```                                                            |
| Finding your .git repo in your working directory                                                             | ```find .git```                                                           |
| Checking the status of the working directory                                                                 | ```git status```                                                          |
| View the logs with one line (you can view the SHA for each commit)                                           | ```git log --oneline```                                                   |
| View the logs of a specific branch with one line (you can view the SHA for each commit)                      | ```git log --oneline <branch_name>```                                     |
| View the logs with one line and graph (you can view the SHA for each commit)                                 | ```git log --oneline --graph```                                           |
| Adding a file or all files (then . means all files) to the staging area                                      | ```git add <file_name>``` or ```git add .```                              |
| Stashing file (temporary)                                                                                    | ```git stash -m <message>```                                              |
| Commiting your file changes to the staging area                                                              | ```git commit -m 'message for your commit'```                             |
| Adding and commiting your changes to staging area                                                            | ```git commit -am 'message for your commit'```                             |
| To undo changes to a file in working directory (not staged)                                                  | ```git restore <file_name>```                                             |
| To undo changes to a file in the staging area (flags, mixed, soft and hard) mixed default                    | ```git restore --staged <file_name>```                                    |
| To undo a commit, get the previous id before your commit (get ids by typing `git log --oneline`              | ```git reset <previous_commit_id>```                                      |
| Remove all working directory changes (all files)                                                             | ```git checkout .```                                                      |
| Remove all working directory changes (all files)                                                             | ```git checkout HEAD .```                                                 |
| To checkout (change) an existent branch                                                                      | ```git checkout <branch_name>```                                          |
| Create and checkout a branch                                                                                 | ```git checkout -b <branch_name>```                                       |
| To merge a branch (feature) to another branch (main)                                                         | ```git merge <branch_name>```  see example below...                       |
| To rebase a branch (feature) with another branch (main)                                                      | ```git rebase <branch_name>``` see example below...                       |
| Adding a remote to your local repo (usual <name> is origin                                                   | ```git remote add <name> <local_path/uri>```                              |
| To fetch the remote repo state to your local repo                                                            | ```git fetch```                                                           |
| Getting the files from the remote repo. Pull fetches the changes and then it merges them to the local.       | ```git pull <remote> <branch>```                                          |
| Sending the files from the local repo. Push fetches the changes and then it merges them to the remote.       | ```git push```                                                            |

Merge Example:
 + Checkout `main` branch first ```git checkout main``` 
 + Then ```git merge feature```

   
Rebase Example:

                    C2 <- C4 (feature)
            C0 <- C1 <- C2 <- C3 <- C5 (main)

            C0 <- C1 <- C2 <- C3 <- C4 (feature after rebase)

  + Checkout `feature` branch first ```git checkout feature```
  + Then ```git rebase main```





