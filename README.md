# khan-omar
Collaboration with Omar to build a website.
 
# Getting Started
 
1. Download and install Git for windows [here](http://git-scm.com/download/win). You can use [this tutorial](https://www.youtube.com/watch?v=albr1o7Z1nw) for reference. Follow the steps in the video till 4:54.
 
2. To understand SCM better, watch [this](https://www.youtube.com/watch?v=8oRjP8yj2Wo). You can read up some articles on this as well.
 
3. I've added your user `ris-tlp` as a collaborator for this repository. Login to github and accept the invite.
 
4. Let's use Visual Studio Code as the IDE for development. You can download and install the community version [here](https://code.visualstudio.com/download).
 
5. Define your local workspace. I like to keep my git projects under one folder and recommend yours to be `C:\workspace\`
 
6. Open git-bash and change your current directory to the local workspace. This command shell will use unix commands which is slightly different from the windows command prompt. That's ok, you'll learn along the way. The command is - <br><br>
`cd C:/workspace` <br><br>
To verify you're in the right place type in <br><br>
`pwd` <br><br>
The cmd will tell you the present working directory which should be `C:/workspace`<br>
 
7. Now comes the cool part, in the same cmd window, issue the following command - <br><br>
`git clone https://github.com/shaeqkhan/khan-omar.git` <br><br>
You should see a folder `khan-omar` in your workspace `C:\workspace\khan-omar`<br><br>
Message me once you're done, pat yourself on the back and then we'll talk about making the website.
 

# Next Steps
 
8. Get familiarized with the IDE, learn the common keyboard shortcuts from the help menu.
 
9. In the IDE, `File > Open`. Select the folder `C:\workspace\khan-omar`. You should see the project in the explorer.
 
10. In the IDE, press `ctrl + ~` . This should open the terminal window at the bottom within VS Code. Now you don't have to switch between the IDE and Git Shell to issue git commands. We'll do eveything from the IDE.
 
11. In the terminal window, type `git status` and you should see the following information - <br>
`On branch master` <br>
`Your branch is up-to-date with 'origin/master'.` <br>
`nothing to commit, working tree clean` <br>
We'll use git commands to interact with the local and remote repository. You can use this cheat sheet to learn the commands [here](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html). Read them atleast once and you'll remember the commands once you start to using them regularly.
 
12. It's good practice to "do a pull" on the repository before starting any new work. This brings down any new changes to the repository in your local workspace. <br>
`git pull origin master`
 
13. Create a new file `index.html` under `C:\workspace\khan-omar\index.html` <br>
This file exists in your local workspace. To push this file up to the github repository, there are a few additional steps.
 
14. In the terminal window, type `git status` <br>
This command shows you all the files that have changed, been added or removed in your repository (`khan-omar` project is the repository here, that's the terminology we use). You should see `index.html` in the list.
 
15. Now, type `git add .` <br>
This command starts tracking all the changed files in the repository and gets them ready to be saved. You can also track individual files by specifying their path, we'll try this later on.
 
16. Now, type `git commit -m "new file"` <br>
This command creates a "commit" with a group of all the files that were tracked for changes in the previous step. The contents within the double quotes is a brief message you can write to describe the work completed by the commit.
 
17. Now, type `git push origin master` <br>
This command pushes your change directly to the "master" branch.
 
18. Now try to add some content in `index.html` and repeat steps 14-17.
 
19. Git uses an interesting concept to manage work between different team members. Read more on branching model [here](https://www.atlassian.com/git/tutorials/using-branches). Feel free to watch some videos on this concept until you get a hang of the basic idea.
 
20. Now lets create a branch where you'll work on [this issue](https://github.com/shaeqkhan/khan-omar/issues/1). Type the following in the terminal window.<br>
`git branch fix-typo` <br>
You have created a branch `fix-typo` that only you can see. To verify - <br>
`git branch` <br>
This command lists all the branches you have on the local repository. You should see - <br>
`fix-typo` <br>
`* master` <br>
The * symbol and green color indicates that the "master" branch is the current working branch.
 
21. To switch to the new branch you just created - <br>
`git checkout fix-typo` <br>
To verify that the command went through - <br>
`git branch` <br>
You should see - <br>
`* fix-typo` <br>
`master` <br>
 
22. Now, open this file from the IDE file explorer and correct this typo, save the file `ctrl + S`
 
23. To view your changes in your branch - `git status`
 
24. To "commit" your changes to the local repository, <br>
`git add .` <br>
`git commit -m "fixes #1"` <br>
A couple of interesting things happen with this command - one, the typo you corrected gets saved with the local repository and the terminology used in the message indicates that you have worked on a particular issue on github and that will be linked to your code automatically. For more information, read [this](https://help.github.com/articles/closing-issues-using-keywords/).
 
25. Now we will push your typo correction in the new branch `fix-typo` to github. <br>
`git push origin fix-typo` <br>
You'll see a bunch of output lines and a success message. Go to https://github.com/shaeqkhan/khan-omar and in the "Code" tab, the top left corner has a dropdown "Branch: master". You branch should show up if you click on that.
 
26. Awesome! Your code is now on github but if you open the [issues section](https://github.com/shaeqkhan/khan-omar/issues), your fix still hasn't made it to the "master" branch. For this, you'll have to create a "Pull Request" - the terminology implies you're requesting me to pull your suggested fix into the main codebase. There are other formats used across different teams and we'll discuss them later.
 
27. To create a "Pull Request", go to https://github.com/shaeqkhan/khan-omar/pulls and click the "New pull request" green button. Select "base:master" and "compare:fix-typo". The "base" branch is the one you want to merge to. The "compare" branch is the one that has your work. The UI will show you the change you made. If things look good, click "Create pull request". I'll get an email once you do this and when I "accept" your request, you will see that issue #1 will close automatically.
 
28. We'll do some practice with git to get you comfortable first. Great job so far! If you understand this then you know enough to start contributing to open source projects.