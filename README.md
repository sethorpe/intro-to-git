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