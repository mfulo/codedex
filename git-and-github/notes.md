<h1 align="center"> Course: Git & GitHub </h1>

## 03. Git Commands

### Steps to connect remote and local repositories
1. Create remote repo in GitHub
2. Copy repo's HTTPS
3. Open local repo in a code editor of your choice (I'll be using VS Code too)
4. Open VS code terminal
5. Initialize local repo and create a .git in your project folder
   ```
   git init
   ```
6. Add connection to remote repo
   ```
   git remote add origin <repository_url>
   ```
7. Rename the branch where code will be pushed to
   ```
   git branch -M main
   ```
8. Check connectivity between remote and local repos
   ```
   git branch
   ```
   > If you see `main` in the output, you're all set! 👌

<br>

### Problems encountered
After step 8, I didn't see the `main` in the output so I repeated steps 5 and 6, but says `error: remote origin already exists`.
I tried to run the following and it worked:
```
git add .
git commit -m "<message>"
git push origin main
```

<br>

### Upon further research...
These are the right steps:

5. Initialize local repo and create a .git in your project folder
   ```
   git init
   ```
6. Optional step but recommended. Rename local branch to "main"
   ```
   git branch -M main
   ```
   > `-M` means rename/move

   > By default, local branch name is "master"
7. Stage files
   ```
   git add .
   ```
8. Commit files
   ```
   git commit -m "<message>"
   ```
9. Add remote repo
    ```
    git remote add <remote_repo_alias> <repository_url>
    ```
    > ex: git remote add origin https://github.com/user/repo.git
10. Push branch to remote and set upstream
    ```
    git push -u <remote_repo_alias> <local_branch_name>
    ```
    > ex: git push -u origin main
    
    > the adding of `-u` sets the "default shipping address" so you can readily use `git push` or `git pull` next time without specifying the remote and local branch

-----
## 08. Branch Out
Branching is like forking but inside your repository.

To create a new branch
```
git branch <new_branch_name>
```
To switch branches
```
git switch <branch_name>
```
To create and switch to that branch
```
git checkout -b <new_branch_name>
```
-----


