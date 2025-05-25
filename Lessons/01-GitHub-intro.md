# Getting familiar with GitHub

This module gets you up to speed on the most common GitHub features and makes sure you have the necessary knowledge for the rest of the GitHub Copilot workshop. Feel free to skip as much as you need, if you are already familiar with the knowledge.

## Create a GitHub account (if necessary)

Creating a new GitHub account is a straightforward process. Here are the steps to follow:

1. **Visit the GitHub Website**
   - Open your web browser.
   - Go to the GitHub homepage at [https://github.com](https://github.com).

2. **Sign Up**
   - On the GitHub homepage, you'll find a sign-up section.
   - Enter your desired username, email address, and a password.
   - Click on the “Sign up for GitHub” button.

3. **Verify Email Address**
   - After signing up, GitHub will send a verification email to the address you provided.
   - Check your email inbox and open the verification email from GitHub.
   - Click on the verification link in the email to confirm your account.

4. **Complete Setup**
   - Once your email is verified, you may be prompted to complete your account setup.
   - This could involve answering questions about your planned use of GitHub, opting into or out of newsletters, and setting up a profile picture.
   - You may also be offered a brief tutorial or guide on using GitHub.

5. **Choose a Plan**
   - GitHub will ask you to choose a plan. There are free and various paid plans, depending on your needs.
   - For most individual users and for learning purposes, the free plan is sufficient.
   - Select your plan and click on “Continue.”

6. **Optional: Configure Additional Settings**
   - Once your account is set up, you can further configure your profile.
   - You can add more details to your profile, such as a bio, company, location, and a website or blog link.
   - You can also explore settings related to security, notifications, and integrations.

7. **Start Using GitHub**
   - After completing these steps, you're ready to use GitHub.
   - You can now create repositories, collaborate on projects, contribute to open source, and more.

Remember, choosing a strong and secure password is crucial for your GitHub account, especially if you will be working on private or sensitive projects. Consider multi-factor authentication as an added security precaution. 

## Create a new repository

Absolutely, let's tailor the instructions to creating a classic snake game, where players find specific words hidden in a grid of letters. Here's how you can proceed with setting up a repository for this project on GitHub:

1. **Log into Your GitHub Account**
   - Open your web browser and navigate to [GitHub](https://github.com).
   - Enter your username and password to log in.
2. **Create a New Repository for the snake Game**
   - Click on the "+" icon in the upper right corner and select "New repository" from the dropdown menu.
   - **Repository Name**: Enter a descriptive name like `SnakeGameModule1`.
      - **Note**: We'll be using the repository you 'forked' earlier for the remainder of the exercise, so this repository is just to learn the ropes.
   - **Description**: Provide a brief description, e.g., "A classic snake  game built in [programming language/technology you are using]."
   - **Visibility**: Choose whether your repository should be public or private.
3. **Initialize the Repository**
   - **Initialize with README**: Check this box to create a README.md file. You can later edit this file to describe your snake game, how to play it, and how to set it up. All repositories should fill this file out to welcome new contributors and get them started.
   - **Add .gitignore**: If you are using a specific programming language or framework, select the corresponding .gitignore template. This will help to ignore unnecessary files from being tracked by Git.
   - **Choose a license (Optional)**: Select an appropriate license for your project. For open-source projects, common choices are MIT or GPL licenses.
4. **Create the Repository**
   - Click on "Create repository". GitHub will create your new repository and take you to its main page.

By following these steps, you’ll have set up a GitHub repository for your snake game project and can start developing and sharing your game with others. Remember, GitHub is not just a place to store your code; it's also a platform for collaboration and showcasing your work.

**Note** We'll be using the repo you 'forked' from the point forward, so that you have the guidance and guardrails that have been set in that project and codespace.

## Clone repository

Cloning a repository is an essential step for working on a project locally on your computer. Here are the steps to clone a GitHub repository, using the example of a snake game repository:

1. **Open the Repository on GitHub**
   - Go to the GitHub page of the snake game repository you want to clone, in this case it's the 'wordsearchgame' repository that you previously forked. 
   - Ensure you are logged in to your GitHub account, or else you will receive a 404 error

2. **Copy the Repository URL**
   - On the repository page, locate the "Code" button. This is typically found near the top of the page, just above the list of files.
   - Click on the "Code" button. A dropdown menu will appear.
   - In this dropdown, you will see a URL under the "HTTPS" tab. This is the URL of the repository.
   - Click on the clipboard icon next to the URL to copy it to your clipboard.

3. **Launch your codespace (optional)**

   You can run the IDE for this workshop via a codespace. A GitHub codespace is a cloud-based development environment that allows you to write, build, and debug your code directly in your browser or in your favorite IDE. It provides a consistent and reproducible development environment, making it easier to collaborate with others and work on projects from anywhere.

   - To Launch your codespace, click on the 'code' button in your repo, then select 'codespaces', 'create codespace on main' (Code > Codespaces > Create codespace on main)
   - Once the Codespace is ready, you can operate it from the browser or [open it from Visual Studio Code](https://docs.github.com/en/codespaces/developing-in-a-codespace/using-github-codespaces-in-visual-studio-code) (VSCode) locally if you have the codespaces extension installed.
   
   When you work with a codespace from your local VSCode the heavy lifting is done in the codespace and streamed to your local VSCode window. The default extensions and settings are all based on the .devcontainer definition of the codespace. Which means you can use codespaces to get new members of the team up and running with a preconfigured codespace in minutes.

   - **Setting Up Visual Studio Code:**
      - Familiarize yourself with the Visual Studio Code interface within the GitHub Codespace. In particular we'll be using the terminal in VSCode for the next few steps
   
3. **Clone the Repository Using Git** 
   - One of the benefits of using a codespace is it can have an already cloned a copy of the repository for you, but these are fundamentals that are good to know.
   - Open your command line interface (CLI), in this case a terminal within your codespace / VSCode. 
      - If we were developing on your local machine, this could also be Command Prompt on Windows, Terminal on macOS, or another terminal application if you're using a different operating system. It also relies on having the git command line tools installed.
   - Navigate to the directory where you want to clone the repository. You can use the `cd` command (which stands for "change directory") to navigate to a specific folder.
   - Once you are in the desired directory, type the clone command followed by the URL you copied from GitHub:
     ```
     git clone [repository URL]
     ```
   - For example:
     ```
     git clone https://github.com/username/WordSearchGame.git
     ```
   - Press Enter. Git will start cloning the repository to your local machine (or in the case of the codespace you are using, clone it again).
   - Once the cloning process is complete, you will have a local copy of the snake game repository.

4. **Verify the Cloning Process**
   - To ensure everything was cloned correctly, you can list the files in the directory by typing:
     ```
     ls
     ```
   - This command will display all the files and folders in the current directory, allowing you to see the contents of the cloned repository.

5. **Create a sub-folder for your snake Game**
   - After cloning, you'll want a new folder to organise your game project files. 
     ```
     mkdir WordSearchGame
     ```

Now you are ready to work on the snake game project within your codespace.

## Commit and push

Committing and pushing changes are fundamental Git operations that allow you to save your changes locally and then update the remote repository on GitHub. Here are the steps to commit and push changes:

### Committing Changes:

1. **Check the Status:**
   - Before committing changes, check the status of your repository to see which files have been modified. Type:
     ```bash
     git status
     ```
   - This will show you the files that have been modified and need to be committed.

2. **Stage Changes:**
   - Use the `git add` command to stage the changes. Replace `filename` with the actual name of the file you want to stage, or use `.` to stage all changes:
     ```bash
     git add filename
     ```
     or
     ```bash
     git add .
     ```

3. **Commit Changes:**
   - Once the changes are staged, commit them with a meaningful commit message using the `git commit` command:
     ```bash
     git commit -m "Your meaningful commit message here"
     ```

### Pushing Changes:

4. **Push to the Remote Repository:**
   - After committing changes locally, you need to push them to the remote repository on GitHub. Use the `git push` command:
     ```bash
     git push origin master
     ```
   - Replace `master` with the name of the branch you are working on if it's different.

   - If you are pushing to a branch other than the master, you might need to set the upstream branch:
     ```bash
     git push -u origin your-branch-name
     ```
     This sets up tracking, allowing you to use `git push` without specifying the branch in the future.

5. **Enter GitHub Credentials:**
   - You may be prompted to enter your GitHub username and password, or a personal access token if you have enabled two-factor authentication.
   - With codespaces, the codespace itself is set up to be able to read/write to the repo it was launched from, but you can modify the codespace .devcontainer configuration file if you ever need a codespace to be able to operate across multiple repos in an organisation.

7. **Verify Changes on GitHub:**
   - Visit the GitHub repository page in your web browser and refresh the page to see the changes you've pushed.

Now, your changes are both committed locally and pushed to the remote repository on GitHub. This workflow allows you to keep your local and remote repositories in sync as you develop your snake game.

## Create a branch and merge

Creating a branch and merging changes is a common workflow in Git when working on features or fixes without affecting the main codebase directly. Branching in Git allows developers to create isolated environments within a repository, enabling them to work on new features or fixes without affecting the main codebase. Each branch represents a distinct line of development, and changes made in a branch can be tested independently before being merged back into the main branch, ensuring a controlled and organized development process.

Here are the steps to create a branch, make changes, and then merge them back into the main branch:

### Create a Branch:

1. **Create a New Branch:**
   - Use the `git branch` command to create a new branch. Replace `branch-name` with a descriptive name for your branch:
     ```bash
     git branch branch-name
     ```

2. **Switch to the New Branch:**
   - Switch to the newly created branch using the `git checkout` command:
     ```bash
     git checkout branch-name
     ```
     or use the combined command:
     ```bash
     git checkout -b branch-name
     ```

### Make Changes in the Branch:

3. **Make Changes:**
   - Open your project files in your preferred code editor.
   - Make the necessary changes to implement a new feature or fix a bug.

4. **Commit Changes in the Branch:**
   - Stage and commit the changes in the branch, similar to the steps mentioned earlier:
     ```bash
     git add .
     git commit -m "Your meaningful commit message here"
     ```

### Merge Changes into the Main Branch:

5. **Switch to the Main Branch:**
   - Switch back to the main branch using the `git checkout` command:
     ```bash
     git checkout main
     ```
   - **Note** Prior to Oct 2020 'master' was the default branch name for github repo's, so you will find master as the default branch on older repositories, or may be part of organisational preferences.

6. **Merge Changes:**
   - Use the `git merge` command to merge the changes from your branch into the main branch:
     ```bash
     git merge branch-name
     ```
     If there are no conflicts, this will automatically merge the changes.

7. **Resolve Conflicts (If Any):**
   - If there are conflicts, Git will notify you. Open the conflicting files in your code editor, resolve the conflicts, and then commit the changes.
     ```bash
     git commit -m "Merge branch-name into main"
     ```

8. **Push Changes to GitHub:**
   - Finally, push the changes to GitHub to update the remote repository:
     ```bash
     git push origin main
     ```

9. **Delete the Branch (Optional):**
    - Once the changes are merged, you can optionally delete the branch:
      ```bash
      git branch -d branch-name
      ```

### Verify Changes on GitHub:

10. **Visit the GitHub Repository:**
    - Open your GitHub repository in a web browser and verify that the changes from your branch are now reflected in the main branch.

This workflow ensures that you can work on features or fixes in isolation, test them, and then merge them back into the main branch without affecting the stability of the main codebase.

## Issue tracking

Issue tracking is a vital aspect of project management on GitHub. It allows you to keep track of tasks, enhancements, bugs, and other issues related to your project. Here's a guide on how to use issue tracking on GitHub:

### Creating an Issue:

1. **Navigate to Your Repository:**
   - Open your web browser and go to the GitHub repository where you want to create an issue.
   - Ensure you are logged in to your GitHub account.

2. **Go to the "Issues" Tab:**
   - In the repository, click on the "Issues" tab near the top of the page.

3. **Create a New Issue:**
   - Click the green "New issue" button.
   - Provide a descriptive title for the issue that summarizes the task or problem.

4. **Write a Detailed Description:**
   - In the comment box, write a detailed description of the issue.
   - Include relevant information such as steps to reproduce, expected behavior, and actual behavior for bug reports.
   - For feature requests, describe the desired functionality.

5. **Assign Labels and Milestones (Optional):**
   - Use labels to categorize the issue (e.g., bug, enhancement, documentation).
   - Assign milestones to group related issues together (e.g., for a specific release).

6. **Assignees (Optional):**
   - Assign the issue to one or more contributors who will be responsible for addressing it.

7. **Submit the Issue:**
   - Click the green "Submit new issue" button.

### Managing and Updating Issues:

8. **Commenting on Issues:**
   - Use the comment section to discuss and provide additional information on the issue.
   - Mention other contributors using `@username` to notify them.

9. **Closing an Issue:**
   - Once an issue is resolved, click the "Close issue" button.
   - Optionally, you can add a comment explaining the resolution.

10. **Referencing Issues in Commits:**
    - When making commits related to an issue, reference the issue number in your commit message (e.g., "Fixes #1").
    - This automatically links the commit to the issue.

11. **Filtering and Searching Issues:**
    - Utilize filters and the search bar in the "Issues" tab to find specific issues.
    - Filters include open/closed issues, assigned issues, and issues with specific labels.

### Notifications:

12. **Subscribe to Notifications:**
    - Click the "Subscribe" button to receive notifications for updates on the issue.
    - Contributors can stay informed about discussions and changes.

Issue tracking on GitHub provides transparency, collaboration, and organization for project development. It serves as a centralized hub for communication and progress monitoring.

## GitHub actions

[GitHub Actions](https://docs.github.com/en/actions) automate workflows for your GitHub projects. Here's a brief guide on how to explain and set up a new GitHub Action:

### Understanding GitHub Actions:

1. **What are GitHub Actions?**
   - [GitHub Actions](https://docs.github.com/en/actions) are workflows that automate processes in your GitHub repository.
   - Workflows are defined in YAML files and can be triggered by events like pushes, pull requests, or scheduled intervals.

2. **Components of GitHub Actions:**
   - **Workflow:** A series of jobs that run in a specific order.
   - **Job:** A set of steps that execute on the same runner, a machine (virtual or physical) with the GitHub Actions runner application installed, responsible for executing the steps of a workflow in response to events on a GitHub repository.
   - **Step:** A single task that can run commands or actions.
   - **Action:** Reusable, shareable units of code that perform a specific task. This could be deploying to Azure, generating docs, running tests, or building a Docker container.

### Setting Up a New GitHub Action:

3. **Create a `.github/workflows` Directory:**
   
   - In your GitHub repository, create a directory named `.github/workflows`.
   - This is where you'll store your workflow YAML files.
   
4. **Write a Workflow YAML File:**
   - Create a new YAML file in `.github/workflows` (e.g., `my_workflow.yml`).
   - Define your workflow, specifying triggers, jobs, and steps.
   - Here's a simple example that runs on each push:

     ```yaml
     name: My Workflow
     
     on:
       push:
         branches:
           - main
     
     jobs:
       build:
         runs-on: ubuntu-latest
     
         steps:
           - name: Checkout Repository
             uses: actions/checkout@v2
     
           - name: Run a Command
             run: echo "Hello, GitHub Actions!"
     ```

5. **Understanding the Workflow:**
   - This example workflow triggers on pushes to the main branch.
   - It has one job (`build`) that runs on the latest version of Ubuntu.
   - The steps include checking out the repository and running a simple command.

6. **Commit and Push:**
   - Commit your new workflow file and push it to your repository.
   - GitHub will automatically detect and run the workflow based on the specified triggers.

7. **Check Workflow Status:**
   - Go to the "Actions" tab in your GitHub repository.
   - You'll see your workflow running or completed, with details on each step.

8. **Explore GitHub Action Marketplace (Optional):**
   - GitHub has a marketplace with pre-built actions.
   - You can include actions in your workflow YAML file using the `uses` key.

     ```yaml
     steps:
       - name: Use a Marketplace Action
         uses: actions/setup-node@v2
         with:
           node-version: '14'
     ```

   - This example uses the `setup-node` action to set up a Node.js environment.

### Leveraging GitHub Actions:

9. **Extend Workflows for Your Use Case:**
   - Customize your workflows for specific use cases, such as testing, building, deploying, or any automation task.

10. **Leverage GitHub Secrets (Optional):**
    - Store sensitive information securely using GitHub Secrets.
    - Access secrets in your workflow by referencing them as `${{ secrets.MY_SECRET }}`.

GitHub Actions streamline your development process, enabling you to automate tasks and workflows with ease. Explore the documentation and marketplace for additional actions and advanced configurations.