
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
