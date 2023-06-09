# Learn-Git-Branching
In this repository, I solve challenges in https://learngitbranching.js.org and take some personal notes. Here are my notes so that you either use it as a quick-hand book or learn commands without stressing yourself in challanges 😀, enjoy!

## 1. Introduction to Git Commits
`git commit` : This command is the most popular git command as far as I know. With this command, you are simply logging that you made a change into the log system. You can use -m flag with a message.

```
git commit -m "Hey, this is my first commit!"
```

You can complete this challenge if you use git commit command twice.
```
git commit;
git commit;
```

## 2. Git Branches
`git branch $branchName$`  This command creates a branch so that you can do you work this path without affecting main work. You can name your branch anything you want.

`git checkout $branchName$`  This command simply SELECTS your branch. That is the purpose so that you would not make changes for another branches (such as main branch, unintentionally 😁).

Main thing here is when you create a branch, you are not going to be SELECT IT AUTOMATICALLY. If you want to checkout a branch when it is created you can use -b flag in git checkout command

```
git checkout -b MyNewBranch;
```

You can complete this challenge with the help of this flag in one line. Yikes!

```
git checkout -b bugFix;
```

## 3. Branches and Merging
`git merge $branchName$` This command merges branches. One branch is what you write its name as a parameter, and the other one is in checkout (This could be wrong irl, but in game it works in that way. If this is false, please let me know). Also, if you are going to merge two branches where one is parent and other is child, git automatically merges onto the parent.


You can complete this challenge by using these commands in order.
```
git checkout -b bugFix;
git commit;
git checkout main;
git commit;
git merge bugFix;

```

## 4. Rebase Introduction
`git rebase $branchName$` This command is also merging branches. The difference is you simply create a copy of that branch and add to the other branch's beneath. However, this command should be used carefully IRL.

You can complete this challenge by using these commands in order.
```
git checkout -b bugFix;
git commit;
git checkout main;
git commit;
git checkout bugFix;
git rebase main;
```

## 5. Moving around in Git
**HEAD** : HEAD as far as I understand, is a pointer to the node. It can be used with node's hash value. Back then, we use `git checkout` command with branch names, but in this case we use hash values of nodes. 


You can complete this challenge by using this command
`git checkout C4`


## 6. Relative Refs
TO BE CONTINUE
