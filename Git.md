
  1. Add  a README file
  2. Add .gitignore
  3. Choose a licence
  4. Click create repo


## Git commands 
1. git add
2. git commit 
3. git push


## To setup git to work with GitHub
1. Git config --global user.name "your git id"
2. git config --global user.email "your email_id"

## To genrate Token
1. Log in to GitHub
2. Click on your profile icon (top-right corner)
3. Select Settings
4. In the left sidebar, click Developer settings
5. Click Personal access tokens
6. Select Tokens (classic) or Fine-grained tokens
7. Click Generate new token
8. Enter a token name (description)
9. Set the expiration period
10. Select required permissions (scopes) such as repo
11. Click Generate token
12. Copy and store the token immediately (it will not be shown again)
13. Use this PAT instead of your GitHub password when performing operations like git push

## On local machine Git Ternimal

```
cd ~
git clone your https://github.com/Your_UID/demo.git
cd demo
nano Hello.java
git status
git add Hello.java
git commit -m "Added Hello.java“
git push origin main
```

## Miscellaneous Git Commands

| Command       | Purpose                             | Example              |
| ------------- | ----------------------------------- | -------------------- |
| git status    | Show current state of repository    | git status           |
| git log       | Show commit history                 | git log              |
| git diff      | Show differences between files      | git diff             |
| git pull      | Fetch and merge updates from remote | git pull origin main |
| git fetch     | Download changes without merging    | git fetch origin     |
| git remote -v | Show remote repositories            | git remote -v        |
| git reset     | Undo staging or commits             | git reset file1.txt  |
| git rm        | Remove a file from repository       | git rm file1.txt     |
| git stash     | Temporarily save changes            | git stash            |
| git stash pop | Restore stashed changes             | git stash pop        |


## Branching and Mearging 

1. Create a New repo
   
```
cd ~ 
git clone https://github.com/Your_UID/Name_of your repo.git
cd Repo_name
vim hello.py
git add .
git commit -m "give comment"
git push origin main
```

Create branches

```
git checkout -b d-1
git checkout -b d-2
```

### For Dev 1
```
git checkout d-1
vim hello.py   #Edit the line and add a line
git add hello.py
git commit -m "Developer-1 hello.py"
```

### For Dev 2

```
git checkout d-2
vim hello.py   #Edit the line and add a line 
git add hello.py
git commit -m "Developer-2 hello.py"
```


### Try to merge d-1 and d-2 branch it give error

```git merge d-1```

resolve the conflict 

```vim hello.py``` 

again add and commit

```
git add hello.py
git commit-m "Conflict handel"
git merge d-1
```

### switch to main and merge branch 2
```
git checkout main
git merge d-2
git push origin main
```

| Command                              | Purpose                                      | Example                           |
| ------------------------------------ | -------------------------------------------- | --------------------------------- |
| git branch                           | List all branches in the repository          | git branch                        |
| git branch branch_name               | Create a new branch                          | git branch feature1               |
| git checkout branch_name             | Switch to an existing branch                 | git checkout feature1             |
| git checkout -b branch_name          | Create and switch to a new branch            | git checkout -b feature2          |
| git merge branch_name                | Merge another branch into the current branch | git merge feature1                |
| git branch -d branch_name            | Delete a local branch                        | git branch -d feature1            |
| git push origin branch_name          | Push a branch to remote repository           | git push origin feature1          |
| git push origin --delete branch_name | Delete a remote branch                       | git push origin --delete feature1 |


| Command                              | Purpose                                      | Example                           |
| ------------------------------------ | -------------------------------------------- | --------------------------------- |
| git branch                           | List all branches in the repository          | git branch                        |
| git branch branch_name               | Create a new branch                          | git branch feature1               |
| git checkout branch_name             | Switch to an existing branch                 | git checkout feature1             |
| git checkout -b branch_name          | Create and switch to a new branch            | git checkout -b feature2          |
| git merge branch_name                | Merge another branch into the current branch | git merge feature1                |
| git branch -d branch_name            | Delete a local branch                        | git branch -d feature1            |
| git push origin branch_name          | Push a branch to remote repository           | git push origin feature1          |
| git push origin --delete branch_name | Delete a remote branch                       | git push origin --delete feature1 |

### Alternative: switch Command

| Command                       | Purpose                                                       | Example                     |
| ----------------------------- | ------------------------------------------------------------- | --------------------------- |
| git switch branch_name        | Switch to an existing branch (modern alternative to checkout) | git switch feature1         |
| git switch -c branch_name     | Create a new branch and switch to it                          | git switch -c feature2      |
| git switch main               | Switch back to the main branch                                | git switch main             |
| git switch -                  | Switch to the previously used branch                          | git switch -                |
| git switch --detach commit_id | Switch to a specific commit (detached HEAD state)             | git switch --detach a1b2c3d |

