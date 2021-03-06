# gg-git-guide
## all commands that programmer needs while working on "git".

_the following file will be separated to 8 parts as follows._

|Part|Title|About|
|----|-----|-----|
|One |Basic Terminal Commands|Basic terminal commands that a developer must know to be able to work  with git.|
|Two|Git Basics|git main commands|
|Three|Git undoing things|git commands that are used to get bach in history, restore data, fix done mistakes, or change some data done previously.|
|Four|Basics Of Github|git commands that are used to push our repository from local machine to the internet, pulling and pushing requests, or clonning a project|
|Five|Working With Branches|git commands used to create,use, and delete branches. Branches make team work more simple and advanced.|
|Six|Merge Branches|git commands that works on merging the branches that the team worked on separately. In this part we will fix the conflict that coulde be hapened while working on a certain code.|
|Seven|Forking and Contributing||
|Eight|Collaboration||

***

## Now we had made a small introduction about what we will discuss in this guide. Let's start.

#### part One
> Basic Terminal Commands

In this file we will discuss the main terminal commands that you should know before start working with "git" or any software depending on termainals and command lines
if your familiar with this concept you can just skip this file and start with git.

1. the command `pwd` :

    * usually we use this command to know the path of our directory that we are working in.

2. the command `cd` :

    * this command is used to pass to a specific folder. For example if we have a folder named "new" and we want to enter it using a command, then we can use `cd new` .
If we want to go back to the latest folder or directory we use the command `cd ..` 

3. the command `mkdir` :

    * we use this command to create a new folder within our directory.

4. the command `touch` :

    * we use this command to create a new file (txt, html, css....) in the current directory.

5.  the command `ls` :

    * we use the this command to see the files that are already created in our current directory.

6. the command `mv` :

    * we use this command to change the name of a specific file. For example if we want to change the name of "index.html" file to "about.html" file, we use the command as follows :

`mv index.html about.html`

7.  the command `rm` :

    * we use this file to delete a file, for example if we want to delete our index.html file, we use the command as follows:

`rm index.html`

8. the command `rm -rf` :

    * we use this command to delete folder, the same as we had done in the above command (7).

9. the command `clear` :

    * we use this command to clear our command line window (power shell, cmd, windows termianl ....) from previous commands and lines.

10. the command `code` :

    * this command is used to open a file in vscode IDE. For example:
`code index.html`
then after clicking on enter the file index.html will be opened in vscode.

>Conclusion:
These are the main commands that we should know to be able to work with git and to deal with terminals.
***
#### Let us continue and start with "Git"

***
#### Part Two:

>Git Basics

##### What is git?
Git is a distributed version control system.
A system that records changes of your file/project and then you are able to recall any specific version or project later.


1.  `git init` :

    * this is the first command that we shoul use, it creates the .git directory to be able to use git within our project.

2. `git status` :

    * this command gives us on which branch we are working, and it also gives us the list of the untracked files that are not add yet to the staged area to be ready to be committed.

3. `git add` :

    * this command is used to add the untracked file to a the staged area. For example, we first create an index.html file. When created this file is by default untracked, and can't be included in a commit. For this reason we use the command "git add":
"git add index.html", then this file will be added to the staged area and can be now included within a commit. Moreover, we can use the command "git add ." or "git add -A" to add all the file within our current dirctory to the staged area.

4. `git rm --cached <file>` :

    * we use this command to remove the file from the staged area, and return it as an untracked file.

5. `git commit -m "commit name or title" `:

    * we use this command to make a new commit. After adding the files you want to the staged area, then they are ready to be included in a commit. For example, if we are working on the style of a login screen "login.css", we add the file to the staged area using "git add login.css", after that we can use the command "git commit -m "login screen style commit"
now there will be create a new commit under the name "login screen style commit".

6. `git config --global user.name "name" `:
7. `git config --global user.email "email" ` :

when using git, we have to specify a username and an email. Moreover, to set your name and email you have to use the above 2 commands, for example:
"git config --global user.name "hadi"
"git config --global user.email "ha.hassan2510@hotmail.com"

now I had set my username to "hadi" and my email to "ha.hassan2510@hotmail.com"

>note: If we want to know our current username and email we write the above command, but without mentioning the names, for example:
"git config --global user.name" // after clicking on enter, we will obtain the current setted username, and the same is done for email
"git config --global user.email // now we will obtain the setted email address.


8. `git log` :

    * this command shows us the history of our made commits in details.

9. `git log --oneline` :

    * this command shows us the history of our made commits, but each commit in oneline, more summarized than the above command.
***

>Conclusion of part two:
in this file we had discussed the main git commands, creating a new git directory, adding files to staged area, set username ane email, creating a commit, and viewing our commits history.
Let's go on to continue with more nice commands using git.

***
***

#### Part Three
> git undoing things

 In this file, we will discuss different ways that we can use in git to undo work that we had done while working on our project.

1. `git show HEAD` :

    * this command allows us to see our last commit that we had made.

2. `git show <id of the commit>` :

    * it allows us to see a specific commit which is according to the id that we had entered.
> note: we can view the id of each commit when using the history command "git log" or "git log --oneline".

3. `git show HEAD~1` :
    * this command let us see the last commit before the HEAD one.



4. `git checkout <file>` :

    * this command let us unmodify the changes that had done on a specific file, if we want to unmodify all the changes in all files we use the following command :
`git checkout .`

5. `the command "`git checkout <id of the commit>` :

 * this command let us go back in history to see the changes that were done during this commit only.

>Note: this command is a -read only- command, it means that the data will never be affected, it only get back in time to view some changes without changing any thing in our work(READ ONLY).

6. `git checkout master` :

    * it returns us to the latest commit (HEAD), so will be able to view all the previous commits.

>  git checkout is a read only method 

7. `git revert <id commit>` : 

    * this command deletes the changes that were made in the specified commit only.

8. `git reset --mixed<id>` :

    * this command deletes the commits from the history, but the changes that were done on the file will still and will not be deleted.
Moreover, if we use after that "git status", we will find that the files will be unstaged(red colored).

9. `git reset --soft<id>` :

    * this command deletes the commits from the history, but the changes that were done on the file will still and will not be deleted.
Moreover, if we use after that "git status", we will find that the files will still staged(green colored).

10. `git reset --hard<id>` :

    * this command deletes the commits and changes from the history. Moreover, when using the "git status" command the files will not be obtained neither staged nor unstaged.

11. `.gitignore` file :

    * every file included in the .gitignore file will be ignored from git commands.
for example, if we include a file named "script.js" in the .gitignore file, the script.js file will be ignored from all the git commands that we are using during our work.

***

> Conclusion of part three :
In this section we had discussed the commands that we usually use to undo some work.

* git checkout
* git revert
* git reset (mixed, soft, and hard)

Let's go.

***
---

#### Part Four
> Basics og Github

What is github?
It is an online service where you can share your code of files in order to collaborate with different people.


The first thing we have to do is signing in to www.github.com, and create our first repository.
Then we have to start writing some command on our local machine inorder to push our local project to our online account on github.
***

1. the command `echo "# gitProject" >>README.md`

    * this command creates a readme file in our project.


> note: till now we should have already created our git dirctory using the "git init" command, and making at least one commit.


2. the command `git remote add origin https://github.com/<our account name>/<our project name>.git` :

    * this command connects our local repository to github.


> note: we have to set our user.name and user.email that we had discussed in previous file "Git-Basics".


3. the command `git push origin master` :

    * this command push our local repository to our online repository, and now all of our project will be seen on github.

***








