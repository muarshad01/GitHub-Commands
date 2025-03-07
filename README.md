
## Useful Links

* [Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk)
* [Create a new branch with git and manage branches](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches)
* [Git Cheat Sheet](https://amanchadha.com/projects/cheatsheets/Git_Cheatsheet_AmanChadha.pdf)

***

## Learn Git Branching

[Learn Git Branching](https://learngitbranching.js.org)

***

# Create And Add SSH Keys To Your GitHub Account

[Create And Add SSH Keys To Your GitHub](https://www.youtube.com/watch?v=itU8KBuE8jk)

## ssh-keygen

```
$ ssh-keygen
```

```
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/user/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /Users/user/.ssh/id_rsa.
Your public key has been saved in /Users/user/.ssh/id_rsa.pub.
...
```

```
$ cd /Users/XYZ/.ssh/              # MacOS
$ cd \Users\XYZ\.ssh/              # Windows
```
* This folder will have a key-pair (id_rsa, id_rsa.pub)
* Goto `https://github.com/user-id` -> `Settings` -> `SSH and GPG Keys` -> Add new SSH Key

```
$ ssh-add -k ~/.ssh/id_rsa_laptop
```

***

## Commands

```
$ git remove
$ git remote -v

$ git checkout -b <new-branch-name>                   # create a new-branch and switch to it
$ git push --set-upstream origin <new-branch-name>

$ git branch                                  # shows ALL branches
$ git checkout <branch-name>                  # switch to <branch-name>
$ git branch                                  # shows ALL branches
$ git push --set-upstream origin chap16
```

## Set `user.name` and `user.email`

```
vim ~/.gitconfig

$ git config --global user.name "abc"
$ git config --global user.email "xyz@pqr.com"

$ git config --list

$ git config --global user.name
$ git config --global user.email

$ git config --global --remove-section user
$ cat ~/.gitconfig
```

## set-branches
```
$ git remote set-branches --add origin 't/tpil/coding-in-core/fy25q1/*'
$ git fetch
```
***

* [Merging vs. rebasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)

***

```
$ mkdir tmp && cd tmp
$ git clone git clone git@git.soma.salesforce.com:marshad/monitor-perfswat.git
$ git remote -v
-- origin	git@git.soma.salesforce.com:marshad/monitor-perfswat.git (fetch)
-- origin	git@git.soma.salesforce.com:marshad/monitor-perfswat.git (push)
$ git remote add perfswat git@git.soma.salesforce.com:perfeng-platform-core/monitor-perfswat.git
-- origin	git@git.soma.salesforce.com:marshad/monitor-perfswat.git (fetch)
-- origin	git@git.soma.salesforce.com:marshad/monitor-perfswat.git (push)
-- perfswat	git@git.soma.salesforce.com:perfeng-platform-core/monitor-perfswat.git (fetch)
-- perfswat	git@git.soma.salesforce.com:perfeng-platform-core/monitor-perfswat.git (push)
$ git fetch perfswat
$ git checkout api_huron
$ git branch
$ git push origin api_huron
```
