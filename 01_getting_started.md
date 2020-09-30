## Initiate Git On Local Machine

```python
git status

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

```python
git init

# output in terminal
Initialized empty Git repository in /Users/jonathangrossman/Documents/Developer/ITC/Work/git/github_exercises/.git/
```

```python
git status

# output in terminal
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        01_getting_started.md

nothing added to commit but untracked files present (use "git add" to track)
```

Stage your uncommitted changes by adding all changes.

```python
git add -A

# nothing should happen in the terminal
```

Commit the staged changes to your local git history.

```python
git commit -m 'first commit'

# output in terminal
[master (root-commit) 1d49d54] first commit
 1 file changed, 60 insertions(+)
 create mode 100644 01_getting_started.md
```

## Create a GitHub Repository

Create a repository on GitHub. Login to your GitHub account. In the upper righthand corner, find the plus sign (`+`). Click it and choose 'New Repository'.

On the 'New Repository' page, you need to specify the details of your repository. First, for repository template, choose 'No template'. For the owner, choose your GitHub account. For the Respository name, give it the name github_exercises.

Leave the description blank, choose private, and click the 'Create repository' button. GitHub should redirect you to the Quickstart page for your new repository. Read the instructions on that page but don't yet follow them. Follow what's below instead.

## Connect Local Git to GitHub

Before connecting your local git history to your GitHub repository, confirm that your local git doesn't yet have a remote connection.

```python
git remote

# should return nothing in the terminal
```

Now let's add a remote. To add a remote repositorty to your local git, the command is `git remote add <name_of_remote> <link_to_github_repo>`. The link to your GitHub repository is on the Quickstart page for your repo and looks something like `git@github.com:<your_github_username>/<your_github_repo_name>.git`

```python
git remote add origin git@github.com:JonathanGrossmanITC/github_exercises.git

# should return nothing in the terminal
```

```python
git remote

# output in terminal
origin
```

Push the local git history to your GitHub repo. Remember above when you committed changes to the local git, now you are going to push those committed changes to your GitHub repository. When first connecting local to remote, the command is `git push -u origin master`.

```python
git push -u origin master

# output in terminal

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 770 bytes | 770.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com-JonathanGrossmanITC:JonathanGrossmanITC/github_exercises.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

Visit your GitHub repository in a browser. Make sure the page is freshly reloaded. You should see your commit in the repository.
