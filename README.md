
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
then we can use something like 

    curl https://www.google.com
to retrive all the data in that link ( in that case the source of the html of google.com )

## 9. df
The `df` command shows the size, used space, and available space on the mounted filesystems of your computer.

    df -h

## 10. clear
The `clear` command is used to clear and clean the screen from all previous commands and make it looks like new terminal window

    clear

## 11. clear
The `clear` command is used to clear and clean the screen from all previous commands and make it looks like new terminal window

    clear

## 12. vi
the  `vi`  command is used edit files, for example to edit file.txt type the following command:

    vi file.txt
to exit from nano click on ESC then write `:wq` if you want to save or `:q!` if not then Enter

## 13. grep

The `grep` utility searches for lines which contain a search pattern. The `grep` command can also search the contents of files. Here we’re searching for the word “hello” in all text files in the current directory.

    grep hello *.txt

## 14. finger
The `finger` command gives you a short dump of information about a user, including the time of the user’s last login, the user’s home directory, and the user account’s full name.

    finger root

## 15. top & htop
The `top` & `htop` command shows you a real-time display of the data relating to your Linux machine. The top of the screen is a status summary.
while htop is more detailed and human friendly 

## 16. free
The  `free`  command gives you a summary of the memory usage with your computer. It does this for both the main Random Access Memory (RAM) and swap memory. The  `-h`  (human) option is used to provide human-friendly numbers and units. Without this option, the figures are presented in bytes.

    free -h

## 17. alias
The alias command lets you give your own name to a command or sequence of commands. You can then type your short name, and the shell will execute the command or sequence of commands for you.

    alias cls=clear

## 18. diff
The  `diff`  command  compares two text files  and shows the differences between them. There are many options to tailor the display to your requirements.

The  `-y`  (side by side) option shows the line differences side by side. The  `-w`  (width) option lets you specify the maximum line width to use to avoid wraparound lines. The two files are called alpha1.txt and alpha2.txt in this example. The  `--suppress-common-lines`  prevents  `diff`  from listing the matching lines, letting you focus on the lines which have differences.

    diff -y -W 70 file.txt file2.txt --suppress-common-lines
    
## 19. echo

the  `echo`  command prints (echoes) a string of text to the terminal window.
The command below will print the words “A string of text” on the terminal window.

    echo A string of text

The  `echo`  command can show the value of environment variables, for example, the  `$USER`,  `$HOME`, and  `$PATH`  environment variables. These hold the values of the name of the user, the user’s home directory, and the path searched for matching commands when the user types something on the command line.

    echo $USER
    
    echo $HOME
    
    echo $PATH
## 20. exit
The exit command will close a terminal window, end the execution of a shell script, or log you out of an SSH remote access session.

    exit
## 21. find

Use the `find` command to track down files that you know exist if you can’t remember where you put them. You must tell `find` where to start searching from and what it is looking for. In this example, the `.` matches the current folder and the `-name` option tells `find` to look for files with a name that matches the search pattern.

    find . file.txt

## 22. groups

The  `groups`  command tells you which groups a user is a member of.

    groups root
    
    groups ubuntu

## 23. gzip

The  `gzip`  command compresses files. By default, it removes the original file and leaves you with the compressed version. To retain both the original and the compressed version, use the  `-k`  (keep) option.

    gzip -k file.txt

## 24. head

The  `head`  command gives you a listing of the first 10 lines of a file. If you want to see fewer or more lines, use the  `-n`  (number) option. In this example, we use  `head`  with its default of 10 lines. We then repeat the command asking for only five lines.
    
    head -n 5 /var/log/syslog

## 25. history

The history command lists the commands you have previously issued on the command line. You can repeat any of the commands from your history by typing an exclamation point  `!`and the number of the command from the history list.

    !188

Typing two exclamation points repeats your previous command.

    !!

## 26. kill

The  `kill`  command allows you to terminate a process from the command line. You do this by providing the process ID (PID) of the process to  `kill`. Don’t kill processes willy-nilly. You need to have a good reason to do so. In this example, we’ll pretend the  `top`  program has locked up.
we can use ps to find the process id of top

    ps -e | grep top
    kill 12345

## 28. man

The man command displays the “man pages” for a command in  `less`  . The man pages are the user manual for that command. Because  `man`  uses  `less` to display the man pages, you can use the search capabilities of  `less`.

For example, to see the man pages for  `chown`, use the following command:

man chown

Use the Up and Down arrow or PgUp and PgDn keys to scroll through the document. Press  `q`to quit the man page or press`h` for help.

## 29. mkdir

The  `mkdir`  command allows you to create new directories in the filesystem. You must provide the name of the new directory to  `mkdir`. If the new directory is not going to be within the current directory, you must provide the path to the new directory.

    mkdir test

## 30. tree
The  `tree`  command show you a tree for the folder or the path that you are in.

## 31. pwd
The  `pwd`  command show you the absolute path of your location now.

## 32. mv ( move )

The  `mv`  command allows you to move files and directories from directory to directory. It also allows you to rename files.

To move a file you must tell  `mv`  where the file is and where you want it to be moved to. In this example, we’re moving a file called  `file.txt`  from the “~” directory and placing it in the current directory, represented by the single  `.`  character.

    mv ~/file.txt .
    
## 33. cp ( copy )
The  `cp`  command allows you to copy files and directories from directory to directory. 

    cp file.txt test
    
## 33. rm ( remove )
The  `cp`  command allows you remove files and directories

    rm test/file.txt test
you can remove directory with all the content using

    rm -rf test
## 34. passwd

The  `passwd`  command lets you change the password for a user. Just type  `passwd`  to change your own password.

You can also change the password of another user account, but you must use  `sudo`. You will be asked to enter the new password twice.

    sudo passwd root

## 35. ping

The  `ping`  command lets you verify that you have network connectivity with another network device. It is commonly used to help troubleshoot networking issues. To use  `ping`, provide the IP address or machine name of the other device.

    ping google.com

The  `ping` command will run until you stop it with Ctrl+C.

## 36. ps

The  `ps`  command lists running processes. Using  `ps`  without any options causes it to list the processes running in the current shell.

    ps

To see every process that is running, use the  `-e`  (every process) option:

    ps -e

## 37. shutdown

The shutdown command lets you shut down your Linux system.

Using  `shutdown`  with no parameters will shut down your computer in one minute.

    shutdown
or if you want to shutdown now use

    shtdown now

## 38. reboot
The shutdown command lets you reboot your Linux system.

    reboot


## 39. sudo

The  `sudo`  command is required when performing actions that require root or superuser permissions, such as changing the password for another user.

    sudo passwd mary
    
## 40. tail

The  `tail` command gives you a listing of the last 10 lines of a file. If you want to see fewer or more lines, use the  `-n`  (number) option. In this example, we use  `tail` with its default of 10 lines. We then repeat the command asking for only five lines.

    tail /var/log/syslog

or you can use it to track the live changes using the option -f

    tail -f /var/log/syslog

## 41. uname

You can obtain some system information regarding the Linux computer you’re working on with the  `uname`  command.

-   Use the  `-a`  (all) option to see everything.
-   Use the  `-s` (kernel name) option to see the type of kernel.
-   Use the  `-r` (kernel release) option to see the kernel release.
-   Use the  `-v` (kernel version) option to see the kernel version.

commands: 

    uname -a

    uname -s
    
    uname -r
    
    uname -v

