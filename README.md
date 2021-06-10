# Notes for my Git workflow
- great resource: https://www.youtube.com/watch?v=0fKg7e37bQE

I downloaded/installed Git from https://git-scm.com/download/win and accepted all the standard stuff

# Clone a repo on a local machine
- navigate to local folder you want the repo stored (I stick with gitrepos as a folder name)
- in the git repo you want to clone select the **Green code button** and copy the clone url
- command line: **git clone https://github.com/Totilarson/CorePy.git** will copy the whole repository locally and puts it ion a folder called Corepy
- command line: **git branch** within the new repo will show you how many branches there are. Should be one: master that has a star. star means it is the one you are working 

# Make a develop branch and push it 
- command line: **git checkout -b develop** makes develope branch (locally) and you will be in this branch now
- command line: **git push origin develop**  this pushes the develop branch to github.com
- command line: **git checkout master** or **git checkout develop** are used to switch the branches you are working in. 
