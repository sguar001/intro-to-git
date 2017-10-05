==============
SECTION 2
==============
#Git 
* (master) means you are on the master branch after git init

# Working Directory
* Area where all of our files and directories are living all the time

# Staging Area
*  Files and directories that we explicitly add to the staging area (add)

# Git Repository 
* Where all our snapshots are stored

# git commit -m "Message goes here"
* Save files to repository

==============
SECTION 3
==============
# Adding multiple files of a certain type
* git add *.html

# Adding all files in a directory (including hidden files and folders from the directory)
* git add -A

# Removing files (unstage files)
* git resest HEAD <file> 

# Ignoring files
* add file name to a created .gitignore file! 

# Rename files
* mv <old_file_name> <new_file_name>

# Move files to a directory
* mv <file-to-move> <directory-to-move-to>

==============
SECTION 4
==============
# Git Branches 
- Listing all branches
    * git branch (asterisk marks current branch)
    
- Adding a branch
    * git checkout -b <branch_name>

- Changing branches
    * git checkout <branch_name>

- Merging a branch
    * git merge <branch_name> (merges branch_name to current branch)

- Removing a branch (best not to do so)
    * git branch -d <branch_name>
    

==============
SECTION 5
==============
# Checking out commits
- Make sure inside project's directory
- Once inside the directory, use git log to view your log history
- You can scroll down to earlier commits by hitting enter
- Once you locate the commit you want to checkout, copy the hash key from the commit    
    - the hash key is the alphanumeric string that comes after teh word "commit"
- Exit out of git log by pressing q
- type git checkout <hash key> and hit enter
- Now look inside of this commmit and copy any code that you need. 
    - If you'd like to start working from this commit, but don't want to overwrite any of the code from the branch that you're currently on 
      (in this case it's master) then you can type git checkout -b <branch_name> to create a new branch to begin working from.
- Once you're done working from this commit, you can return to the most recent commit on the branch of your choosing by typing
  git checkout <branch_name>, (i.e. git checkout master)
- Note: When you checkout an earlier commit, you are now in a "detached HEAD" state, this means that you are no longer on the commit that 
  is being pointed to by the HEAD. The HEAD, in git, is a pointer to the most recent commit of whichever branch you are currently on.

==============
SECTION 6
==============
# Using GitHub
- Connect to GitHub with C9
    - add SSH key to github!
- Push to existing repository!
    - git remote add origin https://github.com/sguar001/intro-to-git.git
      git push -u origin master
      git remote -v (check to see if remote is added)