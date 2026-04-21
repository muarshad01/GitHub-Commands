## Install Git on macOS

#### 1 - Install Homebrew
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```
==> Next steps:
- Run these commands in your terminal to add Homebrew to your PATH:
    echo >> /Users/marshad/.zprofile
    echo 'eval "$(/opt/homebrew/bin/brew shellenv zsh)"' >> /Users/marshad/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv zsh)"
- Run brew help to get started
- Further documentation:
    https://docs.brew.sh
```

#### 2 - Install Git
```
$ brew install git
$ brew install git-gui (Optional)
```

#### 3 - Verify the installation
```
$ git --version
```

#### 4 - Open the Built-in Git GUI 
Navigate to your Project: 
```
$ cd /path/to/your/repository
```
Launch the GUI:
```
$ git gui
```
Launch the History Browser: If you want to see a visual tree of your branches and commits, type:
```
$ gitk 
```

***

## Post-Installation Setup
After installing Git, you should configure your identity so your commits are correctly attributed: 

#### Set your name:
```
$ git config --global user.name "Your Name"
```

#### Set your email:
```
$ git config --global user.email "your.email@example.com"
```

#### Check your configuration:
```
$ git config --list
```

***

## Create And Add SSH Keys To Your GitHub Account
```bash
$ ssh-keygen -t rsa
```

```
marshad@marshad-ltml5wv ~ % ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/marshad/.ssh/id_rsa): 
Enter passphrase for "/Users/marshad/.ssh/id_rsa" (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/marshad/.ssh/id_rsa
Your public key has been saved in /Users/marshad/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:ba9OHFau8C8wPXFp2DxF9RBaEGXTky1O3M2tf/pEyYk marshad@marshad-ltml5wv.internal.salesforce.com
The key's randomart image is:
+---[RSA 3072]----+
|            o*O**|
|             +==O|
|           +o= oo|
|         .ooB = o|
|        S.=+.E =.|
|        o*o+   .o|
|         o=..  .o|
|         ..o  .. |
|         .o..  ..|
+----[SHA256]-----+
marshad@marshad-ltml5wv ~ %
```

#### Copy and Add to GitHub Account
```
$ pbcopy < ~/.ssh/id_rsa.pub
```

#### ssh-add privagte key
```
$ eval $(ssh-agent -s)
$ ssh-add -k ~/.ssh/id_rsa
```

***


## Error and Fix

```
$ git@github.com:muarshad01/GitHub-Commands.git
```

```
marshad@marshad-ltml5wv Desktop % git clone git@github.com:muarshad01/GitHub-Commands.git
Cloning into 'GitHub-Commands'...
The authenticity of host 'github.com (100.64.1.8)' can't be established.
ED25519 key fingerprint is: SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
Host key verification failed.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
marshad@marshad-ltml5wv Desktop %
```

#### Fix
```
$ ssh-keyscan github.com >> ~/.ssh/known_hosts
```

***

## Useful Commands
* [Git Cheat Sheet](https://amanchadha.com/projects/cheatsheets/Git_Cheatsheet_AmanChadha.pdf)
* [Create a new branch with git and manage branches](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches)
* [Merging vs. rebasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)

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

## set-branches
```
$ git remote set-branches --add origin 't/tpil/coding-in-core/fy25q1/*'
$ git fetch
```

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

***

## Course
* [Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk)

***

## Learn Git Branching

[Learn Git Branching](https://learngitbranching.js.org)

***
