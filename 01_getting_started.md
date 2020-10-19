## Initiate Git On Local Machine

On your computer, create a project folder for your new project. Name it github_exercises. You can create the folder using your operating system's graphical user interface, which is probably the way you're used to creating new folders on your computer.

But it's better that you learn and practice terminal commands.

Open VS Code. In the pulldown options at the top, select View and then Terminal. It should open a terminal session. In the terminal, type `pwd`. The terminal should print the present working directory, which is the folder that your terminal is currently operating in. It is probably in your computer's root folder.

You can use the terminal to list the contents of the present working directory. Use the `ls` command to list the items in the present working directory.

You can use the terminal to change the location of the present working directory. Use `cd <filepath_for_folder>` to change directories (to move the terminal into that named folder). For instance, if the folder you want to change into is in your present working directory and is named `developer_projects`, to change your present working directory to that folder, type `cd developer_projects` and hit enter. Note that because this folder is in the present working directory, you just type `cd` followed by the folder name rather than the whole path for that folder.

Type `pwd` to confirm that you are in the correct folder. Type `ls` to see its contents. Repeat these steps until the present working directory for your terminal is the one where you want your project folder to live.

Or instead of repeating these steps, type in your terminal `cd` followed by a space ` ` and then using your operating system's graphical user interface, drag to the terminal the folder where you want your project folder to live. You should see after the `cd ` a filepath for your folder. Then hit enter and confirm you are in the correct folder using `pwd` and `ls`.

Create a project folder. Use the terminal command `mkdir <folder_name>` to make a new folder in your `pwd`. Use for your `<folder_name>` the name `github_exercises`. The command then should be `cd github_exercises`. Enter `ls` in your terminal. You should see your new folder.

Then change directories into that folder `cd github_exercises`. Use `pwd` and `ls` to confirm you're in the correct folder.

Check the status of your local git repository. In your terminal, type `git status` and hit enter. You should see a list of filepaths, which means you need to initiate a local git repository for your project.

```
>>> git status


# output in terminal
 ../../../../../../.CFUserTextEncoding
        ../../../../../../.DS_Store
        ../../../../../../.Trash/
        ../../../../../../.babel.json
        ../../../../../../.bash_history
        ../../../../../../.bash_sessions/
        ../../../../../../.config/
        ../../../../../../.cups/
        ../../../../../../.gitconfig
        ../../../../../../.local/
        ../../../../../../.netrc
        ../../../../../../.npm/
        ../../../../../../.ssh/
        ../../../../../../.v8flags.7.8.279.23-node.34.febf543dfac02d19c086040be0b799f6.json
        ../../../../../../.viminfo
        ../../../../../../.vscode/
        ../../../../../../.yarnrc
        ../../../../../../Applications/
        ../../../../../../Desktop/
        ../../../../../
        ../../../../../../Downloads/
        ../../../../../../Library/
        ../../../../../../Movies/
        ../../../../../../Music/
        ../../../../../../Pictures/
        ../../../../../../Public/
        ../../../../../../rpi_backup/
        ../../../../../../user_dict = {
```

To initiate a local git repository, type in your terminal `git init` and hit enter.

```
>>> git init


# output in terminal
Initialized empty Git repository in /Documents/github_exercises/.git/
```

Your terminal should say that you initialized an empty git repository. Do two things to confirm. List all the contents in your folder. When you initiate a local git repository, it creates a hidden file in your project folder called `.git`. The `.` means that it's hidden. To see hidden files, type in your terminal `ls -al`. You should see a `.git` file listed in the terminal.

```
>>> ls -al


# output in terminal
total 16
drwxr-xr-x   4 name  staff   128 Sep 30 14:07 .
drwxr-xr-x   4 name  staff   128 Jun 21 15:35 ..
drwxr-xr-x  12 name  staff   384 Sep 30 14:49 .git
```

The other thing is the terminal command `git status`.

```
>>> git status


# output in terminal
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        01_getting_started.md

nothing added to commit but untracked files present (use "git add" to track)
```

Remember before the git init, `git status` returned a list of filepaths. Now the terminal output is different. It confirms you successfully iniated a local git repository.

The next step is to add a file to your project. In your project folder, create a file named gitHubCommands.js. Leave it empty for now.

Next, you need to save a copy of your project folder to the local git history. When you save your folder, you're only saving the newest changes since the last time you saved. To save the changes to your local git repository, first you need to stage your edits using `git add -A`. The `-A` means to add all the changes made.

```
>>> git add -A


# nothing should happen in the terminal
```

Next you need to commit the staged changes to your local git history. The staging doesn't actually save the changes. You need to commit them for the changes to save to the local git repository. Use `git commit -m "a short desriptive message about the changes"`.

```
>>> git commit -m 'first commit'


# output in terminal
[master (root-commit) 1d49d54] first commit
 1 file changed, 60 insertions(+)
 create mode 100644 01_getting_started.md
```

You successfully saved your project folder to a local git repository.

## Create a GitHub Repository

Now that you have a project folder with a local git repository, you need to connect the local git repository to a remote one. The first step to connect your local and remote repositories is to create a remote repository. For the remote repository, you should use GitHub.

Login to your GitHub account. In the upper righthand corner, find the plus sign (`+`). Click it and choose 'New Repository'.

On the 'New Repository' page, you need to specify the details of your repository. First, for repository template, choose 'No template'. For the owner, choose your GitHub account. For the Respository name, give it the name github_exercises. The name of your repository doesn't need to be the same name as the project folder on your machine, but you might find that to be a good way to keep things organized.

Leave the description blank, choose private, and click the 'Create repository' button. GitHub should redirect you to the Quickstart page for your new repository. Read the instructions on that page but don't yet follow them. Follow what's below instead.

## Connect Local Git to GitHub

Before connecting your local git history to your GitHub repository, confirm that your local git doesn't yet have a remote connection. In your terminal, type `git remote.`

```
>>> git remote


# should return nothing in the terminal
```

Now add a remote. When you add a remote, you are telling the local git repository the address of where to find your remote repository. To add a remote repository to your local git, the terminal command is `git remote add <name_of_remote> <link_to_github_repo>`. For the `<name_of_remote>`, use `origin`. For the `<link_to_github_repo>`, it is on the Quickstart page for your repo and looks something like `git@github.com:<your_github_username>/<your_github_repo_name>.git`.

```
>>> git remote add origin git@github.com:YourGitHubName/github_exercises.git


# should return nothing in the terminal
```

Now, check again your local git's remote reference using `git remote`. This time you should see the terminal print `origin`.

```
>>> git remote


# output in terminal
origin
```

Now that you've connected the local and remote repositories, save the local git history to your GitHub repo. Remember above when you committed changes to the local git, now you are going to push those committed changes to your GitHub repository. The current version of your project folder from your computer will be saved to GitHub. When first connecting local to remote, the command is `git push -u origin master`.

```
>>> git push -u origin master


# output in terminal

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 770 bytes | 770.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com-YourGitHubName:YourGitHubName/github_exercises.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

From here on out, you only need to use the command `git push` instead of `git push -u origin master` to push your local to the remote.

Visit your GitHub repository in a browser. Make sure the page is freshly reloaded. You should see your commit in the repository. Your project folder from your computer should now be on GitHub.
