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
2. To make `mkdir "first-repo"` into a repository, you need to **go into the directory** by doing `cd first-repo` and then **initialize git**. So, after typing in `mkdir "first-repo"` you need to type in `cd "first-repo"` and then `git init`. It should look like this...

         * `mkdir first-repo`
         * `cd first-repo`
         * `git init`
* It should now say `~/first repo/ (master)`
Make some edits, add commit and push

Congrats, you've just made your very first repository! :wink:

---
## Workflow & Commands



---
## Rolling Back Changes