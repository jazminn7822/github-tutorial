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
**_Inorder to able to use https://ide.cs50.io/, you will have to create an account in https://github.com/._**
1. Go to https://github.com/
2. Click on "**Sign up**" on the top right corner.
3. **Create an account** (_If you are a student from HSTAT, you can use your HSTAT email, but without the `hstat.org`_).
4. After you have created an account, go to https://github.com/hstatsep/ide50 and follow the steps stated there. (_Do not skip this step. You **need** to go to this website which will help you set up your https://ide.cs50.io/_)
   * What is an SSH key and why do we need to set up an SSH key between cs50 and GitHub?
     * An SSH key is a way for your local and remote to be able to connect. In this case the SSH key was generated to use it as a way to identify yourself without having you type in your username and password every single time you will be making a commit.



---
## Repository Setup
1. Make sure you are in your https://ide.cs50.io/
2. First, **create a directory**. You can name it first-repo for this purpose or if you'd really like to name it otherwise, you can go right ahead. So, to create a directory named **first-repo** type `mkdir "first-repo"`in your terminal. `mkdir` means make directory. Not to complicated, right? :smile_cat:
3. Now, to make `mkdir "first-repo"` into a repository, you **need** to **go into the directory**. To do this, you need to type in the command `cd first-repo`. After you have typed this command, type in `git init` to **initialize git**. So, after typing in `mkdir "first-repo"` you need to type in `cd "first-repo"` and then `git init`. It should look like this :point_down:

         * `mkdir first-repo`
         * `cd first-repo`
         * `git init`
* It should now say `~/first repo/ (master)`
Now, lets make a README.md file inside this repository, so that we are able to type in any text we'd like in the README.md file.

  1. Type in `touch README.md` to create a new blank file named README.md inside our `first-repo` repository.
          It should look like this: `~/first repo/ (master) $ touch README.md`
  2. Then, type in `c9 README.md` to go open this file in a new tab in your ide.cs50
          It should look like this: `~/first repo/ (master) $ c9 README.md`
  3. You should now see 2 tabs next to eachother (The terminal tab and the README.md file) and you should have been automatically forwarded to the blank README.md file.
     * To save this file, you can either click on File > Save or command + S (On Mac) or Ctrl + S (On a PC)  (_Both options should have changed the color of the dot right next to the README.md from red to green_)


Congrats, you've just made your very first repository **and** file! :clap:

---
## Workflow & Commands

Now that we have a README.md file, we can start to type in this file any text we would like.
1. Make sure that we are still inside the blank README.md file.
2. Lets type in "This is my first repository."
3. Now that we have some text in the README.md file, lets click on our terminal tab again.
4. Now you should be in the terminal, type in `git add .` This command adds the file README.md  and its edits to the stage. This command can still be used even if you aren't 100 % sure of adding certain files or edits now or in the future, because what you are really doing is just telling Git what you would like to be recorded or commited when you do another command which will be in the next step.
5. Now that we have added everything to the stage, lets commit it. Type in `git commit -m "add text to first-repo"` What this command does is it "captures a photo of the stage" or records the change you have done by naming it "add text to first-repo". When writing commit messages, you should always use small phrases that are in the present-tense form. In the future, if you maybe want to get something back that you deleted in the past, you can type in `git log` to see all the commits you've done and get the one you'd like back by doing another command which is in the **_Rolling Back Changes_** section.
6. In order to do the last command, we need to go through some other steps first which are listed underneath _Git Push_. This command is known as `git push`, and it will push everything we have in our README.md file to github.com. For this, we will have to create our remote repo which will live in github.

  ##### _Git Push_

  * Visit http://github.com/, you should still be signed in.
  * Go to the top left corner and locate the green buton that has a little book and reads "New", then click on it.
  * You should now see the words, "**Create a New Repository**"
  * Type in the repository name. For this purpose, type in _first-repo_ **exactly** the same as you have it named.
  * When you're done, you can include a description if you would like, but you don't have to.
  * Skip the last step, because we already have a README file in our first-repo that we made in our ide.cs50.
  * Last but not least, click on the green button _Create Repository_
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

##### How do you undo an edit?
* To undo a edit you have to type in the command `git checkout --filename`. This command will normally discard an uncommited change.

##### How do you undo something you have added to the stage?
* To undo something you have added to the stage you have to type in `git reset HEAD filename`.

##### How do you undo a commit?
* To  undo a commit you would need to type, `git reset --soft HEAD~1`. This command will delete the last commit you've made and reset to a past commit you would like back.
##### How do you undo a commit, something you've added to the stage, and an edit?
* By doing `git reset --hard HEAD~1` you will be deleting the things you've just added to the stage and any uncommited changes.This is a _very_ dangerous command. Just make sure that you really want to delete something before typing in this command.

#####  How do you undo something that you have pushed already?
*  To undo a pushed commit you can do `git revert`. For instance,`git revert c79856b d67b689a e7g8t8i`. This command will delete the most recent commit, the commit before that, and the third-most recent commit. You could also do `git reset --hard HEAD~1` to remove 1 or multiple commits you have made in the past.
*
### ERROR HANDLING
###### What do you do if you do `git init` in the wrong directory?
Lets say you did git in a first-repo and you didn't want first-repo to be a repository yet. First, you would want to make sure that you have cd into first-repo by doing `cd first-repo` and then just type in the command ` rm -rf .git`. This command will uninitialize git and now you shouldn’t see master.
###### How do you remove a repository from your local cs50 ide and from your remote?
So to remove it from your local, you would just need to type in rm -rf <filename>. It will remove it without asking you if you are sure about deleting it, it will go right ahead. To delete a repository from your remote you would just go to Github.com. Next, you would have to click on your repository and underneath it there should be a settings icon. Click on it. Then, under Danger Zone, click on *Delete this repository.* Read the warnings and if that's really you, go ahead and type in the repository name. Verify that you're deleting the correct repository and click on **I understand the consequences, delete this repository.**

### Collaboration
What do I do if I would like to clone someone else's repository?
To clone someone else's reposirtory follow these steps.
1. Go to GitHub and you should be on their repository.
2. Locate the green _Fork_ square and click on it.
3. You should now see your username and their repository name.
4. Now locate the Clone or Download green button. Click on it and copy the link.
5. Now back in your ide.cs50.io, type in the command `git clone` and paste the link you copied.
6. Now you should see the repository you cloned on the left side of the screen!

What about pull requests?
So, after you have cloned and forked someone else's repository, you can decide if you would like to edit or make changes to their repository.
Lets say you did. Now, how can the owner of the repository see the changes you have made?
* After having made the edits, you should do `git push`  to push everything to the remote that lives in GitHub.
* You can go to GitHub and submit a pull request and if your pull request is approved then they would accept the changes.
* Lets say you were the person receiving the pull requests, you would have to accept the pull request and then just need to type the command `git pull` in your terminal and that is it.