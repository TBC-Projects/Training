# Club Git Tutorial: Workflow
This tutorial assumes you have completed our [Git Setup Tutorial](https://github.com/TBC-Projects/Training/blob/main/gitSetup.md). If you haven't, go back and complete that first.

You can follow this workflow everytime you make changes with Git. Hopefully, it will become second nature after a few times!

## Preparing to Make Changes
### Fetch
Before you can make any changes, you must make sure you have the latest version of the project. For your computer to know what changes have been made by others, you'll need to fetch the latest changes.
```bash
git fetch origin main
```
You can also complete this step by clicking the "Fetch From All Remotes" button in the Git tab of VS Code.
### Status
Now you can check the status of your local copy of the project:
```bash
git status
```
You will now either be _ahead_ or _behind_ the origin project. If you are up-to-date, you can skip to "**Making Changes**"
### Behind (pull)
You are most likely behind the origin project. This means others made changes while you were away. You'll want to pull these updates before changing anything yourself:
```bash
git pull
```
You can also complete this step by clicking the "Pull" button in the Git tab of VS Code.
You are now ready for "**Making Changes**".
### Ahead (reset or stage changes)
There are sometimes situations when you are ahead a commit and you are not supposed to be. 
* A commit was reverted in the origin
* You committed to the main branch when you shouldn't have
* You made commits locally before but never pushed them, and now they are outdated
In these cases, you'll have to reset your local repository:
```bash
git reset --hard origin/main
```
You are now ready for "**Making Changes**".
## Making Changes
You can now make any edits, additions, removals, etc within the repository folder that you can think of! Make sure to save your changes.
## Staging Changes
Staging changes is about telling Git which changes you want to be actually added to the project.
### Add All
In most cases, you'll want to add all your changes:
```bash
git add .
```
In VS Code, click the ``+`` button next to "Changes" in the Git tab.
### Add Specific File
If you want to add specific file(s) that you changed:
```bash
git add ./<filename>
```
In VS Code, click the ``+`` button next to the target file in the Git tab.
## Committing Changes
Committing changes is actually adding the changes you made to the project in Git. You'll include a message with each commit:
```bash
git commit -m "Quick description of changes"
```
In VS Code, type a message in the "Message" box and click the blue "Commit" button.
### Status
Now that you have made commits, they should show up in your status:
```bash
git status
```
This should show you ahead! Now it's time to send your changes to the origin.
## Pushing Changes
Push your changes to the origin:
```bash
git push origin <branchname>
```
In VS Code, cick the Push Button in the Git tab.
If all went successfully, you are ready to open a **Pull Request**.
## Pull Request
Open up your repository in GitHub again. Select your personal branch. You should now see a green button that says **Compare & pull request**.
Click on that button.
### Writing a Good Pull Request
1. Short but descriptive Title
2. Follow this example format for the Body:
```markdown
# Description of Changes
## Improvements to Hello.c
* Fixed syntax errors
* More descriptive comments
## Update README.md
* Added Lesson Learned about C syntax
```
Leads will review and approve/deny your pull request. You can assign your lead as a reviewer which will send a notification.
## Tips and Help
### Tips
* Always pull before working.
* Commit frequently.
* Use descriptive commit messages.
* Never push directly to main.
### Help
Need help? Make a post in [#git](https://discord.com/channels/1161436362067677225/1306411719660273774).
