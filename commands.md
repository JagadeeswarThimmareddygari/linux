## tmux
tmux is one of my favorite command.

tmux is a open source terminal multiplexer. It allows multiple terminal sessions to be accessed simultaneously in a single window.

To install the package type the following command in your terminal
```script
sudo apt install tmux
```
Once the installation is done, first we need to get into the tmux. Type the command following command tmux and you'll get the highlighted green bar at the bottom.
```script
tmux
```
press the following command on your windows to split the screen vertical
```script
ctrl+b+%
```
Press the following command on your windows to split the screen horizontal
```script
ctrl+b+"
```
To navigate between terminals type the following command
```script
ctrl+b+(navigation symbol <- or ->)
```





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
```
>Have to update some more commands
---
## ln command
It's used to create links. What's is a link? It's like a pointer to another file, or a file that points to another file.
We've 2 types of links
- Hard links
- Soft links
#### Hard links
 Hard links are rarely used. They have a few limitations: you can't link to directories and you can't link to external file systems(disks).
 A hard link is created using the following the syntax:
 ``` bash
 ln <original> <link>
 ```
 For example you have a file called fruits.txt. You can create a hard link to it using:
 ``` bash
 ln fruits.txt new_fruits.txt
 ```
 The new hard link that you've created is indistinguishable from a regular file.
 Now you can edit any of those files, the content will be updated for both.
 If you delete the orginal file, the link will still contain the original file content, as that's not removed until  there is one hard
 link pointing to it.
#### Soft links
Soft links are different. They  are more powerful as you can link to other filesystems and to directories. But keep in mind that the original is removed, the link will be broken.
You can create soft links using the -s option of ln:
``` bash
ln -s <original> <link>
```
For example, you have created a file called fruits.txt. You can create soft link to it using:
``` bash
ln -s fruits.txt new_fruits.txt
```
In this case you can see there's a special flag when you list the file using ls -al. The file has a @ at the end or you see new_fruits -> fruits.
Now if you delete the original file, the link will be broken, and the shell will tell you "No such file or directory" if you try to access it.

---
