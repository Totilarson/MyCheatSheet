# Setting up Python
-  https://www.python.org/ I am using Python 3.9.5 https://www.python.org/downloads/release/python-395/
-  and **select 'Add Python to environment variables**. This makes python available in command line
- from cmd: `pip list` shows all the Python packages
installed. **recommmend**
```
pip install numpy
pip install pandas
pip install seaborn
pip install corepytools
pip install sklearn
```
# Setting up Spyder IDE.
```
    - https://www.spyder-ide.org/. install spyder. I use v.5.0.5 
    - https://github.com/spyder-ide/spyder/releases/tag/v5.0.5
    - Set Python interpreter: Tools -> Preferences -> Python Interpreter "Use the following interpreter"
    - From the Start menu navigate to Python, right click -> More - Open file location
    - Copy the file location, paste it in the path. I had to add python.exe. 
    - This syncs Spyder with Python accessed from commandline.
    - In Spyder: Tools -> Preferences -> PYTHONPATH manager -> I navigated to a 'site-packages' folder where all the pip installed packages were going, and added that.
```
# Notes for my Git workflow
```
- great resource: https://www.youtube.com/watch?v=0fKg7e37bQE
- I downloaded/installed Git from https://git-scm.com/download/win and accepted all the standard stuff
- in cmd environment type `git --version` to make sure it is installed correctly
```
# Clone a repo on a local machine
```
- navigate to local folder you want the repo stored (I stick with gitrepos as a folder name)
- in the git repo you want to clone select the **Green code button** and copy the clone url
- command line: `git clone https://github.com/Totilarson/CorePy.git` will copy the whole repository locally and puts it in a folder called Corepy
- command line: `git branch` within the new repo will show you how many branches there are. Should be one: master that has a star. Star means it is the one you are working
```
# Make a develop branch and push it
```
- command line: `git checkout -b develop` makes develop branch (locally) and you will be in this branch now
- command line: `git push -u origin develop`  this pushes the develop branch to github.com -u is ony used the first time
- afterwards, 'git push' is sufficient
- command line: `git checkout master` or `git checkout develop` are used to switch the branches you are working in.
**At this point the CorePy repo is cloned locally and you can work from it in the develop branch**
```

# Pushing edits from local github repo to github.com
My work flow is to make changes on develop, then merge with master and push to remote

- 'git branch -a' to make sure you are working on develop.
- 'git checkout develop' to chagne to develop branch
- 'git status' to list changed tracked and changed untracked files. Untracked files will not be pushed
- 'git commit -a' to commit any changes from the develop branch
- 'git push' to update origin/develop
- 'git checkout master' to switch to master so that you can merge changes from develop
- 'git diff develop' to look at differences between develop and master.....type 'wq' if it is stuck in editor
- 'git merge develop' to bring the changes from develop to master
- 'git push' to update origin/master



# make changes to corepytools on Pypi
- need to install twin `pip install twine` and wheel `pip install wheel`
-  update the version number in the setup.py file 
-  `python setup.py sdist bdist_wheel`
-  `pip install –e .`
-  Twine upload dist/*
