# GitHub Startguide

____________________________________________________________________________

### CREATING A REPOSITORY

ON YOUR GITHUB ACCOUNT

____________________________________________________________________________

1.  🖥️ LOCAL → open Terminal and create a new project folder by typing: 
    
    `mkdir <folder-name>`
    
2. use `cd` (change directory) to navigate to that newly created folder:
    
    `cd <folder-name>`
    
3. initialize this folder to become a git folder and type:
    
    `git init`
    
4. add your files to the staging area by typing:
    
    `git add .`
    
    This will add everything in the current folder to git
    
     *optional → Before you type git add, you can create a readme file and then continue to add it:*
    
    - `*touch [readme.md](http://readme.md)` creates the file*
    - `*echo “your-text” > [readme.md](http://readme.md)`  will write the text in the “”into your readme*
    - `*cat [readme.md](http://readme.md)` will read the text in the file to make sure it got there*
5. commit the changes with a message by typing:
    
    `git commit -m “initial commit”`
    

 6. 🌐 REMOTE → create a new repo on gitHub :

- Go to the gitHub website and your account
- click on new button on the upper left side of the page
- add a repository name and select public (or private).
- click on create repository button
- scroll down all the way to *“…or push an existing repository from the command line”*
    
    *and copy the code underneath*
    

1.  🖥️ LOCAL → switch to Terminal and connect the local repo to the remote one: 
    - paste the code in the command line and hit enter
    - push the local repository to the remote one by typing
        
        `git push -u origin main`
        
    - with `git status` you can check if all worked out
    

____________________________________________________________________________

### CREATING NEW BRANCHES / PULL REQUEST

AS TO WORK ON AN ISSUE OF AN EXISTING REPOSITORY

____________________________________________________________________________

1.  🖥️ LOCAL → open Terminal and navigate to the repository main branch 
    - use `cd` (change directory) to get there
    - use `ls` (list) to list all possible destinations and                                                                             `pwd` (print working directory) to show where you are at
2. get the latest changes from the remote repository by typing:
    
    `git fetch origin`
    
3. create and switch to a new branch for the issue you want to work on by typing:
    
    `git checkout -b <branch-name>`
    
4. work on the issue on you local computer as usual. Make changes to code, add files, etc.
5. add your changes to the staging area by typing:
    
    `git add .`
    
6. commit the changes with a message by typing:
    
    `git commit -m “Example: Commit message”`
    
7. push the new local branch to the remote gitHub repo by typing:
    
    `git push origin <branch-name>`
    
8. 🌐 REMOTE → create a pull request by following these steps:
    - Go to the gitHub repository in your browser
    - click on pull requests tab
    - click the new pull request button
    - select main branch and the newly created branch from the dropdown menu
    - review the changes and click on create pull request
    - add a title and comment and  click on create pull request again
    - click the create pull request button to submit the request
9. merge the pull request
    - if request is approved, message appears “✅*This branch has no conflicts with the base branch”.* You can then merge changes into main branch by hitting merge pull request
    - now add a commit message and hit confirm merge
    - delete the remote child branch on github by clicking on delete branch
10. 🖥️ LOCAL → switch back to Terminal and:
    - copy the SSH link to it
        
        `git@github.com:jennywhitmore/we-share.git` 
        
    - delete child branch locally as well by typing:
        
        `git branch -D <branch name>`