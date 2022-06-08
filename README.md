# Getting Started With GitHub
# What is GitHub ?
<center>
<img src="https://u.cubeupload.com/DROIDXXX/GitHubMarkLight120px.png" width="120" height="120" />
</center>

In short, GitHub is an online software development platform used for storing, tracking, and collaborating on software projects. It enables developers such as yourself to upload their code files and to collaborate with fellow developers on open-source projects.

# What is Git ?
Git is open-source version control software, used for managing and tracking file revisions. It can be used with any file type, but is most often used for tracking code files. Git is the most widely used version control system in software development, and GitHub leverages this technology for its service, hence its name.

You've likely interacted with Version Control before without knowing it. One example would be Google Docs or Microsoft Word (365 Version) which has a “Version History” tool where you can view changes to the document at different points in time.

Advanced version control is necessary for software projects, especially collaborative/group ones. When building software, developers are frequently and simultaneously updating the code to add features and fix bugs. 

It wouldn’t make sense to make these changes to the source code directly, since any issues would affect users and the code itself. Instead, developers work with their own copies of the code, then — after the code has been thoroughly tested — add this code to the main codebase.

That seems all well and good. But, with multiple contributors, things can get very messy very quickly if there’s no way to combine everyone’s contributions into one unified codebase or see who contributed what changes. These changes also must be tracked and stored in case something breaks and the developers need to backtrack and restore a previous version.

This is what Git is for. When a developer wants to make a change to the software, they download their own copy of the source code from its central storage location (called a repository, or “repo” for short) to their local system, make modifications safely to their own copy, then merge their revised copy back with the source files in the repository along with comments explaining the changes. Git tracks all of these modifications and stores previous versions as backups.

# Key Terms To Remember:
## **Repository/Repo**
A repository contains all of your project's files and each file's revision history. Put simply, it's basically a cloud copy of your source code which you can view the version history of, see file changes over time, revert to an older version, collaborate & more.

## **Commits**
At GitHub, changes are called commits.

Each commit (change) has a description explaining why a change was made.

## **Branch**
When you have working code and need to make changes but unsure whether your changes will result in breaking the software, you can use a branch. For example, you could add a 'Feature' branch. Once you have tested this 'Feature' branch, you can simply merge it with the Main branch.

Use a branch to isolate development work without affecting other branches in the repository. Each repository has one default branch, and can have multiple other branches. You can merge a branch into another branch using a pull request.

> The **Main** branch is meant to be stable, and it is the social contract of open source software to never, ever push anything to master that is not tested, or that breaks the build.

>Instead, everyone uses branches created from **Main** to experiment, make edits and additions and changes, before eventually rolling/merging that branch back into the **Main**** once they have been approved and are known to work. **Main** is then updated to contain all the new stuff.

## **Pull Request**
You'll mostly come across this in collaborative projects. Let's assume you are working with a team of 3 people and each person is focussing on 1 aspect of the project. 

In order for all of you to push your changes at the same time without interfering with the other’s work, you create a **branch** (a separate development area — where your team members can work on their own tasks). Meanwhile, you continue working in your branch.

Once your friend finishes their work, they can make a **pull request** asking to combine their work with yours. If you approve, you can merge your branches, and thus your code.

As mentioned before, branches help you prevent situations in which your main or stable branch breaks due to changes made.

## Why Use GitHub?

- It makes it easy to collaborate on projects
- It's safer - Thanks to it's Version Control System
- Cloud Based - Your projects are safe even if your laptop crashes
- Track all file changes as well as who made the change and why
- Easy to integrate with coding software such as Visual Studio

