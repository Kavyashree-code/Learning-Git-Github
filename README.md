# Learning-Git - Procoder
youtube-procoderr "https://www.youtube.com/playlist?list=PLfEr2kn3s-brBO7d9irTRvClcjiNhzczH"

 Git is a tool Version Control System using git project can be saved in different versions, if deleted by mistake old code can be retrieved and use
 
 to use git need to know Terminal/cli - command line interface(is a sw)
   inside terminal we have many shells ex: cmd - command prompt, windows powershell, azure shell, gitbash
   
2 ways to access comp resourses : GUI - graphical user interface, CLI - command line interface

cmd/powershell : windows based, more old no new features, no touch command support ex: 2 or more folder at one cant create, no mv command(rename and move).
Gitbash : Linus based, new features, can move the code to server (all online server shell will be linux based), has all commands a terminal should have - touch, mv...

cmd/powershell ->ls (list of all folders)
-> cd (change directory/folder) (front)
cd ../ (back)
mkdir (new directory)
rm (remove folder permanatly)
code . (vs open)
pwd (print working directory)
git -v or git --version (version of git, if error git is not installed)

NOTE : tab - do autocomplete
ctrl + l - clear terminal works in gitbash
cls - clear the terminal works in cm
if folder name space use"" ex: cd "kavya shree"
ctrl + ~   - opens terminal
ctrl + (increase font size)
shift+ $ q (new gitbash line)
rename or move =mv
to see single code history: vs code -> timetine ->select git history ->can see commited files
ctrl + shift + p = command palet -> graph 

download git (git-scm.com)
  Git Bash ->$ mkdir 00_lening-git (new folder)
  $ mv 00_lening-git/ 00_learning-git (renaming of folder)
  $ touch index.html style.css script.js (create multiple files using cli)
  $ mv index.html style.css script.js ./00_learning-git/

  Repository: container/place/database where we can store diff version of code
  current working area/change area : is a untracked file i.e repository files is not tracked so U, to track need to put code in staging 
                                    area, all files comes to staging area when added + shows A , if - clk comes to changes area shows U 
                                    or ?
                                    when we are in changing area and write additional code can disgard it very easily
                                    
  staging area : is just to verify code before commit
  
  Commit : saving the snapshort of new changes in the code after verifying/testing  of the code in memory with message
  
  gitlens: multiple new users can change the code, or which user changed wt line
      vs code -> extension ->gitlens
      after gitlens opens we can see "YOU 1hr ago" in it
      can see how many commits we made ,can see commit in both gitlens or source control -> commit, shows A-Added and M -modified
      gitlens->file history can see commit here too
      
  github: if the .git folder i.e local repository code deleted we cannot recover the code so we use github i.e remote repository

  Branch : y is it necceccasry to create a branch-here whole project is managed by git here main branch is Master inside Master branch the whole proj code excits using this master branch we publish code to the server, so directly we dont work with the master branch as it goes to live website(production environment) so we create another branch from master
  
  
  $ git -v
  $ git init 
          (starting/initializing git repository) folder we get .git in hidden section, in terminal we see master means a default 
           branch
               
  $ git add filename.extension 
                 (add 1file to staging area)
                 
  $ git add filename.extension filename.extension 
                (adds >1 file to staging area)
                
  $ git add . 
            (adds all file to staging area)
            
  $ git status
           (to know which file in staging area and which is in working/changes area, green-Staging and ready to commit red- Changes)
           
  $ git status -s
         (short form for checking status)
  
  $ git config --global user.name "kavya"
    git config --global user.email "kavya@gmail.com"

    git config --global user.name    (checking name &email)
    git config --global user.email 

    git commit -m "initial commit"
          (file added in repository, proj 1st version repository saved) 
          
  $ git log
         (to see all commited files)
         
  $ git checkout id_1
         (if i hve done 2 commits and now in 2 commit but want 1st commit code)
         
  $ git checkout master
         (we come to current 2nd commit not before i.e1 commit , here code became normal)
  $ git branch
         (list of branches)
         
  $ git branch about
         (creating about branch using master b)
         
  $ git checkout about
          (to go to about branch we created using master b)
          file->about.html-> add some code-> add to staging and commit the code-> if we do "git checkout master" the added code will not 
          disappear no file about.html found as oly change happened in master b, usually senior developer have access to this - to merge we need to pull request and senior developer checks/review  changes in code and then merge, now we have access so can merge easily
          
  $ git log --all
         (shows all other branches also)
         
  $ git log --all --oneline
          (shows all branch in oneline)
          
  $ git checkout id 
          (head comes here)
    git log --all --oneline
          (can see head in tht id)
    git checkout master
          (now head comes here)
          
  $ git log --all --oneline --graph
          (shows up graph)

          ex: we made qst 3 commits in master branch ,nxt e create new branch clled aboutand create 1 commit, here master branch as 3 
              commits, and about has 4 commits including master branch 
          
  $ git branch --delete contact
        (deletes contact branch, note to delete contact branch need to be out of contact b)
    note: if we delete contact b it gets deleted fast bez thr is no commit, git thinks not imp and delete it . But if we delete about b 
          from master cannot delete bez thr is a commit do merge it and then delete if not whole code gets deleted    
          
  $ git branch --D about
      (delete branch permanently but graph shows history)
  $ git branch contact
       (from master b contact b created)
       
  $ git merge contact
       (contact b is merged with master b., when merged comes to staged area and gives merge id)

  =====
  Storing in Server/remote repository
    like google drive for photos we have github for code saving
                                         bitbucket
                                         gitlab
 $ git remote show origin
      (shows weather u connected to any online or not)

$ git remote add origin github_link_repo
       (code connected to origin )

$ git branch -M main
     (master is renamed to main)
     
$ git push -u origin main
      (pushing code to github)
      if error:"failed to push some refs to ..githublnk" then

$ git push --rebase origin main


$ git pull -u origin main
     (now pushes code perfectly)
     
$ git push -u origin main
     
$ git log --all --oneline
     (we get origin/main means even remote repo is also here)
     
$ git push -u origin contact
      (adding another branch contact )
      
$ 

  
