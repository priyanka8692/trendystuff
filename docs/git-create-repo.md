## Creating a git repo

### Creation
1. Create a git repositry.
2. Name it trendystuff.

### Understanding what happens on repo creation
1. A repo named trendystuff is created on github server.
2. A branch named master is created.

### What is difference between repo and branch?
Repo is a place where all of our code is present. This code is present at github server.

Repo is like a tree. A tree has leaves, stem and branches.
stem can also be thought as branch but main branch.
leaves is always present on branches.

In case of repo, code always exists on branch. By default repo needs one branch (similar to tree which needs stem).

So when we create a repo, a branch named master is created by default. Whatever code we push, goes into this master branch.

So pushing changes in a repo means ki pushing changes in its one of the branches

Always think of changes/code as leaves. branch as branch/stem and repo as tree.

### Cloning a repo
Assume that there is a tree in the park. And somehow you have power to make a clone of that tree immediately. So when you went to park for walk, you took a clone of that tree and brought it home. 

So now tree is also present at park and tree is also present at your home.

Similarly git clone is that command/power using which you can clone a repo which is present at github server to your laptop.

Now when we clone the repo, by default code of its main branch which is master comes along with it.

When we create a repo in github server, it creates the repo at github server. But we also need that repo at our laptop for development. So once we create the repo at github server, we clone it using git clone at our laptop.

### Unstage, stage, add, commit, pull and push
So lets say you saw a tree in the park and you took clone of it at your home.
Now you want to add new leaves to the tree at your home.

So you create some leaves separately. Now those leaves are separate and not part of tree. You need to add those leaves to the tree. So currently leaves are separate fom tree means they are unstaged.

Similary when you have some code changes, they are initially unstaged because they are attached to the repo.
