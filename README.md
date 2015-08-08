gitimmersion.com/lab_01.html

-go to dev folder
git init

 "Reinitialized existing Git repository in xxx/JomWeb/.git/"

git add .
git commit -m "mesej"

 "[master (root-commit) f40d0d9] commit 1
  1 file changed, 18 insertions(+)
  create mode 100644 index.html"

git status

 "On branch master
 nothing to commit, working directory clean"
 
git log
 
 "Reinitialized existing Git repository in xxx/JomWeb/.git/"
 
 -if you have any changes
 "On branch master
 Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout - <file>..." to discard changes in working directory)

        modified:   index.html

 no changes added to commit (use "git add" and/or "git commit"  -a")
 
-Commit again

git add .
git commit -m "commit 2"

-check log
git log 
 
git gui 

IN GUI

- create new branch from Commit 1 (testui)

-Change Branch
git checkout master
git checkout testui

-Check different current unchanged file with latest changed file
git diff <filename>

git diff index.html
 
 diff -git a/index.html b/index.html
 index db8ca4a..31f97bc 100644
 -- a/index.html
 +++ b/index.html
 @@ -3,13 +3,13 @@
  <html>
  <body>

 -<h>Selamat Datang ke Bengkel Git 2015 - Master D3</h>
 +<h>Selamat Datang ke Bengkel Git 2015 - Master D4</h>

 
-Red - line removed
-Green - line added 

-If uncommit, "git checkout <filename>" will revert to previous commit.  

Git status to know current status, branch. 

-Merge branches
- 1. Enter required branch
git checkout testui

- Merge the current and required branch 
git merge <branch>

-sample result
 "<<<<<<< HEAD
 <h>Selamat Datang ke Bengkel Git 2015 - testui D5</h>
 =======
 <h>Selamat Datang ke Bengkel Git 2015 - master D4</h>
 >>>>>>> master"
 
 -<<<< HEAD : Current branch file contents. 
 -==== : Separator of the conflicts contents.
 ->>>>>> master : Conflicts contents originally from master branch
 
-To handle conflicting file
-- Open the file that conflicts
-- Edit as per required using any tool
-- Then run add and commit again

git add . 
git commit -m "message"
-Right after commit, the branches will be merged. 

 "[testui xxxxx] merge"
 
-GIT Connect to Remote Repo GITHUB using HTTPS
git remote -v
git remote add origin https://github.com/ajib85/GITLab-Test.git
git push -all 
 
 "username:
 password:"

-File will be uploaded to GITHUB. If error for first time, try below action and try again. 
 
git pull origin master
git push -all


