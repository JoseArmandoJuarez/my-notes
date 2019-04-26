## How to compare 2 files in command prompt or in git bash using FC…
1. Navigate to where the files are
2. Then use the FC command and type in the two files you want to compare
    * FC favorite-app-old.html   favorite-app.html
4. Hit ENTER and you will be able to see the difference between the two files

## How to compare 2 files using the diff command in Linux and Mac…
1. Navigate into where the files are
2. Then enter the command diff -u and the two files you want to compare
    * The -u stands for unified diff format and it will make the output a little easier to read 
    * diff -u favorite-app-old.html  favorite-app.html
4. Hit ENTER and you will be able to see the difference between the two files. Also the output format is different than the output format of FC

* The lines with the plus signs in the diff output were added and the lines with the minus signs were removed, and other lines that don't have either a minus or a plus sign it means that they were unchanged.

---

## What is a commit? 

* Basic building blocks of Git. Each one representing a version of the content at one point in time.

* Example of a commit may look like this….

        commit 3889sa8d893hfaffas
        Author: john <john@gmail.com>
        Date:    Fri 29 12:33:05 2011-0700

            Adding color to title


## How to checkout commits?
* Fist navigate into the file you want to check the commits and the type in git log, and you will be able to see all the commits.
* Each commit has an id, an author, a date and a message telling what changes have been made

---

## Clone command
* Use git clone to clone a git repository
    * git clone https://…./documentation-tests.git

---

## Move a file to a new or another directory use mv command
* Create a new repository using mkdir and then name of file or just move it to the one already created
    * mv file-location/name-of-File.html
    * mv game-folder/space-shooter.html

* Use git checkout to temporarily reset all files in a repository to their state at the time of a specific commit.

---

## git init
* Initializes or creates a new git repository.

---

## Compare Commits
* Use git diff to check the difference made between two commits by comparing their IDs
1. Navigate to the file you want to check the commits
2. Compare the IDs 
    * git diff  234gd4f4gg  343gs78sdf
    * git diff  old-commit   new-commit

---

## git log --stat 
* Gives some statistics about which files have changed in each commit

        *   (HEAD -> master, origin/master)
        |   ed4d8d8 - adding color to the title (2 hours ago) <Reece>
        *   
        |   efdg45f3 - adding an image to the about page (6 hours ago) <John>
        *
        |   fe7763ff - changing the title ( 10 hours ago) <Reece>

---

## git status
* Use git status to show which files have changed since the last commit. Which files you need to add and commit

---

## git add
* To add a file to the staging area to be ready to be committed

---

## git commit
* When you commit DO NOT use uppercase and should not end with a period
	* git commit -m changing text style to title

---

## STEPS TO COMMIT
1. Check the status to check which files need to be committed (the names of the files should be highlighted in red, if they are highlighted in green then they are ready to be committed)
2. Add the file you want to commit by typing:  git add app-game.html
3. To check if done right check the staging area by typing:  git status and if the name of the file is in green then it's ready to commit
4. git commit -m adding color to title
5. To check if committed type git log to see if committed

---

## git log --graph --oneline
* You can see all commits in a graph by typing:
	* git log --graph --oneline
