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

cd ~
git clone your < rpo name >.git
cd demo
nano Hello.java
git status
git add Hello.java
git commit -m "Added Hello.java“
git push origin main


```python
def hello_world():
    print("Hello, World!")
```

