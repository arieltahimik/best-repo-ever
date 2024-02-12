# best-repo-ever

## Overview of the GitHub Workflow  
The GitHub flow is a lightweight workflow that lets you experiment with new ideas safely, without fear of compromising a project. The main steps are:  
  
1. Create a branch off of main  
2. Make commits  
3. Open a pull request  
4. Collaborate  
   - Make more commits  
   - Discuss and review code with team members  
5. Deploy for final testing  
6. Merge your branch into the main branch 
  
The local and remote repositories only interact when you run one of the four network commands in Git:  
`git clone, git fetch, git pull, and git push`  
  
## To work locally on a repository  
You first need to create a clone on your machine. To clone a repository, follow these steps:

1. In GitHub, click the Code tab of the repository you just created.  
2. Click the Code button.  
3. Copy the clone URL to your clipboard.  
4. Open your command line application. If you are on a Mac or Linux, you can use your terminal. If you are on Windows, we recommend you use Git Bash, which comes installed with Git.  
5. Retrieve a full copy of the repository from GitHub: `git clone <repo-name.git>`. Replace with the clone URL you copied above.  
6. Once the clone is complete, navigate into the new directory created by the clone operation: `cd best-repo-ever`  
  
## Configure Your Local Environment  
Before you can make changes to your code, you need to set a few basic configurations. You typically only need to set these configurations once. Git lets you set configuration options at three different levels. Check out these config command options.  
  
### Command Option -> Description  
  
`git config --system` -> These are system-wide configurations. They apply to all users on this computer.  
  
`git config --global` -> These are the user-level configurations. They only apply to your user account.  
  
`git config --local` -> These are the repository-level configurations. They only apply to the specific repository where they are set.  

The default value for git config is --local.  
  
### Git adds several configurations automatically
Type `git config --list` to see config settings from all three levels.  
  
### Git uses the config settings for your *user name* and *email address* to generate a ***unique fingerprint*** for each of the commits you create. 

*You **can't create commits without these settings**, so set them yourself using your command line application:*

`git config --global user.name "First Last"`  
  
and then enter,  
  
`git config --global user.email "you@email.com"`  
  
### Configure autocrlf 
Next, we set `core.autocrlf` (autocrlf stands for auto carriage return line feed). Different systems handle line endings and line breaks differently. If you open a file created on another operating system and do not have this config option set, Git will think you made changes to the file based on the way your operating system handles the line endings.  
  
For Windows users enter:  
   
`git config --global core.autocrlf true`  
  
For Mac or Linux users enter:  
  
`git config --global core.autocrlf input`  
  
THIS CHANGE FROM new-branch-2  
  