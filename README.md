# Working Directory
- Area where all of our files and directories and changes are livinbg all the time

# Staging Area
- Files and directories that we explicitly add to  the staging area

# Git Repository
- Where all our snapshots are stored

# Adding multiple files of a certain type
- git add *.<file extension>
For example git add *.html

# Adding all files in a directory (including hidden)
- git add -A will add ALL files and folders from the directory you're currently working in.
- It's a good command for adding everything in your project at once.

# Removing Files
- git restore --staged <file>
- git reset HEAD <file>
 - Either of these commands should work just fine. 

# Ignoring files
- if you want Git to ignore a file in your directory, create a .gitignore file and then add the name of the file you want ignored to it. When you do a git status command afterwards, you shouldn't see that file name being tracked any longer.

# Git Branches

- Listing all branches
    - git branch
    - the asterisk and green text indicate the current branch you're working from/on.

- Adding a branch
    - git checkout -b <branch_name> - this command will automatically switch you to the branch once you hit ENTER

- Changing branches
    - Before you change branches, do a git branch command to list your branches. It's good practice so you're sure of where you are and the name of the branch you wan to switch to. 
    - git checkout <branch_name> - this will switch you from the current branch to the branch name you specified in the command.

- Merging a branch
    - git merge <branch_name> - this will merge the specified branch into your current branch. So if you're currently in a feature branch, you'd issue a 'git merge master' command to merge your master branch with this one. But you could also do it the other way around which is switching back to your master branch with the git checkout <branch_name> command first, then issue a git merge <branch_name>. Either way works.

- Removing a branch
    - git branch -d <branch_name>. While it's not recommended to delete branches, this command will do the job!
    Run a git branch command thereafter to verify that it's gone.

# Upload your code to GitHub using Git
- Setup
    - Assuming you've already created a GitHub account, created a repository for the code you're attempting to upload, the first thing to do is set the remote origin.
    - Grab the URL of your repository on Github because you'll need it for this next step.
    - So from your current directory (where your code exists), type git remote add orgin <url> and press ENTER
    - To confirm that the command was executed, you can check with git remote -v. It should show you the origin and it should be set to the  URL from your GitHub repository.
- Upload
    - Now to upload, use git push -u origin master
    - This means your local branch master is now on a remote branch master as well. The remote is called origin.
    - Go over to your GitHub account and you should see all your files there.
