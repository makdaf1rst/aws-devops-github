[README(1).md](https://github.com/user-attachments/files/25793961/README.1.md)
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Connect a GitHub Repo with AWS

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-devops-github)

**Author:** Saqib Hossain  
**Email:** saqibh49@gmail.com

---

## Connect a GitHub Repo with AWS

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-devops-github_dd9d254e)

---

## Introducing Today's Project!

In this project, I will demonstrate how to connect my web app project to a GitHub repo, push code changes, and set up a README. I'm doing this project to learn how developers use version control to track and share their code — something that's essential for working on any team or building a real portfolio.

### Key tools and concepts

Services I used were EC2, VS Code, Git, GitHub, and SSH. Key concepts I learnt include version control, initializing a local repo, staging and committing changes, pushing code to a remote repository, authenticating with GitHub using personal access tokens, and how local and remote repos stay in sync through Git commands.

### Project reflection

This project took me approximately 1 and a half hours. The most challenging part was getting authentication to work with GitHub since passwords don't work anymore and I had to figure out the personal access token setup. It was most rewarding to see my code changes show up in my GitHub repo after pushing — it made the whole Git workflow click for me.

I chose to do this project today because version control is something every developer and cloud engineer uses daily, and I wanted to get comfortable with the full Git workflow — from initializing a repo to pushing code to GitHub — so it becomes second nature.

This project is part two of a series of DevOps projects where I'm building a CI/CD pipeline! I'll be working on the next project in a few hours. 

---

## Git and GitHub

Git is a version control tool that tracks changes to your code and lets you collaborate with others by sharing your work through platforms like GitHub. I installed Git using the commands sudo dnf update -y to update my instance's packages first, then sudo dnf install git -y to install Git.

GitHub is a platform for hosting code repositories online, making it easy to store, share, and collaborate on projects. I'm using GitHub in this project to push my web app's code to a remote repo so it's backed up, version controlled, and visible in my portfolio.

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-devops-github_efaadbf7)

---

## My local repository

A Git repository is basically a folder that tracks every change made to the files inside it. It keeps a full history of what was changed, when, and by who — so you can always go back to a previous version if something breaks.

Git init is a command that turns a regular folder into a Git repository so it can start tracking changes. I ran git init in my web app's project folder to set it up as a local repo.

A branch in Git is basically a separate version of your code where you can make changes without affecting the main codebase. After running git init, the terminal confirmed that it initialized an empty Git repository and set the default branch to master, with a hint that I could rename it to something like main or development if I wanted.

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-devops-github_7bf21bae)

---

## To push local changes to GitHub, I ran three commands

### git add

The first command I ran was git add ., which adds all the files in my project folder to the staging area. A staging area is basically a holding zone where files wait before being committed — it lets me choose exactly what changes I want to include in my next commit.

### git commit

The second command I ran was git commit -m "Updated index.jsp with new content", which saves a snapshot of all my staged changes. Using '-m' means I can add a commit message right in the command instead of being taken to a separate text editor to write one.

### git push

The third command I ran was git push -u origin master, which uploads my committed changes to my GitHub repository. Using '-u' sets the upstream branch, so next time I push, I can just type git push without specifying the branch or remote again.

---

## Authentication

When I commit changes to GitHub, Git asks for my credentials because GitHub needs to verify that I'm authorized to push code to the repository. This prevents random people from pushing changes to repos they don't own.

### Local Git identity

Git needs my name and email because every commit is tagged with the author's identity — this way, anyone looking at the project's history can see who made which changes.

Running git log showed me a history of all the commits I've made to my repository, including the commit message, the author name and email, and the date and time each change was made.

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-devops-github_9a27ee3b)

---

## GitHub tokens

GitHub authentication failed when I entered my password because GitHub no longer accepts regular passwords for command-line access. Instead, I had to use a personal access token, which is a more secure way of authenticating that GitHub requires for pushing code from the terminal.

A GitHub token is a secure credential that acts as a replacement for your password when accessing GitHub from the command line. I'm using one in this project because GitHub doesn't accept regular passwords for pushing code anymore — the token is the only way to authenticate from my terminal.

I could set up a GitHub token by going to my GitHub settings, navigating to Developer Settings, then Personal Access Tokens, and generating a new classic token with the right permissions. Once generated, I used that token in place of my password when Git asked for my credentials.

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-devops-github_fa11169d)

---

## Making changes again

I wanted to see Git working in action, so I added a new line to my index.jsp file to test whether changes I make locally would show up in GitHub. I couldn't see the changes in my GitHub repo initially because just saving the file doesn't update the remote repo — I had to stage, commit, and push the changes first before GitHub would reflect them.

I finally saw the changes in my GitHub repo after running git add . to stage my changes, git diff --staged to preview what I was about to commit, git commit -m "added new line to index.jsp" to save the snapshot, and git push to send it all to GitHub.

![Image](http://learn.nextwork.org/grateful_white_lucky_bat/uploads/aws-devops-github_6becb2bc)

---

## Setting up a READMe file

---

---
