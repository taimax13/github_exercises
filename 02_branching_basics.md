## Create New Branch

In this exercise, you are going to create a new branch in your git directory. A branch is a copy of the `main` branch. You can make edits to this copy without changing the `main` branch. Professional developers use branches to develop new features outside of the `main` git history so that they can perfect their work before merging it into the `main` branch. A common workflow is to create a new branch from the `main`, write and test your new code, merge the completed code into the `main`, and then delete the feature branch.

Create a new branch called `from _itc`. Enter in your terminal the command `git checkout -b from_itc`. The `checkout`command is how you switch between locations in git, `-b` is for making a new branch, and `from_itc` is the name of the new branch.

```shell
>>> git checkout -b from_itc

# output
Switched to a new branch 'from_itc'
```

If you run the same command again, you'll get a message saying the branch already exists.

```shell
>>> git checkout -b from_itc

# output
fatal: A branch named 'from_itc' already exists.
```

To switch from the `from_itc` branch back to `main`, enter `git checkout main`. To switch from `main` to `from_itc`, enter `git checkout from_itc`. Each time you switch, your terminal should message you something like the following.

```
# output in terminal
Switched to branch 'from_itc'
Your branch is up to date with 'origin/from_itc'.
```

To see a list of your branches and which branch you're on, enter `git branch`.

```
>>> git branch

# output
* from_itc
  main
```

Make sure you're in the `from_itc` branch. `git checkout from_itc`. Type `ls` to see a list of the contents. What is in your folder?

Now clone this repository using `git clone`.

```
>>> git clone <https for repo you're cloning>

#output
Cloning into 'github_exercises'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 12 (delta 3), reused 11 (delta 2), pack-reused 0
Unpacking objects: 100% (12/12), done.
```

Type `ls` to see a list of the contents. Do you see the cloned repo? What else is in your folder?

Change directories into the folder for the repository you just cloned. Look at the list of all contents using `ls -al`. You should see a `.git` folder. This is the local git history for the cloned repo. If you were going to contribute code to the repo you're cloning, you would work with the cloned repo's git history. However, in this exercise, you are not contributing code to the cloned repo. Instead, you're just copying the code. So, you should delete the clone repo's git history. Deleting a git history is not something you should do lightly because it deletes the entire history from that folder. After deleting it, type `ls -al` to confirm it's gone.

If you don't delete the cloned repo's git history, you will get a warning message like the following:

```
hint: You've added another git repository inside your current repository.
hint: Clones of the outer repository will not contain the contents of
hint: the embedded repository and will not know how to obtain it.
hint: If you meant to add a submodule, use:
hint:
hint:   git submodule add <url> github_exercises
hint:
hint: If you added this path by mistake, you can remove it from the
hint: index with:
hint:
hint:   git rm --cached github_exercises
hint:
hint: See "git help submodule" for more information.
```

In the warning message, the "another git repository inside your current repository" is the cloned repo's git history. If you delete the cloned repo's git history, this warning message disappears.

## Push the Branch

You can change directories up one folder using `cd ..`. Change from the cloned repository folder up one to your project's folder. Type `ls` to see the folder contents.

It's time to push your branch to GitHub. Check the status `git status`. You should see some red untracked files. Track them by adding them to the staging area `git add -A`. Then commit them `git commit -m "cloned from itc"`. Then push `git push`. You might get a terminal message `git push --set-upstream origin from_itc`. Copy that and enter it in your terminal.

You should see in your terminal:

```
On branch from_itc
Your branch is up to date with 'origin/from_itc'.

nothing to commit, working tree clean
```

Now switch from the `from_itc` branch to the `main` branch by entering in your terminal `git checkout main`. Your folders in VS Code should change to the `main` branch. Look at your folders. The cloned repo folder should be missing from your `main` branch.

You should now merge the `from_itc` branch into the `main` branch. Enter in the terminal `git merge from_itc`. In your terminal, you should see something like:

```
Updating 22e99f0..761baee
Fast-forward
 gitHubCommands.js                       |   1 +
 github_exercises/.DS_Store              | Bin 0 -> 6148 bytes
 github_exercises/01_getting_started.md  | 175 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 github_exercises/02_branching_basics.md |  42 +++++++++++++++++++++++++++
 github_exercises/03_pull_request.md     |   3 ++
 github_exercises/04_clone_project.md    |  13 +++++++++
 6 files changed, 234 insertions(+)
 create mode 100644 github_exercises/.DS_Store
 create mode 100644 github_exercises/01_getting_started.md
 create mode 100644 github_exercises/02_branching_basics.md
 create mode 100644 github_exercises/03_pull_request.md
 create mode 100644 github_exercises/04_clone_project.md
```

Also, look at your folders in VS Code. The folder for the repository that you cloned into the `from_itc` branch should now appear in `main`. In your terminal, type `git branch`. It should indicate that you're in the `main` branch.

Now you need to stage and commit your changes to the `main` branch. Then push your commits to GitHub.

```
git add -A

git commit -m 'merged with definitions'

git push
```

## Add definitions to js file

Create a new branch called `definitions`. While in the `definitions` branch, add the code below to your gitHubCommands.js file.

```js
// git add
const gitAdd = "";

// git commit
const gitCommit = "";

// git status
const gitStatus = "";

// git push
const gitPush = "";

// git merge
const gitMerge = "";

// git checkout
const gitCheckout = "";

// git branch
const gitBranch = "";

// git clone
const gitClone = "";

// git pull
const gitPull = "";

// git remote
const gitRemote = "";
```

Don't yet add actual definitions. Push your changes to the `definitions` branch. Then merge the `definitions` branch into the `main` branch. Next stage and commit the change to `main`. Finally, push the `main` to GitHub.

When merging two branches, the branches might have a conflict. A conflict occurs when two branches have edits for the same file that interfere with one another. You can't make both edits because making one of the edits means you can't make the other.

To see what it's like to have a conflict, create a `revised-definitions` branch.

While on your `revised-definitions` branch, in your gitHubCommands.js file, add definitions to to each variable inside the quotation marks. Stage, commit, and push your changes to `revised-definitions`.

Checkout the `main` branch.

In your gitHubCommands.js file, assuming you don't already have the exact definition, change the definition for `gitRemote` to `const gitRemote = "manage remote git (GitHub)";`. When you try to save your file in VS Code, VS Code may give you an error message saying you have a conflict between files. Fix the conflict. Then merge `revised-definitions` to `master`. Then, stage, commit, and push to `master`.

If you don't see an error from VS Code when trying to save, go ahead and merge `revised-definitions` to `main`. If you still don't see a merge conflict. Stage and commit your changes to `main` and then merge `revised-definitions` to `main`. At some point along the way, you should see a merge conflict. It's when two branches have changes that are inconsistent with one another. You need to choose which change should be accepted. After resolving conflicts, merge your `revised-definitions` branch into `main`. Then you should stage, commit, and push your `main` branch.

## How to use branching to collaborate  

Here is a good tutorial on [how to use branching to collaborate](https://youtu.be/MnUd31TvBoU) in Git and Github.
