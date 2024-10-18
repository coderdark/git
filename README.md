# git commands

- Working directory is directory that contains the files of your project
- Staging area (index, file)
- Repo is the .git directory

Creating a git repo

```git init```

Finding your .git repo in your working directory

```find .git```

Checking the status of the working directory 

```git status```

View the logs with one line (you can view the SHA for each commit)

```git log --oneline```

View the logs of a specific branch with one line (you can view the SHA for each commit)

```git log --oneline <branch_name>```

View the logs with one line and graph (you can view the SHA for each commit)

```git log --oneline --graph```

Adding a file or all files (then . means all files) to the staging area

```git add <file_name>``` or ```git add .```

Commiting your file changes to the git repo

```git commit -m 'message for your commit'```

To undo a file added to the staging area

```git reset <file_name>```

To checkout (change) an existent branch

```git checkout <branch_name>```

Create and checkout a branch

```git checkout -b <branch_name>```

To merge a branch (feature) to another branch (main)

```git merge <branch_name>```

Merge Example:
  + Checkout `main` branch first ```git checkout main```
  + Then ```git merge feature```

To rebase a branch (feature) with another branch (main)

```git rebase <branch_name>```

                        C2 <- C4 (feature)
            C0 <- C1 <- C2 <- C3 <- C5 (main)

            C0 <- C1 <- C2 <- C3 <- C4 (feature after rebase)

Rebase Example:
  + Checkout `feature` branch first ```git checkout feature```
  + Then ```git rebase main```

Adding a remote to your local repo (usual <name> is origin

```git remote add <name> <local_path/uri>```

To fetch the remote repo state to your local repo

```git fetch```

Getting the files from the remote repo. Pull fetches the changes and then it merges them to the local.

```git pull <remote> <branch>```

Sending the files from the local repo. Push fetches the changes and then it merges them to the remote.

```git push```





