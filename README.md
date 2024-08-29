# **📚 Comprehensive Git and Development Environment Syllabus**

---

## **Technologies Used 🔧**

<div>
    <h1 style="text-align: center;">Version Control, Development Environment, and Python Project Management</h1>
    <img style="text-align: left" src="https://img.icons8.com/color/48/000000/git.png" width="10%" alt="Git Logo" />
    <img style="text-align: left" src="https://img.icons8.com/color/48/000000/github--v1.png" width="10%" alt="GitHub Logo" />
    <img style="text-align: left" src="https://img.icons8.com/color/48/000000/visual-studio-code-2019.png" width="10%" alt="VS Code Logo" />
    <img style="text-align: left" src="https://img.icons8.com/color/48/000000/python.png" width="10%" alt="Python Logo" />
</div>
<br>

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

---

## **📋 Table of Contents**

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

## **1. Git Basics 🚀**

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
- After making changes, add them to the staging area and commit. Use clear, descriptive commit messages:
```bash
git add .
git commit -m "feat: add new feature for data processing"
```
- **Best Practice for Commit Messages:**
  - Use prefixes like `feat:` for features, `fix:` for bug fixes, `refactor:` for code restructuring, `docs:` for documentation updates, etc.
  - Example: `git commit -m "fix: resolve edge case issue in metric calculation"`

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
git commit -m "chore: add .gitignore file"
```

### **Push Changes to the Remote Repository**
- Push your committed changes to the remote repository. Specify the branch name:
```bash
git push origin feature-branch
```

### **Open a Pull Request**
- Open a pull request from your feature branch to the main branch for code review and merging.

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

## **2. Additional Git Commands and Concepts 💡**

- **Checking Status:** Use `git status` to see the status of your changes and ensure everything is tracked correctly.
- **Staging Area:** Understand the importance of the staging area (`git add`) as an intermediate step before committing changes (`git commit`).
- **Commit Message Standards:** Maintain a consistent format for commit messages, using imperative mood and concise descriptions.
- **Branch Management:** Use `git branch` to list branches, `git branch -d branch_name` to delete branches, and `git branch -r` to list remote branches.
- **Undoing Changes:** Use `git revert <commit-hash>` to undo specific changes without rewriting commit history, or `git reset` for more drastic changes.
- **Tagging Releases:** Use `git tag -a v1.0 -m "Initial release"` to create annotated tags for releases.
- **Rebasing and Merging:** Use `git pull --rebase` to integrate changes without creating merge commits or `git merge` to combine branches.

---

## **3. Development Environment Setup 🛠️**

### **Preparation & Expectation**

- **Download VS Code:** Download Visual Studio Code from the [official site](https://code.visualstudio.com/).
- **GitHub Account:** Ensure you have a GitHub account for version control and collaboration.

### **Explore Common Development Operations**

#### **Environment Creation and Activation**
- Create and activate a Python virtual environment:
```bash
python -m venv venv_name
source venv_name/bin/activate  # On Windows use `venv_name\Scripts\activate`
```
- This keeps dependencies isolated and your project environment clean.

#### **Common Command Line Commands**
- **Navigation:**
  - Change directory: `cd <directory>`
  - Move up one directory: `cd ..`
- **Git Operations:**
  - Check status: `git status`
  - Add changes to staging: `git add .` or specify a path: `git add <path>`
  - Commit changes: `git commit -m "feat: add new API endpoint"`
  - Push changes: `git push origin branch_name`
  - Pull changes: `git pull origin branch_name`
  - Rebase to update: `git pull --rebase`
  - Create a branch: `git branch branch_name`
  - Switch to a branch: `git checkout branch_name`
  - Fetch all branches: `git fetch --all`
  - Clone a repository: `git clone <repository-url>`
- **Tree View:**
  - On Windows, use `tree /F` to see a tree representation of directories and files.
- **Python Package Management:**
  - Install packages: `pip install -r requirements.txt`
  - Freeze dependencies: `pip freeze > requirements.txt`
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
  - Example structure:
    ```
    project/
    ├── main.py
    ├── app/
    │   ├── __init__.py
    │   └── backend.py
    ├── tests/
    │   ├── __init__.py
    │   └── test_backend.py
    ├── requirements.txt
    ├── .gitignore
    └── README.md
    ```

#### **Starting a Project in VS Code**
- **Project Setup:**
  - Open a folder and navigate to your project directory: `cd <project

-directory>`.
  - Clone the repository: `git clone <repository-url>`.
- **Environment and Git Operations:**
  - Create and activate the environment.
  - Check status: `git status`.
  - Make changes, save, and commit:
  ```bash
  git add .
  git commit -m "feat: add initial setup for Streamlit app"
  ```
  - Push changes: `git push origin branch_name`.
  - Verify changes on GitHub and ensure they align with the latest code base.

---

## **4. Extras 🛠️**

- **VS Code Extensions and GUI:** Leverage extensions for Python, GitLens, Docker, and Streamlit to enhance your coding experience.
- **Automate Requirements Management:** Use pipreqs or pip-tools for generating and managing `requirements.txt` files.
- **Working with Forks:** Understand forking on GitHub, managing upstream changes, and contributing back with pull requests.
- **Ubuntu and WSL:** Utilize Ubuntu or Windows Subsystem for Linux (WSL) for a Linux-like development environment on Windows, enhancing command-line operations and development workflows.

---

## **5. Additional Reference 📚**

- **Git Commands and Workflows:** Learn more about Git commands and workflows from the [official Git documentation](https://git-scm.com/doc).
- **VS Code Tips:** Explore VS Code tips and tricks to boost your productivity from the [VS Code documentation](https://code.visualstudio.com/docs).
- **Python Virtual Environments:** Understand virtual environments and package management from the [Python documentation](https://docs.python.org/3/tutorial/venv.html).

---
