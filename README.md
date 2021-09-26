# important-linux-cli-commands
## 1. ls

    ls
It lists the files and folders in the directory you specify. By default, `ls` looks in the current directory. There are a great many options you can use with `ls`
To list the files and folders in the current directory:

    ls

To list the files and folders in the current directory with a detailed listing use the  `-l`  (long) option:

    ls -l

To use human-friendly file sizes include the  `-h`  (human) option:

    ls -lh

To include hidden files use the  `-a`  (all files) option:

    ls -lha

## 2 . cd

The `cd` command changes your current directory. In other words, it moves you to a new place in the filesystem.

If you are changing to a directory that is within your current directory, you can simply type  `cd`and the name of the other directory.

    cd work

If you are changing to a directory elsewhere within the filesystem directory tree, provide the path to the directory with a leading /.

    cd /var/log

To quickly return to your home directory, use the  `~`  (tilde) character as the directory name.

    cd ~


Here’s another trick: You can use the double dot symbol  `..`  to represent the parent of the current directory. You can type the following command to go up a directory:

    cd ..

## 3 . touch
the  `touch`  command is used to create ( or touch ) new or existing files.
for example to create new file.txt type the following command:

    touch file.txt
    
## 4 . nano
the  `nano`  command is used edit files, for example to edit file.txt type the following command:

    nano file.txt
to exit from nano click on CRTL/COMMAND+X then Y if you want to save or N if not then Enter

## 5. cat
The `cat` command (short for “concatenate”) lists the contents of files to the terminal window, for example if we want to see what's the content of file.txt type the following command:

    cat file.txt
## 6. chmod
The `chmod` command sets the file permissions flags on a file or folder. 
When you list files with the  `-l` (long format) option you’ll see a string of characters that look like

    -rwxrwxrwx
One way to use  `chmod`  is to provide the permissions you wish to give to the owner, group, and others as a 3 digit number. The leftmost digit represents the owner. The middle digit represents the group. The rightmost digit represents the others. The digits you can use and what they represent are listed here:

-   **0:**  No permission
-   **1:**  Execute permission
-   **2:**  Write permission
-   **3:**  Write and execute permissions
-   **4:**  Read permission
-   **5:**  Read and execute permissions
-   **6:**  Read and write permissions
-   **7:**  Read, write and execute permissions

To set the permission to be read, write, and execute (7 from our list) for the  _owner;_ read and write (6 from our list) for the  _group;_  and read and execute (5 from our list) for the  _others_  we’d need to use the digits 765 with the  `chmod`  command:

    chmod  765 file
To set the permission to be read, write and execute (7 from our list) for the  _owner_, and read and write (6 from our list) for the  _group_  and for the  _others_  we’d need to use the digits 766 with the  `chmod`  command:

    chmod 766 file

## 7. chown

The  `chown`  command allows you to change the owner and group owner of a file.

You can use  `chown`  to change the owner or group, or both of a file. You must provide the name of the owner and the group, separated by a  `:`  character. You will need to use  `sudo`. To retain dave as the owner of the file but to set mary as the group owner, use this command:

    chown ubuntu:ubuntu file.txt
## 8. curl

The  `curl`  command is a tool to retrieve information and files from Uniform Resource Locators (URLs) or internet addresses.

The  `curl`  command may not be provided as a standard part of your Linux distribution. Use `apt-get` to install this package onto your system if you’re using Ubuntu or another Debian-based distribution. On other Linux distributions, use your Linux distribution’s package management tool instead.

    apt-get install curl
## 9. df
The `df` command shows the size, used space, and available space on the mounted filesystems of your computer.

    df -h