---
# Installing & Setting Up Git on Your PC
1. Install the [latest version of Git](https://git-scm.com/downloads) on your device. You’ll need Git installed to work with your GitHub repository. 

You can refer to [THIS YouTube Video](https://www.youtube.com/watch?v=4xqVv2lTo40) on how to install Git on your PC.

2. After installing Git, go to [GitHub’s website](https://github.com/signup) and create an account with your email address.

3. Once your GitHub account is set up, you’ll be taken to your dashboard. To start your first repository, click Create repository on the left side OR Click the **+** icon on the Nav Bar at the top.

![Create Repo](https://u.cubeupload.com/DROIDXXX/2231.png)

![Create The Repo](https://u.cubeupload.com/DROIDXXX/ghrepo.png)

* **Add a name for your repository** - Names should be unique within your account so you cannot have 2 projects called **Task-1** in the same account.
* **Add A Description** - This part is optional. You can add it if you want to OR you can add it later.
* **Select The Visibility** - This one is important. For Private projects such as assignments or personal works which you do not want to showcase to the world *yet*, select PRIVATE. Only select PUBLIC if you want the project to be visible to everyone.

*NOTE: Private Projects are ONLY VISIBLE TO YOU!*

* Adding a README: A README is typically a Markdown document (.md format) which gives people information about your project. To understand the syntax for Markdown documents, you can simply visit [this website](https://www.markdownguide.org/basic-syntax/)
* .gitignore - This is basically a template which tells GitHub to ignore certain files. It's more common with JS and other type of projects which have a lot of dependencies and adding them all to GitHub will result in a very large file. 

**Note:** *Use with caution & double check the template to ensure you do not have files that are required in folders that are excluded by the .gitignore template.*

NOTE: If you want the easiest/fastest possible experience pushing your project to GitHub, without facing any issues, then it's better to add a README, .gitignore and License last.

# Pushing Your First Repository to GitHub
## The Easy Way!

![First Project](https://u.cubeupload.com/DROIDXXX/myfirstproject.png)

On the repo creation page, I filled in the Repository Name & Description. I set the visibility to Private and **did not include any files**!

Since I did not add any files to the repository, I see the following page:
![Creation Page](https://u.cubeupload.com/DROIDXXX/1stProj.png)

I can simply follow the steps listed on this page to push my existing project to GitHub.

## Here's What That Looks Like:

![SS](https://u.cubeupload.com/DROIDXXX/ss1.png)

Navigate to where your project is stored on your PC, clear the top bar, type 'cmd' and hit 'Enter'. A command prompt will open up at this destination.

## Initialize The Repository
To do this, simply run the following command in your command prompt.

```sh
git init
```
You should get the following message:
> Initialized empty Git repository in D:/Downloads/My First GitHub Project/.git/

The next step is to add your existing files which you will be committing. To do this, simply type:

```sh
git add .
```
NOTE: There is a full stop (.) in the command. This '.' simply means 'all'.

The next step is to add a commit message. You can do this by typing the following:
```sh
git commit -m "Adding My Project To GitHub"
```

The next step is to specify a Branch. We use the **Main** branch and therefore we need to type the following command:
```sh
git branch -M main
```

Now we can simply copy this line from the GitHub Page (Shown in Step 1):
```sh
git remote add origin https://github.com/r1337x/My-First-Project.git
```
Lastly, we simply push our local project to our remote like so:
```sh
git push -u origin main
```

Refresh the GitHub Page and you should see your project:
![SS2](https://u.cubeupload.com/DROIDXXX/ss2.png)

# Example 2  
## You Are Trying To Connect A Local Repository To A Remote Which Has A README, .gitignore & a License File

For this example, we assume you created a repo and added and README etc. Once the repo is created, you see this page instead of the page telling you what commands to type.

![SS3](https://u.cubeupload.com/DROIDXXX/SS3.png)

If you tried pushing to this repo by following the steps above, you should see the following error:

>error: src refspec master does not match any.  
error: failed to push some refs to 'ssh://xxxxx.com/project.git'

# The solution:

## Initialize The Repository
To do this, simply run the following command in your command prompt.

```sh
git init
```
You should get the following message:
> Initialized empty Git repository in D:/Downloads/My Second GitHub Project/.git/

Thereafter add the origin like so:
```sh
git remote add origin https://github.com/r1337x/My-Second-Project.git
```
We got the URL by clicking the Green button on our repo titled 'Code' and copying the URL displayed.

Thereafter we need to 'pull' those extra files  our remote has which we don't. We can do this by typing the following command:
```sh
git pull origin main
```

The next step is to add your existing files which you will be committing. To do this, simply type:

```sh
git add .
```
NOTE: There is a full stop (.) in the command. This '.' simply means 'all'.

The next step is to add a commit message. You can do this by typing the following:
```sh
git commit -m "Adding My Project To GitHub"
```

The next step is to specify a Branch. We use the **Main** branch and therefore we need to type the following command:
```sh
git branch -M main
```

Lastly, we simply push our local project to our remote like so:
```sh
git push -u origin main
```

![SS4](https://u.cubeupload.com/DROIDXXX/SS4.png)

Now our files are displayed on GitHub!

# Troubleshooting
**NOTE: Every problem you'll ever face, has been faced before. Therefore, the best solution is to simply Google search the error message and there's a 99% chance you'll find the solution on StackOverflow or similar websites**
