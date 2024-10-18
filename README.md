# git commands

Creating a git repo

```git init```

Checking the status of the working directory 

```git status```

View the logs with one line (you can view the SHA for each commit)

```git log --oneline```

Adding a file or all files (then . means all files) to the staging area

```git add <file_name>``` or ```git add .```

Commiting your file changes to the git repo

```git commit -m 'message for your commit'```

To checkout (change) an existent branch

```git checkout <branch_name>```

Create and checkout a branch

```git checkout -b <branch_name>```

To merge a branch (feature) to another branch (main)

```git merge <branch_name>```

Merge Example:
  + Checkout `main` branch first ```git checkout main```
  + Then ```git merge feature```

