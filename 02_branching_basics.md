# create a new branch

Create a new branch called `from _itc`.

```python
git checkout -b from_itc

# output
Switched to a new branch 'from_itc'
```

To see a list of your branches and which branch you're on, enter `git branch`.

```python
git branch

# output
* from_itc
  master
```

Type `ls` to see a list of the contents. What is in your folder?

```python
git clone https://github.com/JonathanGrossmanITC/github_exercises.git

#output
Cloning into 'github_exercises'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 12 (delta 3), reused 11 (delta 2), pack-reused 0
Unpacking objects: 100% (12/12), done.
```

Type `ls` to see a list of the contents. Do you see the cloned repo? What else is in your folder?

Change directories into the `github_exercises` folder. Look at the list of all contents using `ls -al`. You should see a `.git` folder. This is the local git history for the cloned repo. You should delete it. After deleting it, type `ls -al` to confirm it's gone.

You can change directories up one folder using `cd ..`. Change from the `github_exercises` folder up one to your project folder. Type `ls` to see the folder contents.

It's time to push your branch to GitHub. Check the status `git status`. You should see some red untracked files. Track them by adding them to the staging area `git add -A`. Then commit them `git commit -m cloned from itc`. Then push `git push`. You might get a terminal message `git push --set-upstream origin from_itc`. Copy that and enter it in your terminal.

You should see in your terminal:

```python
On branch from_itc
Your branch is up to date with 'origin/from_itc'.

nothing to commit, working tree clean
```

Now switch from the `from_itc` branch to the `master` branch entering in your terminal `git checkout master`. You folders in VS Code should change to the master branch. Look at your folders. The `github_exercises` folder should be missing.

You should now merge the `from_itc` branch into the `master` branch. Enter in the terminal `git merge from_itc`. In your terminal, you should see something like:

```python
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

Also, look at your folders in VS Code. The `github_exercises` folder that you cloned into the `from_itc` branch should now appear. In your terminal, type `git branch`. It should indicate that you're in the master branch.

# Assignment.

Create a new branch called `assignment`. While in the `assignment` branch, add the code below to your gitHubCommands.js file. For each variable, replace the empty string with a string describing the corresponding git command. Then merge the `assignment` branch into the master branch and push the master to GitHub.

```python
# git add
const gitAdd = ''

# git commit
const gitCommit = ''

# git status
const gitStatus = ''

# git push
const gitPush = ''

# git merge
const gitMerge = ''

# git checkout
const gitCheckout = ''

# git branch
const gitBranch = ''

# git clone
const gitClone = ''

# git pull
const gitPull = ''

# git remote
const gitRemote = ''
```
