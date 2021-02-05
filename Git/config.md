# Configuration

## Configuring the username and email for commit
In order to be able to commit on remote repositories, you will have to ensure that you configured your username and email address on your git local and have access to the remote repo
1. to check your git configuration run this on your command line either globally or on the specific folder you are working on:`cat .git/config`
2. If you haven't had any git configuration, you can add them globally or locally on the working folder

## Add globally:
1. Add username: on your command line, run: 
```
git config --global user.name "USER_NAME"
```
2. Add email address that you have the access to remote:
```
git config --global user.email "Name.of.email@email.com"
```
## Setup the local folder different from global configuration, remove the `--global`:
1. Add username locally:
```
git config user.name "USER_NAME"
```
2. Set your email address locally
```
git config user.email "Name.of.email@email.com"
```
3. then check if all correct:
```
cat .git/config
```

 
