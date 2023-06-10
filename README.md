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


## 6. Relative Refs #1
As you experienced in Chapter 5, we use `git checkout` command with a hash value. Normally, hashes are not that simple values. For example, 5th chapter's hashcode was actually `fed2da64c0efc5243660bdd822f82b54e8cbc5d8`, or something like that you will encounter. Relative references comes in handy in such situations. Instead of typing all the hash value, you can simply use `fed2` in order to indicate the hashcode. Also do not forget, you can still use branch names. 

Now, there is a special character denoted as `^` named "caret operator". This operator provides you to make operations about one parent above of the current selected node. For example, if you type `git checkout main^`, you will checkout the first parent of main and HEAD will point that node. In that way, you do not work with hashcodes. That's great. Also, you can do operations with HEAD reference. In other words, you can travel backwards with `HEAD^`.

You can complete this challenge by using these commands.
```
git checkout bugFix^
```

## 7. Relative Refs #2
In chapter 6, Caret operator (^) was introduced.Actually, almost nothing is different in Tilde operator(~). This time, we can specify the number of how many times we want to go upwards. For example, instead of using 4 Caret operator, we can simply use "~4".


You can complete this challenge by using these commands.
```
git branch -f main C6;
git branch -f bugFix C0;
git checkout C1;
```

## 8. Reversing Changes in Git
`git reset $branchReference$`, reverses changes by moving a branch reference backwards in time to an older commit.

For example, `git reset HEAD^` goes one step back, and acts as the last commit was never there before.



`git revert` TODO







