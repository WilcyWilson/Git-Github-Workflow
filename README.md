# Github Workflow

## The Four Git Zones

- Working Directory
  <pre>The project folder on your computer where you write and edit files. Changes here are unsaved and untracked by Git until you act.</pre>

- Staging Area (Index)
  <pre>A temporary holding space. You use git add to place selected file snapshots here before saving.</pre>
- Local Repository
  <pre>The .git database stored on your machine. You use git commit to permanently record the staged snapshots into your project history.</pre>

- Remote Repository

  <pre>A shared server like GitHub or GitLab. You use git push to upload your local commits so a team can access them.</pre>

<img width="1000" height="510" alt="image" src="https://github.com/user-attachments/assets/d192c7f2-0b17-4255-b593-00497a5c7250" />

## Github Sign In Commands

<pre>
Config Username: git config --global user.name "wilcywilson"
Config email: git config --global user.email wilsonshresthaxxxxxx@gmail.com
</pre>

## Commands to get started

<pre>
git init (initialization)
git remote add origin https://github.com/WilcyWilson/7thSem-FinalProject-EncryptionApp (origin github link)
git pull origin branchname(git pull remote branch )
git branch (list branches in repo)
git checkout branchname
git status (displays changes made to the branch)
git add . (adds changes)
git commit -m ""  (commits changes)
git push -u origin branchname (push to current branch)

Now, to add a different branch make a different folder to make things easier. And, repeat the above steps.
To push to branch next time just type "git push"
New Folder for every new branch
</pre>

## Setting Up a New Extending Branch (Preferably in a new folder in pc to make things easy)

<pre>
git init
git remote add origin https://github.com/WilcyWilson/7thSem-FinalProject-EncryptionApp
git pull origin splashscreen (Pulling the branch you want to add new features to.)
git checkout -b uisetup (Creates a new branch which will base it off the HEAD of current branch i.e. splashscreen.)
git branch (To check your current branch and available branches)
git push -u origin uisetup (Makes uisetup branch as upstream)

After this new branch will be created in the github website too.
</pre>

## Setting Up a New Empty Branch (Preferably in a new folder in pc to make things easy)

<pre>
git init
git remote add origin https://github.com/WilcyWilson/7thSem-FinalProject-EncryptionApp
git checkout --orphan NEWBRANCH (Creating Empty Branch)
Add files and changes.
git add .
git commit -m "commit for empty branch"
git push -u origin NEWBRANCH (Makes NEWBRANCH branch as upstream)
git pull (get remote branches info)

After this new branch will be created in the github website too.
</pre>

## Hard Reseting to head

<pre>
git reset --hard

This will reset our project to the previous head at the remote repo. Discards all local modifications and resets the entire project to the state of the last commit.

<img width="1360" height="864" alt="image" src="https://github.com/user-attachments/assets/90434e3e-6ae3-4ea4-8bd2-db7a128b38f8" />

</pre>

## Delete a Git Branch

#### Locally
<pre>
git branch -d branchname
</pre>

#### Remote Branch
<pre>
git push origin --delete branchname
</pre>

## Discard Untracked Uncommited files using git
<pre>
git restore <filename> (discard local, uncommitted changes and return a single file to its last committed state)
git restore --staged <filename> (unstage a file and move it back to "modified" status)
git restore --source <commit_hash> <filename> (To restore a file to its state from a specific historical commit)
</pre>

## Concise command that shows a list of previous commits and their hashes to identify a rollback target
<pre>
git log --oneline
</pre>

<img width="1004" height="258" alt="image" src="https://github.com/user-attachments/assets/20aceca7-16e9-482c-8fb0-c09e622b8140" />

## Discards all local changes to all tracked files in the current directory at once
<pre>
git checkout .
</pre>

<img width="1530" height="612" alt="image" src="https://github.com/user-attachments/assets/ae0e673b-b806-4639-af23-4bab9601f4c0" />

## Bulk removal of untracked files from the working directory
<pre>
git clean
git clean -f (git clean require the -f (force) flag by default to prevent the accidental permanent deletion of files that are not stored in Git's history)
</pre>

<img width="1500" height="364" alt="image" src="https://github.com/user-attachments/assets/b5a812c7-49dc-4f7a-85f9-6fe3f741e7f0" />

<pre>
git clean -fdn (safest git clean command to preview the deletion of both untracked files and directories)
<img width="846" height="112" alt="image" src="https://github.com/user-attachments/assets/659e656c-8a20-4e86-9a27-f86d15954f05" />
  
git clean -fd (forcibly remove all untracked files and directories in the current path)
<img width="804" height="106" alt="image" src="https://github.com/user-attachments/assets/0b75c233-8f63-4141-bfbb-428e1635b0b3" />

git clean -i (git clean flag allows you to choose which files to delete via a yes/no prompt for each item)
<img width="2216" height="250" alt="image" src="https://github.com/user-attachments/assets/f85a5ec3-2f2e-4ce2-b8a0-53e01e8cf684" />
</pre>

## Git command to list all configured remote aliases along with their fetch and push URLs
<pre>
git remote -v
<img width="1244" height="132" alt="image" src="https://github.com/user-attachments/assets/f4b1bbdd-c2f8-4e15-a75a-2450cb86e68a" />
</pre>

## Git command that lists both local and remote-tracking branches
<pre>
git branch -a
<img width="908" height="360" alt="image" src="https://github.com/user-attachments/assets/a5214438-91d6-4928-8b81-4963152af78a" />
</pre>

## Rename the most recent commit directly from the terminal without opening a text editor
<pre>
git commit --amend -m "Your new commit message"
</pre>

## Remove the folder in remote that has been already commited and pushed to remote but keep the local files intact
<pre>
git rm -r --cached "folder path or folder name"
</pre>

## Rename branch from master to main
<pre>
git branch -m master main
git push -u origin main
</pre>

## Delete branch from remote
<pre>
git push origin --delete master
</pre>

## Commit type suggestion
<pre>
feat: A new feature for the user (e.g. feat: add CSV export.)
fix: A bug fix 
refactor: improving code without changing what it does
pref: A code change that specifically improves performance
style: Formating, missing semi-colons, fixing indentation etc
test: Adding or fixing tests
docs: Changes to documentation (eg. to README.md)
chore: Updating build tasks, .gitignore, or pacakge dependendies
</pre>

## Install the Github CLI (gh)
<pre>
# Windows
winget install --id Github.cli
</pre>

## Create new branch
<pre>
git switch -c feat/thing-you-are-going-to-do
</pre>

## Rename commit that is older than the most recent commit
<pre>
git rebase -i (Interactive rebase)
</pre>



