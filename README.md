# GitHub Tutorial

_by Jazmin Nugra_

---
## Git vs. GitHub

#### _What is Git?_
Git is a version control system that runs in the command line. A version control system means that if you were working on a file and you decide to edit, delete, or move things, git will allow us to keep a picture or a snapshot of the code. This will help us see the changes we have made in the past and will allow us to get something back if we would like. The good thing about Git is that we can use it without having to use GitHub.
#### _What is GitHub?_
GitHub is a website that saves your code to the cloud. It is very useful when you would like to collaborate with others on a certain file or project from anywhere in the world. GitHub also gives you the ablility to interact with other repositories and visually track the past changes or commits they have done to their projects. Furthermore, GitHub does require git.



---
## Initial Setup
Inorder to able to use https://ide.cs50.io/, you will have to create an account in https://github.com/.
1. Go to https://github.com/
2. click on "**Sign up**" on the top right corner.
3. **Create an account** (_If you are student from HSTAT, you can use your HSTAT email._)
4. After you have created an account, go to https://github.com/hstatsep/ide50 and follow the steps stated there.
   * What is an SSH key and why do we need to set up an SSH key between cs50 and GitHub?
     * An SSH key is a way for your local and remote to be able to connect. In this case the ssh key was generated to use it as a way to identify yourself without having you type in your username and password every single time. This is why we need to set up an SSH key, so that we can log into our ide.cs50 without a password.



---
## Repository Setup
1. First, **create a directory**. You can name it first-repo or whatever you'd like. Do this by typing in `mkdir "first-repo"`
2. Now, to make `mkdir "first-repo"` into a repository, you need to **go into the directory** by doing `cd first-repo` and then `git init` to **initialize git**. So, after typing in `mkdir "first-repo"` you need to type in `cd "first-repo"` and then `git init`. It should look like this...

         * `mkdir first-repo`
         * `cd first-repo`
         * `git init`
* It should now say `~/first repo/ (master)`
Now, lets make a README.md file inside  so that we are able to type in any text we'd like in the README.md file.

  1. Type in `touch README.md` to create a new blank file inside our directory named README.md
          It should look like `~/first repo/ (master) $ touch README.md`
  2. Then, type in `c9 README.md` to go open this file in a new tab in your ide.cs50
          It should look like  `~/first repo/ (master) $ c9 README.md`
  3. You should now see 2 tabs next to eachother and you should be in the blank README.md file.
     * To save this file, you can either click on File > Save or command + S (On Mac) or Ctrl + S (On a PC)  (_Both options should lead you to the red dot changing to the color green_)


Congrats, you've just made your very first repository AND file! :clap:

---
## Workflow & Commands

Now that we have a README.md file, we can start to type in this file any text we would like.
1. Make sure that we are inside the blank README.md file.
2. Lets type in "This is my first repository."
3. Now that we have some text in the README.md file, lets click on the first-repo tab. **insert image**
4. Now you should be in the terminal, type in `git add .` This command adds the file README.md  and its edits to the stage. This command can still be used even if you aren't sure of adding certain files or edits, now or in the future because you are just telling Git what you would like to be recorded or commited when you do another command which will be in the next step.
5. Now that we have added everything to the stage, lets commit it. Type in `git commit -m "add text to first-repo"` What this command does is it "captures a photo of the stage" or records the change you have done before by naming it "add text to first-repo". When writing commit messages, you should always use small phrases that are in the present-tense form. In the future, you want to get something back that you maybe deleted in the past, you can type in `git log` to get see all the commits you've done and get the one you'd like back by doing another command which is in the **_Rolling Back Changes_** section.
6. In order to a command known as `git push`, we will have to create our remote repo in order to push the text we have in our file somewhere and we need to go through some other steps first.

  ##### _Git Push_

  * Open up a new tab and go to http://github.com/
  * Go to the top left corner and locate the green buton that has a liitle book and reads "New", then click on it.
  * You should now see this on your screen
  * Type in the repository name. For this purpose, type in _first-repo_ **exactly** the same as you have it named.
  * When you're done, you can include a description if you would like, but you don't have to.
  * Skip the last step, because we already have a README file in our first-repo that we made in our ide.cs50.
  * Click on the green button _Create Repository_
  * Now you should see the words "_Quick Setup -- if you've done this kind of thing before_". Below this you should also see a sub heading "_...or push an existing repository from the command line_ " and below that are 2 lines of code. There is `git add remote origin` and then a URL. There is also `git push -u origin master`.
       *   What does the command`git add remote origin (URL)` do?
            * This command sets up a connection between our repository in our CS50 IDE and the new repository that lives on GitHub. The URL should be github.com:_yourusername_/first-repo.git
       *  What does the command `git push -u origin master` mean?
            *  This command is done inorder to send any changes or edits we've made from our local CS50 IDE to our remote repo which is on GitHub. The -u means upstream which means that it will remember to push our changes to our remote repo whenever we type in `git push` in the future.
   * Copy those 2 lines of code and then paste them into your command line in the CS50 IDE. Make sure you are in your first-repo.
   * Now go back to github and refresh the page and now you should see "This is my first repository."
   * Now keep adding any text you'd like and repeat the steps you've done already by doing git add, git commit, and git push.

Hooray, you've learned how to do these three commands! :thumbsup:



---
## Rolling Back Changes
In order to dicard any changes we would have to do the command `git checkout --<file>...`
##### How do you undo an edit?
* To undo a edit you have to type in the command `git checkout --filename`.

##### How do you undo something you have added to the stage?
* To undo something you have added to the stage you have to type in `git reset HEAD filename`.

##### How do you undo a commit?
* To  undo a commit you would need to type, `git reset --soft HEAD~1`. This command will delete the last commit you've made and reset to a past commit you would like back.
##### How do you undo a commit, something you've added to the stage, and an edit?
* By doing `git reset --hard HEAD~1` you will be deleting the things you've just added to the stage and any uncommited changes.

#####  How do you undo something that you have pushed already?
*  To undo a push commit you can do `git revert`. You could also do `git reset --hard HEAD~1` to remove 1 or multiple commits you have made in the past.