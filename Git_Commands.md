# Useful Git Commands

## Initializing a Repository

- `git init`: Initialize a new Git repository.

## Checking Status

- `git status`: Show the working tree status.

## Adding Files

- `git add .`: Add all changes in the current directory to the staging area.
- `git add -A`: Add all changes (including deletions) to the staging area.
- `git add <your file name>`: Add a specific file to the staging area.

## Committing Changes

- `git commit -m "commit message you want to add"`: Commit changes with a message.

## Pushing Changes

- `git push -u origin main`: Push changes to the main branch on the remote repository.
- `git push -u origin <branch name>`: Push changes to a specific branch on the remote repository.

## Configuring Global User

- `git config --global user.name "your name"`: Set the global username.
- `git config --global user.email "your email"`: Set the global email.

## Connecting to a Remote Repository

- `git remote add origin <remote url>`: Add a remote repository.
- `git remote -M main`: Rename the current branch to main.
- `git push -u origin main`: Push the main branch to the remote repository.

## Removing Connections

- `git remote remove <remote name>`: Remove a remote repository.
- `git remote rm <remote name>`: Remove a remote repository (alternative command).
- `git branch -r -d <remote/branch>`: Delete a remote-tracking branch.

## Pulling Changes

Sometimes you need to pull before pushing if your remote repository contains some changes that are ahead of your local repository.

- `git pull --rebase origin main`: Pull and rebase changes from the main branch of the remote repository.

## Viewing Differences

- `git diff`: Show changes between the working directory and the staging area.
- `git diff --staged`: Show changes between the staging area and the last commit.
- `git diff <source branch> <target branch>`: Show changes between two branches.

## Viewing Logs

- `git log`: Show the commit history.
- `git log --oneline`: Show the commit history in a compact format.
- `git log --graph --oneline --all`: Show the commit history in a graphical format.

## Branching

- `git branch`: List all branches.
- `git branch <branch name>`: Create a new branch.
- `git checkout <branch name>`: Switch to a specific branch.
- `git checkout -b <branch name>`: Create and switch to a new branch.
- `git branch -d <branch name>`: Delete a local branch.

## Merging

- `git merge <branch name>`: Merge a branch into the current branch.

## Stashing

- `git stash`: Stash the current changes in a dirty working directory.
- `git stash apply`: Apply the stashed changes to the working directory.
- `git stash pop`: Apply the stashed changes and remove them from the stash list.
- `git stash list`: List all stashes.

## Resetting

- `git reset --soft HEAD~1`: Undo the last commit, keeping changes in the staging area.
- `git reset --hard HEAD~1`: Undo the last commit and discard changes in the working directory and staging area.

## Cloning

- `git clone <repository url>`: Clone a remote repository to your local machine.

## Fetching

- `git fetch`: Fetch changes from the remote repository without merging.
- `git fetch --all`: Fetch changes from all remote repositories.

## Reverting

- `git revert <commit>`: Create a new commit that undoes the changes of a previous commit.

## Tags

- `git tag`: List all tags.
- `git tag <tag name>`: Create a new tag.
- `git push origin <tag name>`: Push a tag to the remote repository.

## Aliases

- `git config --global alias.<alias name> '<git command>'`: Create a custom alias for a Git command.

Example:
```sh
git config --global alias.co 'checkout'
```


## After Uploading to Remote Repository
1. `git status`: Check the status to ensure the repository is clean.
2. `git remote remove origin`: Remove the remote connection if no longer needed.
3. Close the terminal window.

## Starting a New Project

- Create a new directory and navigate into it:
```sh
mkdir new_project
cd new_project
```

- Initialize a new Git repository:
- `git init`

- Add a new remote connection:
- `git remote add origin <new_remote_url>`


- Removing Git Tracking from a Folder
- Navigate to the directory you want to ungit:
```sh
cd path/to/your/directory
```

- Remove the .git directory:
```sh
rm -rf .git
```


- Verify by checking the status:
```sh
git status
```

## If the directory is no longer a Git repository, you should see an error message:
```sh
fatal: not a git repository (or any of the parent directories): .git
```
