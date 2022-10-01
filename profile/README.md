# Cornell-Med-HBDS-5018

## Welcome

Here is some instruction to help you make things correct (hopefully).

## Clone the Repository

Before you get started, you need to clone the remote repository to your own computer with one of the commands (replace `<X>` to the lab #):

```
# via HTTPS
$ git clone https://github.com/Cornell-Med-HBDS-5018/lab-<X>.git

# via SSH
$ git clone git@github.com:Cornell-Med-HBDS-5018/lab-<X>.git
```

## How to Make Commits

### :warning: Before You Get Started

Make sure you synchronize your local `main` branch from the GitHub:

```
# checkout to main branch
$ git checkout main

# pull from GitHub
$ git pull origin main

# create a new branch from main (replace <your_branch_name> with your own branch name)
$ git checkout -b <your_branch_name>

# if the branch exists
$ git checkout <your_branch_name>
$ git merege main
```

### :new: Make Commits

Once you believe you completed part of the work or everything, you need to make a commit to keep the moment:

Before you make commits, you need to execute `git status` to check modified/untracked files:

```
$ git status

On branch CathZz

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.gitignore
	profile/

nothing added to commit but untracked files present (use "git add" to track)
```

In this case, `.gitignore` and `profile/` are NOT tracked by github. Then you need to add **files/directories you want to commit** into staging area via `git add <file you changed>`

```
$ git add .gitignore profile/
$ git status

On branch CathZz

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   .gitignore
	new file:   profile/README.md
```

Once you **confirmed** files in staging area is the file you want to commit, you can use command:

```
# replace <commit message> to your own
$ git commit -m "<commit message>"
``` 

Congratulation, you make a commit by your own.

### :octocat: Push to GitHub

Then you need to push your commits to GitHub so everyone else will see what you have done so far (replace `<your_branch_name>` with your own branch name):

```
$ git push origin <your_branch_name>
```

Note: Direct push to `main` branch is **NOT allowed**. You have to make commits on your own branch locally then push it to GitHub. I will merge your commits into the `main` branch.
