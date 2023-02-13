# Git and Github
## Git
Git is a version control system that allows you to track changes to files and collaborate with others. It is a distributed version control system, meaning that each developer has a full copy of the repository on their local machine. This allows for offline development and the ability to work on multiple branches at once. Git is a command line tool, but there are many graphical user interfaces (GUIs) that can be used to interact with Git. The most popular GUI is [GitHub Desktop](https://desktop.github.com/). GitHub Desktop is a GUI for Git and GitHub, which is a web-based hosting service for Git repositories.

### Setting up git:
For linux go to terminal and type the following commands:
```bash
sudo apt-get install git
```
To check if git is installed type:
```bash
git --version
```
To configure git type:
```bash
git config --global user.name "Your Name"
git config --global user.email "Your Email"
```

### Creating a repository:
To create a repository, you must first create a directory for the project . Then, navigate to the directory and type:
```bash
git init
```
Now you have a local repository. You can now edit files and local changes will be tracked. To see the status of the repository type:
```bash
git status
```
To add files to the staging area type:
```bash
git add <file>
```
To commit changes to the repository type:
```bash
git commit -m "Commit message"
```