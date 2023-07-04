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

<br>



