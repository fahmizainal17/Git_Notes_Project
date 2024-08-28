# **Comprehensive Git and Development Environment Syllabus**

## **Table of Contents**

1. [Git Basics](#git-basics)
   - [Clone a Repository](#clone-a-repository)
   - [Update the Local Repository](#update-the-local-repository)
   - [Create a New Branch](#create-a-new-branch)
   - [Switch to the New Branch](#switch-to-the-new-branch)
   - [Add and Commit Changes](#add-and-commit-changes)
   - [Create a `.gitignore` File](#create-a-gitignore-file)
   - [Save and Commit `.gitignore`](#save-and-commit-gitignore)
   - [Push Changes to the Remote Repository](#push-changes-to-the-remote-repository)
   - [Open a Pull Request](#open-a-pull-request)
   - [Switch Back to the Main Branch](#switch-back-to-the-main-branch)
   - [Update the Local Main Branch](#update-the-local-main-branch)

2. [Additional Git Commands and Concepts](#additional-git-commands-and-concepts)

3. [Development Environment Setup](#development-environment-setup)
   - [Preparation & Expectation](#preparation--expectation)
   - [Explore Common Development Operations](#explore-common-development-operations)
     - [Environment Creation and Activation](#environment-creation-and-activation)
     - [Common Command Line Commands](#common-command-line-commands)
     - [Common Python Project Structure](#common-python-project-structure)
     - [Starting a Project in VS Code](#starting-a-project-in-vs-code)

4. [Extras](#extras)

5. [Additional Reference](#additional-reference)

---

## **Git Basics**

### **Clone a Repository**
- Clone a repository to get a local copy of the code on your machine.
```bash
git clone <repository-url>
cd <repository-directory>
```
- Replace `<repository-url>` with the actual URL of the repository.

### **Update the Local Repository**
- Update your local copy to ensure it's synchronized with the main branch.
```bash
git pull origin main
```
- Replace `main` with the name of your primary branch if different.

### **Create a New Branch**
- Create a new branch for feature development or bug fixing.
```bash
git branch feature-branch
```

### **Switch to the New Branch**
- Switch your working directory to the new branch.
```bash
git checkout feature-branch
```
- Or create and switch in one step:
```bash
git checkout -b feature-branch
```

### **Add and Commit Changes**
- After making changes, add them to the staging area and commit.
```bash
git add .
git commit -m "Description of your changes"
```

### **Create a `.gitignore` File**
- Specify files and directories to be ignored by Git.
```plaintext
# Example .gitignore content
.idea/
*.pyc
```

### **Save and Commit `.gitignore`**
- Save and commit the `.gitignore` file.
```bash
git add .gitignore
git commit -m "Add .gitignore file"
```

### **Push Changes to the Remote Repository**
- Push your committed changes to the remote repository.
```bash
git push origin main
```

### **Open a Pull Request**
- Open a pull request for code review and merging your changes.

### **Switch Back to the Main Branch**
- Switch to the main branch.
```bash
git checkout main
```

### **Update the Local Main Branch**
- Pull the latest changes from the remote main branch.
```bash
git pull origin main
```

---

## **Additional Git Commands and Concepts**

- **Checking Status:** Use `git status` to see the status of your changes.
- **Staging Area:** Understand the importance of the staging area for preparing commits.
- **Commit Message Standards:** Adopt a consistent format for commit messages.
- **Pushing and Pull Requests:** Familiarize yourself with pushing branches and opening pull requests.
- **Switching Branches:** Use `git checkout` to switch between branches.
- **Remote Branches:** List remote branches with `git branch -r`.
- **Undoing Changes:** Use `git revert <commit-hash>` to undo specific changes.

---

## **Development Environment Setup**

### **Preparation & Expectation**

- **Download VS Code:** Get VS Code from the Microsoft Store.
- **GitHub Account:** Ensure you have a GitHub account.

### **Explore Common Development Operations**

#### **Environment Creation and Activation**
- Create and activate a Python virtual environment:
```bash
python -m venv venv_name
venv_name/Scripts/activate
```
- Understand where the `.git` directory and your virtual environment are located.

#### **Common Command Line Commands**
- **Navigation:**
  - Change directory: `cd <directory>`
  - Move up one directory: `cd ..`
- **Git Operations:**
  - Check status: `git status`
  - Add changes to staging: `git add .`
  - Commit changes: `git commit -m "feat: add feature"`
  - Push changes: `git push`
  - Pull changes: `git pull`
  - Rebase: `git pull --rebase`
  - Create a branch: `git branch branch_name`
  - Switch to a branch: `git checkout branch_name`
  - Fetch all branches: `git fetch --all`
  - Clone a repository: `git clone <repository-url>`
- **Tree View:**
  - On Windows, use `tree /F` to see a tree representation of directories and files.
- **Python Package Management:**
  - Install packages: `pip install -r requirements.txt`
  - Freeze packages: `pip freeze > requirements.txt`
  - Show installed packages: `pip show <package>`

#### **Common Python Project Structure**
- **Project Files:**
  - `main.py`
  - `README.md`
  - `.gitignore`
  - `LICENSE`
  - `requirements.txt`
- **Modules and Imports:**
  - Organize your code into modules and use `__init__.py` to make them importable.

#### **Starting a Project in VS Code**
- **Project Setup:**
  - Open a folder and navigate to your project directory: `cd <project-directory>`.
  - Clone the repository: `git clone <repository-url>`.
- **Environment and Git Operations:**
  - Create and activate the environment.
  - Check status: `git status`.
  - Make changes, save, and commit: 
  ```bash
  git add .
  git commit -m "feat: add features"
  ```
  - Push changes: `git push`.
  - Verify changes on GitHub and vice versa.

---

## **Extras**

- **VS Code Extensions and GUI:** Explore useful extensions and GUI features in VS Code.
- **Pipreqs Command Line:** Automate the creation of `requirements.txt` with pipreqs.
- **Forking GitHub Repositories:** Understand the difference between local and remote repositories, and the process of forking.
- **Ubuntu and WSL:** Explore Ubuntu and Windows Subsystem for Linux (WSL) for a Linux-like development environment.

---

## **Additional Reference**

- **Git Commands:** Master a variety of Git commands for effective version control.
- **Git Workflow:** Learn about different Git workflows to enhance collaboration and code management.

---
