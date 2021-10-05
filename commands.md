### tmux

---
### man

man page contains so much information about the commands that you want to look at sometimes it's almost too much.
Most of the time when I need to learn a command quickly I use the man <command>. It gives a very quick overview of command.
Another command which is tldr, this is not a substitute for man, but a handy tool to avoid using yourself in the huge amount of information
present in a man page.
``` linux
Ex: man ls
```
You can use the man page to explore all the different options and parameters you can see on a command.

---
### ls
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
