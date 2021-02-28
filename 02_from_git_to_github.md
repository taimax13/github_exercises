# From Git to GitHub  

In the previous lessions, you learned how to work with the command line and how to work with projects from GitHub Classroom. When learning about GitHub classroom, you created a project folder on your machine by cloning a GitHub repository, and that repository came pre-loaded with `git`. In this lesson, you learn how to create projects locally on your machine instead of cloning them from GitHub. You'll also learn how to setup `git`, connect to GitHub, and push your work to GitHub.

This lesson is a workshop format. Follow along on as you read the instructions by doing the tasks on your computer too. By the end of this lesson, you will:

- Create a project folder and **[initiate `git`](#initiate-git-on-local-machine)** inside it  
- [Save Your Work Locally Using `git`](#save-your-work-locally-using-git)
- [Create a GitHub repository](#create-a-github-repository) for your project  
- [Connect your project](#connect-local-git-to-github) to GitHub and push your code    

Plus, you'll have more experience using the command line with `git` and GitHub and will gain experience with a common workflow for setting up projects.  

Before you start the workshop tasks, get a quick conceptual overview of `git` and GitHub. This overview assumes you have no previous experience with `git` and GitHub. By the end, however, you'll have an excellent idea of what `git` and GitHub are and what you can use them for. Then, after the video, you can put what you learned from the video into actual practice on your machine and in your GitHub account.  

[![GitHub Classroom](images/git_one.png)](https://www.youtube.com/watch?v=BCQHnlnPusY)  

## [Initiate `git` On Local Machine](#initiate-git-on-local-machine)

On your computer, create a project folder for your new project. Name it github_exercises. You can create the folder using your operating system's graphical user interface, which is probably the way you're used to creating new folders on your computer.  

But it's better that you learn and practice terminal commands.

Open VS Code. In the pulldown options at the top, select View and then Terminal. It should open a terminal session. In the terminal, type `pwd`. The terminal should print the present working directory, which is the folder that your terminal is currently operating in. It is probably in your computer's root folder.

Use the terminal to list the contents of the present working directory by entering the `ls` command. The `ls` command lists the items in the present working directory.

Use the terminal to change the location of the present working directory to the folder on your computer where you store your code. The command to change directories (to move the `pwd`) is `cd <filepath_for_folder>`. For instance, if the folder you want to change into is in your present working directory and is named `developer_projects`, to change your present working directory to that folder, type `cd developer_projects` and hit enter. Note that because this folder is in the present working directory, you just type `cd ` followed by the folder name rather than the whole path for that folder.

Type `pwd` to confirm that you are in the correct folder. Type `ls` to see its contents. Repeat these steps until the present working directory for your terminal is the one where you want your project folder to live.

Or instead of repeating these steps, type in your terminal `cd` followed by a space ` `. Then, using your operating system's graphical user interface, drag to the terminal the folder where you want your project folder to live. You should see after the `cd ` a filepath for your folder. Then hit enter and confirm you are in the correct folder using `pwd` and `ls`.

Create a project folder inside your `pwd` named `github_exercises`. Using the terminal command `mkdir <folder_name>`, the command is `mkdir github_exercises`. after entering that command, enter `ls` in your terminal. You should see your new folder.

Then change directories into that folder `cd github_exercises`. Use `pwd` and `ls` to confirm you're in the correct folder.

Now it's time to check the `git` situation for your new folder. In your terminal, type `git status` and hit enter. You should see a list of filepaths, which means you need to initiate a local `git` repository for your project.

```shell
git status

# output in terminal
 ../../../../../../.CFUserTextEncoding
        ../../../../../../.DS_Store
        ../../../../../../.Trash/
        ../../../../../../.cups/
        ../../../../../../.local/
        ../../../../../../.netrc
        ../../../../../../.npm/
        ../../../../../../.ssh/
        ../../../../../../Applications/
        ../../../../../../Desktop/
        ../../../../../
        ../../../../../../Downloads/
        ../../../../../../Library/
        ../../../../../../Movies/
        ../../../../../../Music/
        ../../../../../../Pictures/
        ../../../../../../Public/
```

One other way to confirm that you don't yet have `git` initiated is to list all contents of your project folder, including the hidden folders and files. When you initiate a local `git` repository, it creates a hidden file in your project folder called `.git`. The `.` means that it's hidden. To see hidden files, type in your terminal `ls -al`. If you don't see a `.git` file listed in the terminal, then you don't have `git` initiated yet.

To initiate a local `git` repository, type in your terminal `git init` and hit enter.

```shell
git init

# output in terminal
Initialized empty Git repository in /Users/jonathangrossman/Documents/Developer/ITC/Work/git/github_exercises/.git/
```

Your terminal should say that you initialized an empty git repository. Do two things to confirm. List all the contents in your folder. Remember, when you initiate a local `git` repository, it creates a hidden file in your project folder called `.git`. The `.` means that it's hidden. This time when you type in your terminal `ls -al`, you should see a `.git` file listed in the terminal. This means your folder has `git` initiated.

```terminal
total 16
drwxr-xr-x   4 computer_user  staff   128 Sep 30 14:07 .
drwxr-xr-x   4 computer_user  staff   128 Jun 21 15:35 ..
drwxr-xr-x  12 computer_user  staff   384 Sep 30 14:49 .git
```

The other thing you should do to check that `git` is tracking your folder is to enter the terminal command `git status`. It should print out something like the following:

```terminal
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        01_getting_started.md

nothing added to commit but untracked files present (use "git add" to track)
```

Remember before initiating `git`, the `git status` command returned a list of filepaths. Now the terminal output is different. It confirms you successfully initiated a local `git` repository.

## [Save Your Work Locally Using `git`](#save-your-work-locally-using-git)  

The next step is to add a file to your project. In your project folder, create a file named `gitHubCommands.js.` Leave it empty for now.

Next, save a copy of your project folder to the local `git` history. Remember, `git` doesn't save your work automatically. You first have to move files from your project folder to the `git` staging area using `git add -A` (of instead of `-A` for all, you can enter just the name of the file you want to add). Then, you need to commit the files in the staging area, which is like officially saving them to your local `git` repository. You use `git commit -m "a message here"`. When you save your folder, you're only saving the newest changes since the last time you saved. 

Here is a step-by-step walkthough for saving the changes to your local `git` repository. First, stage your edits using `git add -A`. The `-A` means to add all the changes made.

```shell
git add -A

# nothing should happen in the terminal
```

Next, commit the staged changes to your local `git` history. The staging didn't actually save the changes to your `git` history. You need to commit them for the changes to save to the local `git` repository. Use `git commit -m "a short desriptive message about the changes"`.

```shell
git commit -m 'first commit'

# output in terminal
[master (root-commit) 1d49d54] first commit
 1 file changed, 60 insertions(+)
 create mode 100644 01_getting_started.md
```

You successfully saved your project folder to a local `git` repository.

## [Create a GitHub Repository](#create-a-github-repository)

Now that you have a project folder with a local `git` repository and have saved your code to it, you need to connect the local `git` repository to a remote one. The first step to connect your local and remote repositories is to create a remote repository. For the remote repository, you should use GitHub.

Login to your GitHub account. In the upper righthand corner, find the plus sign (`+`). Click it and choose 'New Repository'. Note that in this exercise, you are not using GitHub Classroom. If, however, you had a GitHub Classroom repo without starter code, the steps in the next section should work for you (and you could skip over the rest of this section).    

On the 'New Repository' page, you need to specify the details of your repository. First, for repository template, choose 'No template'. For the owner, choose your GitHub account. For the Respository name, name it `github_exercises`, like your local project folder name. The name of your repository doesn't need to be the same name as the project folder on your machine, but you might find that a good way to keep things organized.

Leave the description blank, choose private, and click the 'Create repository' button. GitHub should redirect you to the Quickstart page for your new repository. Read the instructions on that page and follow them. The description below helps guide you through those instructions.

## [Connect Local Git to GitHub](#connect-local-git-to-github)  

The Quickstart instructions for your new Github repo have six `git` commands. You don't need to do the first three now because you basically already did them. Here are the first three:   

```shell
git init
git add README.md
git commit -m "first commit"
```

You've already done the first one, you can skip the second one because you already did `git add -A` to add files (you can add a READ.md later if you want), and you've already done the third one.  

The fourth `git` command sets the name of your primary working branch to `main`. Enter in your terminal the following:  

```
git branch -M main
```

The fifth command has you connect your local `git` to GitHub by storing the GitHub address in your `git` files. Before doing that, confirm that your local `git` doesn't yet have a remote. In your terminal, type `git remote`.

```terminal
git remote -v

# should return nothing in the terminal
```

Now add a remote. When you add a remote, you are telling the local `git` repository the address of where to find your remote repository. To add a remote repository to your local `git`, the terminal command is `git remote add <name_of_remote> <link_to_github_repo>`. For the `<name_of_remote>`, use `origin`. For the `<link_to_github_repo>`, it is on the Quickstart page for your repo and looks something like `git@github.com:<your_github_username>/<your_github_repo_name>.git`.

```terminal
git remote add origin https://github.com/your-github-name/your-repo-name.git

# should return nothing in the terminal
```

Now, check again your local `git` remote reference using `git remote -v`. This time you should see the terminal print `origin` and the GitHub address.

```shell
git remote -v

# output in terminal
origin	https://github.com/your-github-name/your-repo-name.git (fetch)
```

Now that you connected the local and remote repositories, you can save the local `git` history to your GitHub repo. Remember above when you committed changes to the local `git`? Now you are going to `push` those committed changes to your GitHub repository. When first connecting local to remote, the command is `git push -u origin master`.

```shell
git push -u origin master

# output in terminal

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 770 bytes | 770.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com-yourname:yourname/your-repo.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

The current version of your project folder from your computer should now be saved to GitHub. From here on out, you only need to use the command `git push` instead of `git push -u origin master` to push your local to the remote.

Visit your GitHub repository in a browser. Make sure the page is freshly reloaded. You should see your commit in the repository. Your project folder from your computer should now be on GitHub.
