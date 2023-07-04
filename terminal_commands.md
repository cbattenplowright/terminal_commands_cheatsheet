# Terminal Commands cheatsheet

This markdown file is a document of relevant commands required to navigate the terminal and use git on MacOS. These commands should also run on a terminal of any UNIX operating system as MacOS is built upon the UNIX operating system. <br><br>

## Terminal Commands

Below are some core commands you should know for navigating around the termianl proficiently <br><br>

## Navigating the File System

| **Command** | Description |
| --- | --- |
| `pwd` | print working directory |
| `ls` | lists files in the current directory |
| `ls -l`| detailed list of files in current directory |
| `ls -a` | lists **all** files including hidden files in the current directory |
| `ls -al`| prints a detailed list of **all** files including hidden files in the current directory |
| `cd <directory_path>`| change directory |
| `cd` | returns to the root directory |
| `.`| signifies this directory |
| `..`| represents the parent directory |
| `history`| outputs the entire command history inputted into the terminal |
| ctrl + k | clears the terminal
| ctrl + l | moves the current line to the top of the screen |

> ### *You can combine flags which are denoted by a space and the dash symbol eg.* `ls -al`

<br>

## Creating Files and Directories

| **Command** | Description |
| --- | --- |
| `mkdir <name_of_directory>` | makes directory in the parent directory |
| `touch <filename.file_extension>`| creates file of the given file extension |
| `open <filename.file_extension>`| opens file in default application |
| `mv <filename/directory> <filename/directory>`| moves the file/directory to the specified directory, specifying a different filename renames the file too
| `cp <filename/directory> <directory>`| copies the file/directory to the specified directory. Providing a filename in the second path renames the file as it is moved.
| `rm <filename.file_extension>` | removes file of given name |
| `rm -r <name_of_directory>`| removes the directory and all that is in it |
| `rm -rf <name_of_directory>`| ***CAUTION!*** removes recursively and forecfully the specified file |

> ### ***DO NOT USE `rm -rf ~/` unless you wish to ***NUKE*** your computer  ***

<br><br>

## Git terminal commands

### Below are some useful commands when interacting with the git version control system in the terminal

<br> 

```
git init 
```
Initialises a git repository in the current directory <br><br>

```
git status
```
Gives the status of the current working tree <br><br>

```
git add <filename>
```
Used before committing after making changes to the working tree. Stages the content by updating the index in the working tree. <br><br>

```
git commit -m "file commit message here"
```
Commits the change to the repository with a message <br><br>

```
git log
```
Displays the git commit history <br><br>

## Linking a repository to Github using terminal

```
git remote add <name> <https/ssh link>
```
Adds a remote repository named \<name> by convention we tend to use ***origin*** at the URL provided <br><br>

```
git push origin main
```
Pushes the contents of the main branch to the remote repository, in this case origin. <br><br>

```
git clone <https/ssh link>
```
Creates a clone of a repository or branch into a newly created directory on the local machine <br><br>

```
git pull origin main
```
Brings changes of the remote repository into the clone repository

<br>

## Ignoring files and directories

Sometimes you do not want Git to commit certain file classes. Generally these are generated files such as log files or system generated files. You can create a `.gitignore`file listing patterns matching the file patterns. Setting a `.gitignore` file before starting a project is normally a good idea to save a file being created and then being accidentally committed.

There are multiple locations to have Git ignore certain files see: http://vinyll.scopyleft.fr/using-gitignore-the-right-way/ for more information regarding .gitignore files in project directories and a the root directory.

There are various rules for patterns as follows:

- Blank lines or lines starting with `#` are ignored
- Standard glob patterns work, and are applied recursively
- You can start patterns with a `/`to avoid recursively
- You can end patterns with a `/`to specify a directory
- You can negate a pattern with a `!`

```
touch .gitignore
```
Creates the .gitignore file to load and input the file patterns

Example of a .gitignore file:
````
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in any directory named build
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf

#credit git-scm.com
```