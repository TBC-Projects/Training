# Club Git Tutorial: Setting up your Environment

This tutorial will guide you through using Git, Git Bash, VS Code, and GitHub for our club projects. Even if you’ve never used Git before, follow these steps carefully. Already setup? Go to [workflows](https://github.com/TBC-Projects/Training/blob/main/gitWorkflow.md).

## What is Git?

Git is a version control system. It tracks changes to files in a project so multiple people can collaborate safely.

### Key terms:

* Repository (repo): The project folder that Git tracks.

* Commit: A saved snapshot of changes.

* Branch: A separate workspace for your changes.

* Pull Request (PR): A request to merge your branch into main.

* Origin: The remote repository on GitHub.

## Install Git & VS Code

### Windows Users (via WSL)

1. Install WSL and a Linux distro (e.g., Ubuntu): [https://learn.microsoft.com/en-us/windows/wsl/install](https://learn.microsoft.com/en-us/windows/wsl/install)  
2. Open your WSL terminal and install Git:

```bash
sudo apt update
sudo apt install git
```  
3. Install VS Code: https://code.visualstudio.com/

4. Install the Remote - WSL extension in VS Code.

### Mac Users (via Xcode)
1. Use Xcode to install Git and/or any other tools you need for The Boring Club
```zsh
xcode-select --install
```
2. Install VS Code: https://code.visualstudio.com/

## Configure Git
Open WSL terminal (Windows) or Terminal (Mac):
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```
## Clone the Repository
```bash
git clone <repo-url>
cd <repository-folder>
```
## Create your Branch
Go to your repository page on GitHub
* Click on branch dropdown (it will likely say main)
* Type in the name you will use for your personal branch
* Click "create branch <name> from main"

Congratulations, you are now ready to make changes!
