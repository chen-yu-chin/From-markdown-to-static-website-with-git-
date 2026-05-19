
# Version-control with git & Github

###### Using git & Github for Collaborative Documentation
---

## What is git?
git is a distributed version control system used to track changes in files over time.

git allows you to:
- Save snapshots of your work
- Track file history
- Compare changes
- Restore older versions
- Collaborate with others safely
- Experiment using branches

---

### What is GitHub?
GitHub is a cloud platform built around git.
git works locally on your computer, while GitHub allows you to:

- Store repositories online
- Collaborate with teams
- Review changes
- Open Pull Requests
- Publish documentation websites
- Backup your repositories remotely

---

### Preparation

- Make sure you already have a [Github](https://github.com/?utm_source=chatgpt.com) account.
- Install [git](https://git-scm.com/install/).
- Check your git version, open your terminal and run: 
  `git --version`
- Configure your username and email:
  `git config --global user.name "Your Name"`

    `git config --global user.email "your@email.com"`

---

### Create and Clone a Github Repository:

Create a new repository:

1. Sign in to your Github account
2. Create a new repository
3. Choose a repository name
4. Set visibility:
   - Public
   - Private
5. Click Create repository

Clone the repository:

1. Go to the repository you want to clone.
2. Click on the drop-down menu: <> Code.
3. Copy the repository URL.
4. Go to Terminal and type in: `git clone https://github.com/yourname/your-repo.git`

This downloads the repository to your local machine.

---

### Create First Commit

   1. Move into the project folder: `cd your-repo`
   2. You can create new files or edit existing files in the folder.
   3. Before saving changes, check the repository status: `git status`  
    You may see: `Untracked files: README.md`

        This means git sees the file but is not tracking it yet.  
        You must add your files to tracking before commiting them.

   4. Track a specific file: `git add README.md`   
    Or track all changed files: `git add --all`    

        Now the files are in the staging area, ready for commit.

   5. Commit your files: `git commit -m "some description"` 
   6. Push your changes to Github: `git push`     

        Now your remote repository is updated.   
        You can refresh GitHub in the browser to see the changes online.
   7. Use `git log` to view your commit history.

---

### Working with Branches

Branches allow you to experiment safely without affecting the main project.   
Instead of editing directly on main, you can create a separate branch.

1. Create a new branch: `git branch new-branch`
2. Switch to the new branch: `git checkout new-branch`
3. Make your edits, then repeat the workflow:
```
git status
git add --all
git commit -m "Add new feature"
git push origin new-branch
```
Now the branch exists online on GitHub.

---
  
### Pull requests and merge:

A pull request is a request to merge changes from one branch into another.

Pull requests are important because they allow:
- Documentation / Code review
- Team discussion
- Error checking
- Collaboration before publishing

Create a pull request on GitHub:

1. Open the repository on GitHub.
2. Click: Compare & pull request.
3. Add title and description.
4. Click: Create pull request

After review, you can merge the pull request:

1. Click: Merge pull request
2. You can add Commit message and Extended description.
3. Click: Confirm merge
4. Delete the branch if no longer needed.

Now the changes become part of the main branch.

---

### Update Your Local Main Branch

The changes were made online on Github, now you have to pull the changes back to your local machine.

1. Switch back to the main branch: `git checkout main`
2. Pull the latest changes: `git pull`
   
Now your local repository is synchronized.

---

### Team Collaboration Workflow

main branch

   ↓

create branch

   ↓

edit documentation

   ↓

commit changes

   ↓

push branch

   ↓

open pull request

   ↓

review and discussion

   ↓
   
merge into main

