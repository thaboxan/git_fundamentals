# git_fundamentals
learn git 

# GITHUB

### **Configuring Git**

If you haven't configured Git on your system, you need to set up your username and email. This information will be used to identify your commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"

```

### Clone Repository

1. **Open Terminal**:
    - Open the Terminal application on your computer. You can usually find it in the "Utilities" folder within the "Applications" folder on macOS or by searching for "Command Prompt" or "PowerShell" on Windows.
2. **Navigate to Desired Directory**:
    - Use the `cd` command to navigate to the directory where you want to clone the repository. For example:
        
        ```
        cd ~/Documents
        
        ```
        
3. **Clone the Repository**:
    - Use the `git clone` command followed by the URL of the GitHub repository you want to clone. For example:
        
        ```
        git clone <https://github.com/username/repository.git>
        
        ```
        
    
    Replace `https://github.com/username/repository.git` with the actual URL of the repository you want to clone.
    
4. **Enter Credentials (if required)**:
    - If the repository is private and requires authentication, you will be prompted to enter your GitHub username and password or a personal access token. After entering your credentials, press Enter.
5. **Verification**:
    - Once the cloning process is complete, you should see a message indicating that the repository has been cloned successfully.
6. **Navigate into the Cloned Repository**:
    - After cloning, you can navigate into the cloned repository using the `cd` command followed by the repository's name. For example:
        
        ```
        cd repository
        
        ```
        

### **Creating a New Repository**

To create a new repository on GitHub, you can use the GitHub web interface. However, you can also create one using the terminal:

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <https://github.com/username/new_repository.git>
git push -u origin master

```

### **Adding Changes**

After making changes to files in your local repository, you need to stage and commit those changes.

```bash
git add <file1> <file2> ... <fileN>    # Stage specific files
git add .                               # Stage all changed files
git commit -m "Commit message here"     # Commit staged changes

```

### **Pushing Changes to GitHub**

To push your committed changes to GitHub, use the `git push` command.

```bash
git push origin master    # Push changes to the 'master' branch

```

### **Pulling Changes from GitHub**

To fetch changes from a GitHub repository and merge them into your local repository, use the `git pull` command.

```bash
git pull origin master    # Pull changes from the 'master' branch

```

### **Checking Status**

To check the status of your local repository, including staged changes and untracked files, use the `git status` command.

```bash
git status

```

### **Viewing Commit History**

To view the commit history of your repository, use the `git log` command.

```bash
git log

```

### **Branching**

To create, switch, and delete branches in your repository, you can use the following commands:

```bash
git branch                       # List all branches
git branch <branch_name>         # Create a new branch
git checkout <branch_name>       # Switch to a branch
git branch -d <branch_name>      # Delete a branch

```

### **Merging Branches**

To merge changes from one branch into another, you can use the `git merge` command.

```bash
git checkout master       # Switch to the branch you want to merge changes into
git merge <branch_name>  # Merge changes from <branch_name> into the current branch

```

### Renaming Repository

To rename a cloned repository on your local machine, you need to rename the directory containing the repository files. Here's how you can do it:

1. **Navigate to the Directory:**
Open your terminal and navigate to the directory where the cloned repository is located using the `cd` command. For example:
    
    ```bash
    cd /path/to/cloned/repository
    
    ```
    
2. **Rename the Directory:**
Use the `mv` command to rename the directory containing the cloned repository. For example, if you want to rename the repository directory from `old_repo_name` to `new_repo_name`, you would use:
    
    ```bash
    mv old_repo_name new_repo_name
    
    ```
    
3. **Update Remote URL (Optional):**
If you want to update the remote URL to reflect the new repository name on GitHub, you can use the following command:
    
    ```bash
    git remote set-url origin <https://github.com/username/new_repo_name.git>
    
    ```
    
    Replace `https://github.com/username/new_repo_name.git` with the actual URL of the renamed repository on GitHub.
    

That's it! You have successfully renamed the cloned repository on your local machine. If you updated the remote URL, it will reflect the new name on GitHub as well.
