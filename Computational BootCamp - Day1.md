
#### Prerequisites
1. Install Git:
	- Windows: Download and install from https://git-scm.com/download/win
	- macOS: Install using Homebrew: brew install git
	- Linux: Use your package manager, e.g., sudo apt-get install git	- 
2.  Install WSL:
	 - Download and install from https://code.visualstudio.com/
3.  Install Visual Studio Code:
	 - Download and install from https://code.visualstudio.com/
#### Hands-on Practice Session
###### 1. Basic Shell Commands  
Open a terminal and practice these essential commands:
```bash
pwd                 # Print working directory
ls                  # List files and directories
cd <directory>      # Change directory
mkdir <directory>   # Create a new directory
touch <filename>    # Create an empty file
cat <filename>      # Display file contents
cp <source> <destin>  # Copy files or directories
mv <source> <destin>  # Move or rename files/directories
rm <filename>       # Remove a file
rm -r <directory>   # Remove a directory and its contents

```

###### 2. Creating a Bash Script
1. Create a new file named `greet.sh`:
```bash
touch greet.sh

```
2. Open the file in VS Code:
```bash
code greet.sh

```
3. Add the following content to greet.sh:
```bash
#!/bin/bash

echo "What's your name?"
read name
echo "Hello, $name! Welcome to bash scripting."

current_date=$(date +"%Y-%m-%d")
echo "Today's date is: $current_date"

echo "Your current working directory is:"
pwd

echo "Files in this directory:"
ls -l

```
3. Make the script executable:
```bash
chmod +x greet.sh

```
3. Run the script:
```bash
./greet.sh

```
###### 3. Setting up Git
Open a terminal or command prompt and configure Git:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

###### 4. Creating a Local Repository
1. Create a new directory for your project:
```bash
mkdir my-bash-project
cd my-bash-project
```
2. Initialize the Git repository:
```bash
git init
```
###### 5. Creating and Editing Files from the terminal
1. Create a README file:
```bash
echo "# My Bash Project" > README.md
```
2. Create a new bash script named `file_info.sh`:
```bash
touch file_info.sh
code file_info.sh
```
3. Add the following content to `file_info.sh`:
```bash
#!/bin/bash

if [ $# -eq 0 ]; then
    echo "Usage: $0 <filename>"
    exit 1
fi

filename=$1

if [ ! -f "$filename" ]; then
    echo "File not found: $filename"
    exit 1
fi

echo "File information for: $filename"
echo "------------------------"
echo "Size: $(du -h "$filename" | cut -f1)"
echo "Permissions: $(ls -l "$filename" | cut -d ' ' -f1)"
echo "Last modified: $(stat -c %y "$filename")"
echo "File type: $(file -b "$filename")"
```
 4. Make the script executable:
```bash
chmod +x file_info.sh
```

###### 6. Creating and Editing Files in VS Code
1. Open Visual Studio Code:
```bash
code .

```
2. Open the file named `README.md` and can edit the following content(optional):
```text
# My First Repository

This is a practice repository for learning Git and GitHub.
```
3. Create another file named `main.py` with the following content:
```python
def greet(name):
    return f"Hello, {name}!"

print(greet("World"))

```
###### 7. Staging and Committing Changes
1. Check the status of your repository:
```bash
git status
```
2. Stage the files:
```bash
git add README.md main.py file_info.sh greet.sh
```
3. Commit the changes:
```bash
git commit -m "Initial commit: Add README, bash scripts and main.py"
```
###### 8. Creating Branches
1. Create a new branch:
```bash
git branch feature-greeting
```
2. Switch to the new branch:
```bash
git checkout feature-greeting
```
3. Modify `main.py`:
```python
def greet(name):
    return f"Hello, {name}! Welcome to Git practice."

print(greet("World"))
```
4. Stage and commit the changes:
```bash
git add main.py
git commit -m "Update greeting message"
```
###### 9. Merging Branches
1. Switch back to the main branch:
```bash
git checkout main
```
2. Merge the feature branch:
```bash
git merge feature-greeting
```
###### 10. Creating a Remote Repository (GitHub)
1. Go to GitHub and create a new repository named "my-first-repo":
2. Link your local repository to the remote:
```bash
git remote add origin https://github.com/your-username/my-first-repo.git
```
3. Push your local repository to GitHub:
```bash
git push -u origin main
```
###### 11. Collaborative Work
1. Create a new directory for your project:
2. Initialize the Git repository:

###### References:
1. [`A beginner's guide to Git version control`](https://developers.redhat.com/articles/2023/08/02/beginners-guide-git-version-control#)
2. [`The Shell Scripting Tutorial`](https://www.shellscript.sh/)
3. [`Remote Linux Tutorial`](https://www.classes.cs.uchicago.edu/archive/2021/spring/15200-1/resources/linux.html)
4. [`Git Cheat Sheet`](https://developers.redhat.com/cheat-sheets/git-cheat-sheet)
5. [`Linux Commands Cheat Sheet`](https://developers.redhat.com/cheat-sheets/linux-commands-cheat-sheet)
6. [`Bash Commands Cheat Sheet`](https://developers.redhat.com/cheat-sheets/bash-shell-cheat-sheet)
