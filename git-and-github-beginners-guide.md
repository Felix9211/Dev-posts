####Practical Guide for Git And Github Beginners.

![](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6wsuwwf2uvdedfu6c43q.webp)
##**Git and Github Explained**##
Git is a version control system installed on your computer that helps you manage and track changes in your code over time. It allows you to record progress through commits, which are saved snapshots or versions of your project.
GitHub, on the other hand, is an online platform that hosts Git repositories,enables you to store projects in the cloud, share code with others, collaborate with teams, and securely back up your work. *Think of Github as a Integrated Development Environment(IDE) as far as coding is concerned.*

###**Version Control Explained**##
This is a system that allows track  of changes over time. For context now this is the role that Git plays. Versio Control tools help in,
- Keeping record of every meaningful change
- Navigating to a previous verdion of what has been changed safely
- Collaborating with each others work without overwriting it
- Gives room for experimenting freely and safely

###**A Quick Guideline on Git Installation**###
1. Go to your browser and search Git official Website:https://git-scm.com/
2. Head to the Downloads:https://git-scm.com/install/
3. Choose the Operating System Version of your choice and downlod the prigram
4. Complete the Installation

The software unpacks other `exe files`alongside Git. Search for `Git Bash exe`and run
Configure your Git Commands as;

```
git config --global user.name "Your Full Name"
```
and

```
git config --global user.email "your.email@example.com"
```
You can verify the configuration entries by;

```
git config --global --list
```
####**Setting Up the SSH Keys**####
These are keys that bridge the Git Bash directly to your GitHub account Safely. *for context,think of Passkeys functionality*

#####Generating a new SSH Key in Git Bash######

```
ssh-keygen -t ed25519 -C"your.email@example.com"`
```
After entering the key press enter to activate and designate a default location`~/.ssh/id_ed25519`

Then add the SSH agent followed by your key as follows;

```
eval "$(ssh-agent -s)"
```
Press Enter to Activate the Key

From there you can copy your public key to the clipboard for later use in linking it to the GitHub as follows
- Log in to GitHub.
- Click your profile picture and select Settings.
- Navigate to SSH and GPG keys and click New SSH key.
- Enter a descriptive title for the key (e.g., "My Windows PC").
- Paste your SSH key into the provided field and click Add SSH key.

You can now test the connection by running:

```
ssh -T git@github.com

```

##**How to Push and Pull Code**##
In laymans terms, Push defines sending your local project to your github while pulls is the making of the changes.

Here is a step by step process of how to Push code;
1. Go to your Github account.
2. Create a new Repository.
3. Copy the repository Url.
4.Connect your local project by entering the command `git add`which enables git to start the tracking process of the project
5. Add the variables in the folder and enter the command `git add.` then commit your changes by entering`git commit -m "Added data cleaning script."`
6. Copy the Repository web address from GitHub `https://github.com/yourusername/repository-name.git` then Run it as follows;

```
git branch -M main
git remote add origin https://github.com/yourusername/repository-name.git

```
7. And Lastly,enter  `git push -u origin main`to Push your code on GitHub

Now, Inorder to Pull the code from Git, Here is how to approach it;
1. Go to the project Folder on Bash `cd repo-name`
2. Pull the recent changes`git pull`
3. From there  you can track the changes by entering `git status` and that gets the work done.

From what you observe right from this piece. The version controls tools are inevitable in the data analysis path.
Ensure you follow step by step guideline as it flows.