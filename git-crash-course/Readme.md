## Git Hidden Folder
there is a `.git` hidden folder that tells you that our project is a git repo

if we were to create a new git repo we would create a new project folder and initiliaze that repo using `git init`

```sh
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
code Readme.md
git status
git add Readme.md
# makes changes to it
git commit -m "add readme file"
```
## Cloning
HTTP, SSH, GitHub CLI

1. HTTP
```sh
mkdir workspace/tmp
cd workspace/tmp
```
```sh
git clone https://github.com/Test-Tasos/Github-examples.git
cd Github-examples
```
2. SSH
```sh
git clone git@github.com:Test-Tasos/Github-examples.git
```
we need to generate a ssh-key and copy the code to github https://github.com/settings/ssh/new
```sh
ssh-keygen -t -rsa
cat key.pub
```
we might need to add it
```sh
eval 'ssh-agent
ssh-add key (without the extension)
```
3. Github CLI

install the CLI

## Commits
when we want to commit code git commit will open up the commit code editor of choice
```sh
git commit
```
when we want to commit without opening the code editor
```sh
git commit -m "comment"
```

you will need to create a personal access token (PAT)
https://github.com/settings/tokens and you will use it a s password

## Branches
list of branches
```sh
git branch
```
create a new branch
```sh
git branch name
```
checkout that branch
```sh
git checkout name
```
## Remotes

## Stashing
```sh
git stash save readmechanges 
git stash list
git stash pop
git stash apply (will pop the last one)
```

## Merging

## Add
when we want to stage changes that will be included inm the commit
```sh
git add .
git add Readme.md
```

## Reset
reset allows you to return staged changes back to unstaged
```sh
git add .
git reset
```

## Status
git status will show you which files are or not to be commited
```sh
git status
```
## Gitconfig file
the gitconfig file is what stores your global configurations such as name, email, editor and more
```sh
git config --list
git config --global user.name "John Doe"
git config --global user.email "johndoe@example.com"
```
## Log
git log will show recent commits to the git tree

## Push
when we want to push our local repo to remote repo
