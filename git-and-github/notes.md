<h1 align="center"> Course: Git & GitHub </h1>

## 03. Git Commands

### Steps to connect remote and local repositories
1. Create remote repo in GitHub
2. Copy repo's HTTPS
3. Open local repo in a code editor of your choice (I'll be using VS Code too)
4. Open VS code terminal
5. Run this to initialize local repo and create a .git in your project folder
   ```
   git init
6. Run this to add connection to remote repo
   ```
   git remote add origin <repository_url>
7. Run this to rename the branch where code will be pushed to
   ```
   git branch -M main
8. Run this to check connectivity between remote and local repos
   ```
   git branch
   ```
   > If you see ```main``` in the output, you're all set! 👌

<br>

### Problems encountered
After step 8, I didn't see the ```main``` in the output so I repeated steps 5 and 6, but says ```error: remote origin already exists```.
I tried to run the following and it worked:
```
git reset
git add .
git commit -m "<message>"
git push origin main
```

-----


