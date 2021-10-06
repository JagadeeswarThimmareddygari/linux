## tmux

---
## man

man page contains so much information about the commands that you want to look at sometimes it's almost too much.
Most of the time when I need to learn a command quickly I use the man <command>. It gives a very quick overview of command.
Another command which is tldr, this is not a substitute for man, but a handy tool to avoid using yourself in the huge amount of information
present in a man page.
``` script
man ls
```
You can use the man page to explore all the different options and parameters you can see on a command.

---
## ls
You can list all the files that the folder contains using the ls command:
``` linux
ls
```
If you add a folder name or path it'll print the folder content
``` linux
ls \mnt\h\webdevelopment
```
ls accepts lot of options. Try for al

``` linux 
ls -al
```
a- will display all hidden files (start with dot)
l- will display from left to right below information
- a file permission
- The number of links to the file
- The owner of the file
- The group of the file
- The file size in bytes
- The files last modified datatime
- The file name

> Also one of my favorite command is tree command to display all files and directories in the current folder.

---

## cd command
Once you've a folder, you can move into it using the cd command. cd means change directory. You can invoke it by specifying a folder to move into. You can specify a folder name or entire path.
``` linux
mkdir devops
cd deveops
```
Now you're in devops folder
You can use .. special path to indicate the parent folder.
cd .. # moves to the previous directory
You can also use absolute path which starts from the root directory
```linux
cd /mnt
```
---

## pwd command
Whenever you feel lost in the filesystem,call the  pwd command to know where you are:
``` bash
pwd
```

---

## mkdir command
You create folders using mkdir command:
``` bash
mkdir fruits
```
You can create multiple folders using one command
``` bash
mkdir python javascript
```
You can also create multiple nested folders by adding the -p option:
``` bash
mkdir -p fruits/apples
```
If you want to find out all the options you can use command man mkdir for more examples.

---
## rmdir command
Just as you can creat a folder using mkdir, you can delete a folder using rmdir.

``` bash
rmdir fruits
```
You can delete multiple folders at once
```bash
rmdir python javascript
```
The folder that you delete must be empty
To delete the folder with files in them, we'll use the more generic rm command which deletes all files and folders using -rf option.
``` bash
rm -rf python javascript
```
Be careful as this command doesn't ask for confirmation. It'll immediately remove anything that you ask it to remove.
There is no bin when removing files from command line, and recovering lost files can be hard.

---
## mv command
Once you've a file you can move it around using mv command. You can specify the current file path and it's new path.

``` bash
mv lab4 lab5
```
lab4 file is now moved to lab5 file. This is how you rename files and folders.

``` bash
mv pear apple fruits
```

pear and apple moved to the fruits folder.

---
## cp command
You can copy file using the cp command:
``` bash
cp apple another_apple
```
To copy folders you need to add the -r option to recursively copy the whole folder contents:
``` bash
cp -r python javascript
```
---
## touch command
You can create an empty file using the touch command:
``` bash
touch apple
```
If the file already exists, it opens the file in write mode, and time stamp of the file is updated.

## find command
The find command is used to find files or folders matching a particular search pattern.It searches recursively
Example:
find all the files under the current tree that have the .py extension and print the relative path of each file that matches:
``` bash
find . -name '*.py'

>Have to update some more commands

