# ***Git Tutorial: How to Use Git***

## *Step 1: Install Git and Create a GitHub Account*

The first thing you need to do is to install Git and create a GitHub account.

There are several different ways to install Git. Follow the instructions below to install Git on your system:

[Install Git on Windows](https://phoenixnap.com/kb/how-to-install-git-windows)  
[Install Git on Mac](https://phoenixnap.com/kb/install-git-on-mac)  
[Install Git on Ubuntu]( https://phoenixnap.com/kb/how-to-install-git-on-ubuntu)  
[Install Git on CentOS 7](https://phoenixnap.com/kb/how-to-install-git-on-centos-7)  
[Install Git on CentOS 8](https://phoenixnap.com/kb/how-to-install-git-centos-8)

>*Note: If you already have Git installed on your machine, it's best to update to the latest version available.
To update Git, follow the instructions in our article on [how to update Git](https://phoenixnap.com/kb/how-to-update-git) on Windows, macOS, or Linux.*

After installing Git on your machine, the next step is to create a free GitHub account.

Follow these steps:

1. Visit the official account creation page: [Join GitHub](https://github.com/join)

2. Pick a **username**, enter your **email address**, and choose a **password**.

3. Opt for or opt out of receiving updates and announcements by checking/unchecking the **Email preferences** checkbox.

4. Verify you're not a robot by solving the **Captcha** puzzle.

5. Click **Create account**.

    ![Create your account](https://phoenixnap.com/kb/wp-content/uploads/2021/09/create-an-account-on-github.png)

6. GitHub sends a **launch code** to the specified email address. Copy-paste the code in the designated field.

7. Optionally, enter account personalization details when asked or **Skip**, and click **Continue**.

You have now successfully created a GitHub account.

## Step 2: Create a Local Git Repository  

After installing or updating Git, the next step is to **create a local Git repository**. Our article explains in detail [what a Git repository](https://phoenixnap.com/kb/what-is-a-git-repository) is and how to create one.

To create a Git repository, follow the steps below:

1. Open a Git Bash terminal and move to the directory where you want to keep the project on your local machine. For example:

        cd ~/Desktop  
        mkdir myproject  
        cd myproject/
    In this example, we changed the directory to **Desktop** and created a subdirectory called *myproject*.

2. Create a Git repository in the selected folder by running the **`git init`** command. The syntax is:

        git init [repository-name]

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/create-git-repository.png)  
Now you have successfully created a local Git repository.

## Step 3: Create a New Repository on GitHub

GitHub allows you to keep track of your code when you're working with a team and need to modify the project's code collaboratively.

Follow these steps to create a new repository on GitHub:

1. Log in and browse to the GitHub home page.

2. Find the **New repository** option under the + sign next to your profile picture, in the top right corner.

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/create-repository-in-github.png)

3. Enter a name for your repository, provide a brief description, and choose a privacy setting.

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/github-repository-personalization.png)

4. Click the **Create repository** button. 

GitHub allows you to add an existing repo you have **created locally**. To push a local repository from your machine to GitHub, use the following syntax:

    git remote add origin https://github.com/[your-username]/[repository-name.git]
    git push -u origin master

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/push-local-repo-to-github.png)

## Step 4: Add a File to the Repository

Git notices when you add or modify files in the folder containing the Git repository but **doesn't track** the file unless instructed. Git saves the changes only for the files it tracks, so you need to let Git know you want to track changes for a specific file.

You can check which files Git is tracking by running:

    git status

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/git-status-command.png)

Git notifies you if you have any untracked files. If you want Git to start tracking a file, run the following command:

    git add [filename]

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/add-file-to-repository.png)

In this example, we instructed Git to start tracking changes for the test.txt file. Rerunning the git status command shows that Git is tracking the specified file.

## Step 5: Unstage Files on Git

Working with Git usually involves adding all the files to your index to prepare them for a commit. If you want to remove some files from the index before committing, you have to [unstage the files in Git](https://phoenixnap.com/kb/git-unstage-files).

One way to unstage files on Git is to run the **`git reset`** command. The syntax is:

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/unstage-file-in-git.png)

>Note: You can also use the **`rm`** command to unstage files on Git.  
>The syntax is: **`git rm --cached [file-name]`**.


## Step 6: Create a Commit

After adding the specified files to the staging environment, instruct Git to package the files into a commit using the **`git commit`** command. Git then stores that file version. You can review the stored version at any given time.

The syntax is:

    git commit -m "Notes about the commit"

Add a message at the end of the commit to state whether it's a new feature, a bug fix, or anything else. Commits remain in the repository, and they are rarely deleted, so an explanation of what you changed helps other developers working on the project or help you keep track of all the changes.

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/push-commit-on-git.png)


## Step 7: Undo Last Commit

>**Important:** Git allows users to [revert the last commit](https://phoenixnap.com/kb/git-revert-last-commit). However, other developers could have already retrieved the updated project, and deleting updates from one system could cause conflicts for other team members.

Use the **`revert`** and **`reset`** commands to undo changes and revert to a previous commit.  
To undo a published commit, use the following syntax:

    git revert [hash]

A hash is a code that identifies each commit. Obtain a commit hash by running:

    git log

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/undo-last-commit-on-git.png)

In this example, we first ran the **`git log`** command to obtain the commit hash and then reverted the last commit by running **`git revert`** with the commit hash we obtained.

## Step 8: Create a New Branch

The first branch in a git repository is called master, and it is the primary branch in a project.

[Creating a new Git branch](https://phoenixnap.com/kb/git-create-new-branch) means creating a copy of the project from a specific point in time. Branches in Git allow users to make new features without applying the changes to the main branch while the feature is in development.

The common method for creating a new branch is by running:

    git branch [new_branch_name]

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/create-a-new-branch-in-git.png)


## Step 9: Switch Branches

Having several branches of a Git project provides a test environment for developers to track progress without affecting the production version of an application. Git allows you to [switch between branches](https://phoenixnap.com/kb/git-switch-branch) with the **`checkout`** command easily. The syntax is:

    git checkout [branch_name]

Replace **`[branch_name]`** with the branch name you want to access.

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/switch-branch-in-git.png)


## Step 10: Rename a Local or Remote Git Branch

In Git, you can [rename a local or remote Git branch](https://phoenixnap.com/kb/how-to-rename-git-branch-local-remote).

The syntax for changing a **local** Git branch name is:

    git branch -m new-name

For example:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/change-branch-name-in-git.png)

In this example, we changed the local branch name from new-feature to feature-testing.

Since there isn’t a way to directly **rename a remote Git branch**, you first need to delete the old branch name, then push the new branch name to the remote repository.

## Step 11: Delete a Local or Remote Git Branch

You may decide to delete a Git branch after merging the changes with the master branch or if the branches become corrupted.

You can [delete local and remote Git branches](https://phoenixnap.com/kb/delete-remote-and-local-git-branch).

Deleting a local branch doesn't affect a remote branch. To delete a **local** Git branch, run:

    git branch -d [branch_name]

Use the following syntax to delete a remote Git branch:

    git push [remote_project] --delete [branch_name]

In this example, we deleted a local Git branch:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/delete-a-branch-in-git.png)


## Step 12: Set Upstream Branch

Sending something upstream in Git means that you are sending it back to the repository owner.

Using the **`git set upstream`** command, you can choose the flow direction of your current local branch. The command also allows you to change the default remote branch.

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/set-upstream-branch-in-git.png)

Our tutorial on [What Is Git Upstream and How to Set an Upstream Branch](https://phoenixnap.com/kb/git-set-upstream) deals with the different methods for setting an upstream branch and gives a detailed explanation on the topic.

## Step 13: Remove a Git Remote

A git remote is a connection to a repository hosted on a **remote server** – GitHub, BitBucket, GitLab, or any other remote location.

However, over time, the remote repository may move to another host, or a team member may stop working on the project. The remote in question is then no longer needed.

There are several ways to [remove a Git remote](https://phoenixnap.com/kb/git-remove-remote). One of the ways is to delete a remote using the command line. The syntax is:

    git remote remove [remote name]

In the following example, running **`git remote -v`** shows the available remotes, 'origin' and 'test-remote.' After removing 'test-remote' and rerunning **`git remote -v`** to list available remotes, we see that the only available remote is 'origin.'

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/remove-a-git-remote.png)

## Step 14: Git Merge

Git merge unifies **multiple commit sequences into a single commit**. It can combine two branches, thus integrating the independent development lines into a single branch.

After merging two branches, Git updates the current branch to reflect the merge, but the target branch isn't affected. That means you have to use the **`git branch -d`** command to delete the obsolete target branch.

For example, you may want to merge a new feature branch into the main branch. Follow the steps below:

1. Run the **`git status`** command to ensure that HEAD is pointing to the correct merge-receiving (master) branch. If it is not, run **`git checkout master`** to switch to the master branch.

    ![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/git-merge-first-step.png)

2. Run **`git fetch`** to pull the latest remote commits and **`git pull`** to ensure the main branch has the latest updates.

    ![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/git-merge-update.png)

3. Run **`git merge X`** where X is the name of the branch you want to merge into the receiving branch.

    ![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/git-merge.png)

## Step 15: Resolve Merge Conflicts

Merge conflicts usually occur when multiple developers work on the same code of a project or when they work with several development branches. Git merge warns the user about these conflicts.

Although most merge conflicts resolve **automatically**, there are cases when git merge **cannot resolve an issue**.

>**Note:** Our detailed guide on [How To Resolve Merge Conflicts in Git](https://phoenixnap.com/kb/how-to-resolve-merge-conflicts-in-git) offers tips for preventing merge conflicts, as well as ways to resolve existing merge conflicts.

## Step 16: Create a Pull Request

Create a pull request (PR) to inform a repository owner that they should **review the changes** you've made to their code. Then the owner can **approve the pull request** and merge the changes into the main repository.

If you are the co-owner or owner of a repository, you don't have to create pull requests to merge your changes. However, you can still do it to keep track of your feature updates and history.

For this guide, we will create a readme file for our repository locally and make a pull request on GitHub to illustrate the process.

Follow the steps below:

1. In [Git Bash](https://phoenixnap.com/kb/what-is-git-bash), create an empty readme file by running touch readme.md.

2. Create and switch to a new branch on which to modify the file. Run:

        git checkout -b create-readme-file

3. Open the readme file in a text editor and add the text you want it to contain. In this example, we will use the [Nano text editor](https://phoenixnap.com/kb/use-nano-text-editor-commands-linux) to modify the file within the command line window. Run **`nano readme.md`**.

    ![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/opening-a-file-in-nano-text-editor.png)

    >Note: Check out our list of 22 [best Linux text editors](https://phoenixnap.com/kb/best-linux-text-editors-for-coding).

4. After you save the file, track it by running **`git add readme.md`**.

5. Create a commit.

        git commit -m "Added a readme file"

6. Push the changes to GitHub.

        git push origin create-readme-file

7. Log in to your GitHub page. There is now a **Create pull request** option in your repository with the branch name we created in the command line. Click the **Compare & pull request** button.

    ![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/compare-and-pull-request-on-github.png)

8. GitHub states if you can merge the branches and apply the changes. Optionally, add a comment about your pull request and click **Create pull request**.

    ![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/create-pull-request.png)

Now the repository owner, in this case, you, can review the changes and accept or reject them.

You can accept the changes in the **Pull requests** tab on GitHub. When you merge the branches, delete the obsolete branch by clicking **Delete branch** to keep the repository clean.


## Step 17: Synchronize Changes on GitHub and Locally

When you merge changes on GitHub, they don't appear automatically in your local repository. You have to pull the changes to your local repository to see the updates.

Synchronize your local repository with GitHub by running:

    git pull origin master

The command updates your local repository to match the one on GitHub, and states the changes.

In the following example, we first switched to our master branch, and Git warned us that we should update our local repository:

![code](https://phoenixnap.com/kb/wp-content/uploads/2021/09/sync-git-and-github.png)

## Conclusion

You now know the basic and some more advanced Git functions. Feel free to test them out to make sure you understand how they work.

Download our [Git commands cheat sheet](https://phoenixnap.com/kb/git-commands-cheat-sheet) to have all Git commands in one place for future use.

### This article from [**phoenixnap.com**](https://phoenixnap.com/kb/how-to-use-git)

#### new line for test

##### readme1 branch