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

### Unstage, stage, add, commit
So lets say you saw a tree in the park and you took clone of it at your home.
Now you want to add new leaves to the tree at your home.

So you create some leaves separately. Now those leaves are separate and not part of tree. You need to add those leaves to the tree. So currently leaves are separate fom tree means they are unstaged.

Similary when you have some code changes, they are initially unstaged because they are not attached to the repo.

Now those leaves which are not yet part of tree, we attached it to tree by fevicol. Now they are attached to the tree but attached via fevicol. i mean ki tree doesn't consider those leaves at its own. Tree will not send any water/food to those leaves because they are attached using fevicol.

Similarly unstaged code changes are attached to repo using git add command. But git add command means ki they are attached to repo but not part of it. Attached code changes are called as staged.

Now with time, tree will consider those leaves as its own. this happens really. In actual life also, if we attach some leave to the tree, there are chances that tree will integrate with that leave.

Similary in code changes, we can integrate the staged changes with repo using git commit command.

So in summary
1. by default, changes are unstaged (i.e. not attached to repo)
2. git add command stage the changes. i.e changes are attached to repo but repo doesnt consider changes as its own.
3. git commit command integrates staged changes to repo. i.e. changes are now part of repo.

### push command
Now when we commited the code, code became part of repo. But this repo is the repo of your laptop. (i mean ki you integrated new leaves to tree at your home).

But you need these new leaves at park wala tree also. Currently park wala tree doesnt have those leavces but your home wala tree has those leaves.

So we go to the park, compare that what my home tree has but park tree doesnt. You take a copy of those leaves from your home tree and paste to the park tree.

This process is done using git push command.
git commit integrated changes to your local repo (i.e. repo at your desktop). But I need to update these changes to my remote repo (github server repo) also.

So I want to make changes in remote repo also. So we use git push command which finds that what is extra in local repo which remote repo doesnt have. Those extra commits are sent/pushed to remote repo.
Thus by git push command, those commits also go to remote repo.

### pull command
We cloned/copied home tree from park tree. We are making new changes in local tree, commiting them and sending those changes to park tree. Everything is going alright.

But something wierd happens now. Some other guy named ak also took a clone of park tree to his home. He added some changes in its home tree and pushed those changes in park tree.

Now park tree has some changes which you home tree doesnt have. Now when I am making some changes in my home tree and pushing them to park tree, park tree will reject it. It will say there is some issue. I have something additional from some other source. If you need to add some changes in me, you need to first take changes from me and then add changes in me.

We can take park tree new changes using git pull command. Then we can do push

### How to push
So general rule is that:
1. If you dont have local repo, use git clone to clone remote repo locally.
2. make some changes in the repo. By default they will be unstaged i.e. unattached.
3. use git add to add those changes in repo. But it will just attach the changes to repo but not integrate it.
4. use git commit command to commit/integrate those changes to the local repo.
5. use git pull to take changes from remote repo.
6. use git push to push you changes to remote repo.

### What is branch and how to create new branches
So in your local home tree, you add leaves to the tree. But where you are addind the leaves?
Leaves are always added to a branch. But we haven't talked till now about branch.

By default when you add leaves to a tree but doesnt tell where to add it. it adds it to its main branch which is stem.

Similary in code, when we dont mention where to add the changes, be default it adds it in its main branch which is master.

So be default everything gets added to the master branch.

Now if you want to create a new branch in your home tree, use "git checkout -b newBranchName" command. i.e. running command git checkout -b branch1 adds branch1 branch to the home tree.

branch includes its own leaves and leaves of stem also. This is because branch is always considered from root.

Lets say that stem is 3 meter in length. But branch1 branch is starting from 1 meter length of stem. So in this case, will stem leaves from 1 meter to 3 meter be part of branch1? No.
But stem leaves within 1 meter will be part of branch1.

So we create new branch using git checkout -b branchName command. That branch will contain master branch code also as branch starts from root. But it will not contain that master code which is added after creating the branch.

For now lets stick on master branch only.
With every command, we need to know for which branch we are working on.
Go for git push, if we are pushing changes in master branch we need to mention the branch.
i.e. git push origin master Here origin is the name of park where the tree is.
So by above command we are saying that these new leaves which are integrated in my local tree, send these changes to the tree at park named origin and in that tree the changes will go to master branch.

By default we do only git push. git push command automcatically understands that as nothing is given means i have to go to park named origin and make changes in master branch.

### Commiting directly in remote repo
Lets say you decide ki i will not make leaves at my home and then add it in my locla tree. Then integrate it in my local tree and then push those new leaves to park tree.

Instead, I want to directly add new leaves in park tree.

So, I can just go to the park. Create new leaves right there. Add those leaves to the tree. Integrate those leaves. Here as integration is happening directly at park tree, I dont need to push these changes anywhere.

So, we can directly go to github server. Edit any file. Commit that file and done. No need to push as changes are directly happening in remote repo.