## Optionally select:
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
Log in to GitHub
Click on your profile icon (top-right corner)
Select Settings
In the left sidebar, click Developer settings
Click Personal access tokens
Select Tokens (classic) or Fine-grained tokens
Click Generate new token
Enter a token name (description)
Set the expiration period
Select required permissions (scopes) such as repo
Click Generate token
Copy and store the token immediately (it will not be shown again)
Use this PAT instead of your GitHub password when performing operations like git push

## On local machine Git Ternimal

cd ~
git clone your < git rpo name >.git
cd demo
nano Hello.java
git status
git add Hello.java
git commit -m "Added Hello.java“
git push origin main



