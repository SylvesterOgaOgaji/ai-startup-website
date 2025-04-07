# Hands-On Git Project: Collaborative Website Development with Git and GitHub

In this mini project, I create a step-by-step project to simulate the workflow of Tom and Jerry using Git and GitHub. This hands-on project will include installation of Git (Done from my earlier project), setting up a GitHub repository, cloning the repository, creating branches, making changes, and merging those changes back into the main branch.

![Project Introduction](./img/)

## Part 1: Setup and Initial Configuration

### 1. Install Git:

- Visit the [official Git website](https://git-scm.com/) and [download](https://git-scm.com/downloads) the version of Git for your operating system. Follow the installation instructions.

![Installing Git](screenshots/02_installing_git.png)

### 2. Create a GitHub Repository:

- Sign up or log in to [GitHub]().
- Click the "+" icon in the top-right corner and select "New repository."

![Creating New Repository](./img/1.%20click%20plush%20and%20new%20repo.jpg)

- Name your repository (e.g., "ai-startup-website") and initialize it with a README file.

![Repository Settings](./img/2.%20add%20name%20and%20readme%20file.jpg)


### 3. Clone the Repository:

- On your repository's page on GitHub, click the "Code" button and copy the HTTPS URL.

![Copy Repository URL](./img/3.%20copy%20clone%20link.jpg)

- Open your terminal or command prompt
- Create a folder named "git-project" in the folder where you are storing all related work. For example in the Desktop folder on your laptop, you may create a folder called "training".

![Create Project Folder](./img/4.%20makedir-changedir-clonegithubdir.jpg)

- Change directory into the "git-project"
- Clone (Download) the repository from Github using

```bash
git clone [https://github.com/SylvesterOgaOgaji/ai-startup-website.git]
```

![Clone Repository](./img/5.%20gitbranch-main.jpg)

Since you just cloned your repository, your branch is "main".

- Navigate into the repository you cloned:

```bash
cd ai-startup-website
```

![Navigate to Repository](./img/6.%20navigate%20tp%20the%20ai-startup-website.jpg)

- Create an empty file "index.html"

![Create index.html](./img/7.%20create%20empyt%20index%20and%20add%20content.jpg)

- Add the content below:

```
This is the Admin creating an index.html file for Tom and Jerry.
```

![Add Content to index.html](./img/7.%20create%20empyt%20index%20and%20add%20content.jpg)

- Check changes has not been staged:

```bash
git status
```

![Check Git Status](./img/8.%20stagging.jpg)

- Stage changes:

```bash
git add index.html
```

![Stage Changes](./img/9.%20main%20stagging.jpg)

- Confirm changes have been staged for commit:

```bash
git status
```

![Confirm Staged Changes](./img/10.%20Stagging%20confirm.jpg)

Now, after staging the changes, the file name will appear in green in the terminal output. This color change signifies that the file has been successfully staged, making it ready for the next step, which is committing these changes to the project's history.

- Commit changes:

```bash
git commit -m "This is my first commit"
```

![Commit Changes](./img/11.%20Push%20main%20branch%20to%20git.jpg)

This takes the staged changes and records them in the repository's history with a message describing what was done. This commit is a milestone, marking a specific point in the project's development.

- Push main branch to Github:

```bash
git push origin main
```

![Push to GitHub](./img/11.%20Push%20main%20branch%20to%20git.jpg)

This sends commits from your main branch on your laptop to GitHub (Remote Repository).

## Part 2: Simulating Tom and Jerry's Work

To simulate both Tom and Jerry working on the same laptop, you'll switch between two branches, making changes as each character.

### 1. Tom's Work:

- Navigate to the project directory you just cloned:

```bash
cd ai-startup-website
```

![Navigate to Project Directory](./img/12.%20navigate%20to%20clone%20github%20repo%20and%20check%20the%20branc.jpg)

This moves you into the folder containing the cloned GitHub repository on your local machine. It's like stepping into the project's workspace.

- Check the current branch: This shows you a list of all branches in your local repository. Initially, you'll see only the "main" branch because that's the default starting point and no other branches have been created yet.

```bash
git branch
```

![Check Current Branch](./img/12.%20navigate%20to%20clone%20github%20repo%20and%20check%20the%20branc.jpg)

- Create a new branch for Tom's work:

```bash
git checkout -b update-navigation
```

![Create Tom's Branch](./img/13.%20create%20a%20new%20branch%20for%20Toms%20work.jpg)

This creates a new branch named "update-navigation" (You can name it whatever you want). The command also automatically switches to the newly created branch from the "main" branch. This branch "update-navigation" is where you'll simulate Tom's updates to the website without affecting whatever is in the main branch.

Check the branch again to see your newly created branch.

```bash
git branch
```

![Check Branch After Creation](./img/14%20Tom%20branch%20is%20confirm.jpg)

Running git branch again now shows your newly created branch, indicating you're now working in this new "workspace" dedicated to Tom's navigation updates.

Recall you created an empty file "index.html" in the main. The file will also exist in the `update-navigation-branch`. Open the `index.html` and add the content below:

```
This is Tom adding Navigation to the AI-website
```

![Tom Modifies index.html](./img/15.%20Open%20up%20index%20dot%20html.jpg)
![Tom Modifies index.html](./img/14.%20Tom%20added.jpg)

This simulates Tom's contribution to the project. This text represents the work he's doing on the navigation bar. In the real world, this will be an actual software code.

Check changes has not been staged:

```bash
git status
```

![Check Tom's Unstaged Changes](./img/16.%20status%20not%20stagged.jpg)

At this stage, Tom has modified the file, but these changes haven't been prepared for a commit in Git. This is indicated by the file name appearing in red in the terminal output, signaling that the changes are recognized by Git but not yet staged.

- Stage Tom's changes:

```bash
git add index.html
```

![Stage Tom's Changes](./img/17.%20Toms%20branch%20has%20been%20staged.jpg)

This tells Git that you want to include the updates made to index.html in the next commit. It's like saying, "Okay, I'm happy with these changes and ready to record them."

- Confirm changes have been staged for commit:

```bash
git status
```

![Confirm Tom's Staged Changes](./img/18.%20confirms%20the%20stagging.jpg)

Now, after staging the changes, the file name will appear in green in the terminal output. This color change signifies that the file has been successfully staged, making it ready for the next step, which is committing these changes to the project's history.

- Commit Tom's changes:

```bash
git commit -m "Update navigation bar"
```

![Commit Tom's Changes](./img/19.%20Takes%20the%20stage%20and%20record%20it%20in%20the%20repo%20history%20with%20a%20message.jpg)

This takes the staged changes and records them in the repository's history with a message describing what was done. This commit is a milestone, marking a specific point in the project's development.

- Push Toms branch to Github:

```bash
git push origin update-navigation
```

![Push Tom's Branch](./img/20%20commit%20and%20push.jpg)

This sends Tom's commits from your local branch on your laptop to GitHub (Remote Repository). It's like publishing your work so that others (or in this case, "Jerry") can see and interact with it. This step updates the remote repository with Tom's contributions.

After completing Tom's workflow, you will now simulate Jerry's contribution to the project. To do this, you'll:

- switch back to the main branch,
- create a new branch for Jerry,
- make changes, and then
- stage, commit, and push these changes to GitHub.

### 2. Jerry's Work:

- Switch Back to the Main Branch:

```bash
git checkout main
```

![Switch to Main Branch](./img/21.%20switch%20back%20to%20main%20branch.jpg)

This command switches your current working directory back to the main branch, ensuring that Jerry's changes start from the latest version of the project.

- Pull the Latest Changes:

```bash
git pull origin update-navigation
```

![Jerry Pull Latest Changes](./img/22.%20pull%20changes%20from%20update-navigete%20to%20main.jpg)

This ensures that you have the latest updates from the repository, including Tom's merged changes, if any.

- Create a New Branch for Jerry's Work:

```bash
git checkout -b add-contact-info
```

![Create Jerry's Branch](./img/24.%20Open%20index%20dot%20html.jpg)

This creates a new branch where Jerry will make his changes, keeping them separate from the main project until they're ready to be merged.

- Open index.html and Add Contact Information: Make your changes to the index.html file by adding contact information. This simulates Jerry's task.

![Jerry Modifies index.html](./img/24.%20Open%20index%20dot%20html.jpg)

![Jerry Modifies index.html](./img/24.%20Open%20index%20dot%20html.jpg)

- Stage Jerry's Changes:

```bash
git add index.html
```

![Stage Jerry's Changes](./img/25.%20Stagging%20Jerrys%20work.jpg)

This command stages the changes Jerry made to the index.html file, preparing them for commit.

- Commit Jerry's Changes:

```bash
git commit -m "Add contact information"
```

![Commit Jerry's Changes](./img/26.%20Save%20jerrys%20changes%20in%20the%20branch%20history.jpg)

This saves Jerry's changes in the branch's history, with a message describing what was done.

- Push Jerry's Branch to GitHub:

```bash
git push origin add-contact-info
```

![Push Jerry's Branch](./img/26.%20Save%20jerrys%20changes%20in%20the%20branch%20history.jpg)

![Push Jerry's Branch](./img/27.%20checkout%20to%20main%20branch%20and%20pull%20from%20add%20dash%20contact%20dash%20info.jpg)
