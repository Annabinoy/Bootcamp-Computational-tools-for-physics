
### Prerequisites
1. Install Git:
	- Windows: Download and install from https://git-scm.com/download/win
	- macOS: Install using Homebrew: brew install git
	- Linux: Use your package manager, e.g., sudo apt-get install git	- 
2.  Install WSL:
	 - One can follow this [tutorial](https://www.howtogeek.com/744328/how-to-install-the-windows-subsystem-for-linux-on-windows-11/).
3.  Install Visual Studio Code:
	 - Download and install from https://code.visualstudio.com/
	 - One can also follow this [tutorial](https://microsoft.github.io/vscode-essentials/en/01-getting-started.html).
### Hands-on Practice Session
#### 1. Basic Shell Commands  
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

#### 2. Creating a Bash Script
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

4. Create a new directory for your project:
```bash
mkdir my-bash-project
cd my-bash-project
```

#### 3. Creating and Editing Files
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
 5. Run the script::
```bash
./file_info.sh ../greet.sh
```

6. Create another file named `main.py` with the following content:
```python
def greet(name):
    return f"Hello, {name}!"

print(greet("World"))

```

##### References:
1. [`A beginner's guide to Git version control`](https://developers.redhat.com/articles/2023/08/02/beginners-guide-git-version-control#)
2. [`The Shell Scripting Tutorial`](https://www.shellscript.sh/)
3. [`Remote Linux Tutorial`](https://www.classes.cs.uchicago.edu/archive/2021/spring/15200-1/resources/linux.html)
4. [`Git Cheat Sheet`](https://developers.redhat.com/cheat-sheets/git-cheat-sheet)
5. [`Linux Commands Cheat Sheet`](https://developers.redhat.com/cheat-sheets/linux-commands-cheat-sheet)
6. [`Bash Commands Cheat Sheet`](https://developers.redhat.com/cheat-sheets/bash-shell-cheat-sheet)
