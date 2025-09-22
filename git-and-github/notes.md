<h1 align="center"> Course: Git & GitHub </h1>

## Table of contents
- [03. Git Commands](#03-git-commands)
- [08. Branch Out](#08-branch-out)
- [10. Merges](#10-merges)

<br>

-----
## 03. Git Commands

### 📚 Steps to connect remote and local repositories
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

### 😱 Problem encountered
After step 8, I didn't see the `main` in the output so I repeated steps 5 and 6, but says `error: remote origin already exists`.
I tried to run the following and it worked:
   ```
   git add .
   git commit -m "<message>"
   git push origin main
   ```

<br>

### 🧐 Upon further research...
These are the right steps:

Repeat steps 1-4 above.

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

[^](#table-of-contents)

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
   > or: git checkout <branch_name>

To create and switch to that branch
   ```
   git checkout -b <new_branch_name>
   ```
   > or: git switch -c <branch_name>
   
[^](#table-of-contents)

-----
## 10. Merges

Merging is taking changes from branch_A to your current branch
   ```
   git merge <branch_A>
   ```

<br>

✅ Best practice to merge changes when working in a team: 
> assuming your team is using remote and you're working locally

1. Switch to main
   ```
   git switch main
   ```
2. Make sure your local main is up to date with remote main
   ```
   git pull origin main
   ```
   > git pull = git fetch + git merge
   
3. Merge your feature branch to main
   ```
   git merge <feature_branch>
   ```
4. Update remote main with local main
   ```
   git push origin main
   ```
[^](#table-of-contents)

-----
