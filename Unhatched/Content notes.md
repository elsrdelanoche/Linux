# Basic Command Syntax
A command is a software program that when executed on the CLI (command line interface), performs an action on the computer. When you type in a command, a process is run by the operating system that can read input, manipulate data and produce output. A command runs a process on the operating system, which then causes the computer to perform a job.

The name of the command is often based on what it does or what the developer who created the command thinks will best describe the command's function. For example, the ls command displays a listing of information about files. 

**ls** command displays a listing of information about files.

Notes:
-Every part of the command is normally case-sensitive
-Most commands follow a simple pattern of syntax:  command [options…] [arguments…]


# Arguments
command [options…] **[arguments…]**
Can be used to specify something for the command to act upon. 

An argument can be used to specify something for the command to act upon. The ls command can be given the name of a directory as an argument, and it will list the contents of that directory. In the next example, the Documents directory will be used as an argument:
```console
sysadmin@localhost:~$ ls Documents
School           alpha-second.txt  food.txt     linux.txt     os.csv
Work             alpha-third.txt   hello.sh     longfile.txt  people.csv
adjectives.txt   alpha.txt         hidden.txt   newhome.txt   profile.txt
alpha-first.txt  animals.txt       letters.txt  numbers.txt   red.txt
```

# Options
command **[options…]** [arguments…]
Options can be used to alter the behavior of a command.
The -l option is provided to the ls command, which results in a "long display" output, meaning the output gives more information about each of the files listed:

```console
sysadmin@localhost:~$ ls -l
total 32
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Desktop                        
drwx------ 4 sysadmin sysadmin 4096 Dec 20  2017 Documents                      
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Downloads                      
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Music                          
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Pictures                       
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Public                         
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Templates                      
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Videos
```

Often the character is chosen to be mnemonic for its purpose, like choosing the letter l for long or r for reverse. 
By default, the ls command prints the results in alphabetical order, so adding the -r option will print the results in reverse alphabetical order.

```console
sysadmin@localhost:~$ ls -r
Videos  Templates  Public  Pictures  Music  Downloads  Documents  Desktop
```

Multiple options can be used at once, either given as separate options as in -l -r or combined like -lr.
```console
sysadmin@localhost:~$ ls -l -r
total 32
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Videos                         
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Templates                      
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Public                         
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Pictures                       
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Music                          
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Downloads                      
drwx------ 4 sysadmin sysadmin 4096 Dec 20  2017 Documents                      
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Desktop   
sysadmin@localhost:~$ ls -rl
total 32
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Videos                         
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Templates                      
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Public                         
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Pictures                       
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Music                          
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Downloads                      
drwx------ 4 sysadmin sysadmin 4096 Dec 20  2017 Documents                      
drwx------ 2 sysadmin sysadmin 4096 Dec 20  2017 Desktop
```
Remember the aptitude easter egg?
It is possible to alter the behavior of this command using options. See what happens when the -v (verbose) option is added:
There really are no Easter Eggs in this program.
```console
sysadmin@localhost:~$ aptitude moo                                              
There are no Easter Eggs in this program.                                       
sysadmin@localhost:~$ aptitude -v moo                                           
There really are no Easter Eggs in this program. 
sysadmin@localhost:~$ aptitude -vv moo                                          
Didn't I already tell you that there are no Easter Eggs in this program?        
sysadmin@localhost:~$ aptitude -vvv moo                                         
Stop it!                                                                        
sysadmin@localhost:~$ aptitude -vvvv moo                                        
Okay, okay, if I give you an Easter Egg, will you go away?                      
sysadmin@localhost:~$ aptitude -vvvvv moo                                       
All right, you win.                                                             
                                                                                
                               /----\                                           
                       -------/      \                                          
                      /               \                                         
                     /                |                                         
   -----------------/                  --------\                                
   ----------------------------------------------                               
```


# Print working Directory
The pwd command prints the working directory, your current location within the filesystem:

**pwd [OPTIONS]**
```console
sysadmin@localhost:~$ pwd
/home/sysadmin
```

Note: 
~ is equivalent to /home/sysadmin, representing the user's home directory.
```console
sysadmin@localhost:~$
```


# Changing Directories
Directories are a type of file used to store other files–they provide a hierarchical organizational structure.

To navigate the filesystem structure, use the cd (change directory) command to change directories.

**cd [options] [path]**

To move to the Documents directory, use it as argument to the cd command:
```console
sysadmin@localhost:~$ cd Documents                                              
sysadmin@localhost:~/Documents$
```

Note:
- Directories are equivalent to folders on Windows and Mac OS.
- It is not called "My Computer", but rather the root directory and it is represented by the / character.

To move to the root directory, use the / character as the argument to the cd command.  
```console
sysadmin@localhost:~/Documents$ cd /
sysadmin@localhost:/$
```

The argument to the cd command is more than just the name of a directory, it is actually a path. A path is a list of directories separated by the / character. For example, /home/sysadmin is the path to your home directory.
If you think of the filesystem as a map, paths are the step-by-step directions.

There are two types of paths: absolute and relative. Absolute paths start at the root of the filesystem, relative paths start from your current location.

## Absolute Paths
An absolute path allows you to specify the exact location of a directory. It always starts at the root directory, therefore it always begins with the / character. The path to the home directory /home/sysadminis an absolute path. 

Use this path as an argument to the cd command to move back into the home directory for the sysadmin user.
```console
sysadmin@localhost:/$ cd /home/sysadmin
sysadmin@localhost:~$
```
No output means the command succeeded. Go ahead and confirm this using the pwd command.
```
sysadmin@localhost:~$ pwd                                                       
/home/sysadmin
```

## Relative Paths
A relative path gives directions to a file relative to your current location in the filesystem. Relative paths do not start with the / character, they start with the name of a directory. 
```console
sysadmin@localhost:~$ cd Documents                                              
sysadmin@localhost:~/Documents$
```

A relative path begins in from with the current directory, however you don't include it in the path.
```console
sysadmin@localhost:~/Documents/$ cd School/Art
sysadmin@localhost:~/Documents/School/Art$
```


Note:
The output of the pwd command is the absolute path to the Art directory.

## Shortcuts
### The .. Characters

Regardless of which directory you are in, .. always represents one directory higher relative to the current directory, sometimes referred to as the parent directory. 
```console
sysadmin@localhost:~/Documents/School/Art$ cd ..                                
sysadmin@localhost:~/Documents/School$
```

### The . Character
Regardless of which directory you are in, the . character always represents your current directory.

### The ~ Character
The home directory of the current user is represented by the ~ character. 
To return to your home directory at any time execute the following command:
```console
sysadmin@localhost:~/Documents/School$ cd ~
sysadmin@localhost:~$
```

# Listing Files
The ls command is used to list the contents of a directory.
***ls [OPTIONS] [FILE]***
By default, when the ls command is used with no options or arguments, it will list the files in the current directory:
```console
sysadmin@localhost:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
```
To learn the details about a file, such as the type of file, the permissions, ownerships or the timestamp, perform a long listing using the -l option to the ls command. 
```console
sysadmin@localhost:~$ ls -l /var/log/
total 844                                                                       
-rw-r--r-- 1 root   root  18047 Dec 20  2017 alternatives.log                   
drwxr-x--- 2 root   adm    4096 Dec 20  2017 apache2                            
drwxr-xr-x 1 root   root   4096 Dec 20  2017 apt                                
-rw-r----- 1 syslog adm    1346 Oct  2 22:17 auth.log                           
-rw-r--r-- 1 root   root  47816 Dec  7  2017 bootstrap.log                      
-rw-rw---- 1 root   utmp      0 Dec  7  2017 btmp                               
-rw-r----- 1 syslog adm     547 Oct  2 22:17 cron.log                           
-rw-r----- 1 root   adm   85083 Dec 20  2017 dmesg                              
-rw-r--r-- 1 root   root 325238 Dec 20  2017 dpkg.log                           
-rw-r--r-- 1 root   root  32064 Dec 20  2017 faillog                            
drwxr-xr-x 2 root   root   4096 Dec  7  2017 fsck                               
-rw-r----- 1 syslog adm     106 Oct  2 19:57 kern.log                           
-rw-rw-r-- 1 root   utmp 292584 Oct  2 19:57 lastlog                            
-rw-r----- 1 syslog adm   19573 Oct  2 22:57 syslog                             
drwxr-xr-x 2 root   root   4096 Apr 11  2014 upstart                            
-rw-rw-r-- 1 root   utmp    384 Oct  2 19:57 wtmp
```

Each line corresponds to a file contained within the directory. The information can be broken down into fields separated by spaces. The fields are as follows:
## File Type
**d**rwxr-xr-x

The first field actually contains ten characters, where the first character indicates the type of file and the next nine specify permissions. The file types are:
| Symbol| File Type | Description |
| :-----------: | ----------- | ----------- |
| d |	directory	| A file used to store other files. |
| -	| regular file	| Includes readable files, images files, binary files, and compressed files. |
| l	| symbolic link	| Points to another file. |
| s |	socket	| Allows for communication between processes. |
| p |	pipe	| Allows for communication between processes. |
| b |	block file	| Used to communicate with hardware. |
| c |	character file	| Used to communicate with hardware. |

## Permissions
d**rwxr-xr-x**

Permissions indicate how certain users can access a file. Keep reading to learn more about permissions.

## Hard Link Count
-rw-r----- **1**

This number indicates how many hard links point to this file.

## User Owner
-rw-r----- 1 **syslog**

User syslog owns this file. Every time a file is created, the ownership is automatically assigned to the user who created it.

## Group Owner
-rw-rw-r-- 1 root   **utmp** 

Indicates which group owns this file

## File Size
-rw-r----- 1 syslog adm   **19573**

Directories and larger files may be shown in kilobytes since displaying their size in bytes would present a very large number. Therefore, in the case of a directory, it might actually be a multiple of the block size used for the file system. Block size is the size of a series of data stored in the filesystem.

## Timestamp
drwxr-xr-x 2 root   root   4096 **Dec  7  2017**

This indicates the time that the file's contents were last modified.

## Filename

-rw-r--r-- 1 root   root  47816 Dec  7  2017 **bootstrap.log**
The final field contains the name of the file or directory.

Consider This

In the case of symbolic links, a file that points to another file, the link name will be displayed along with an arrow and the pathname of the original file.

lrwxrwxrwx. 1 root root 22 Nov 6 2012 **/etc/grub.conf -> ../boot/grub/grub.conf**



# Sorting
By default the output of the ls command is sorted alphabetically by filename. It can sort by other methods as well.

Follow Along

The options in examples below will be combined with the -l option so the relevant details of the files are displayed. Notice fields corresponding to the search option.

The -t option will sort the files by timestamp:
```console
sysadmin@localhost:~$ ls -lt /var/log                                           
total 844                                                                       
-rw-r----- 1 syslog adm   19573 Oct  2 22:57 syslog                             
-rw-r----- 1 syslog adm    1346 Oct  2 22:17 auth.log                           
-rw-r----- 1 syslog adm     547 Oct  2 22:17 cron.log                           
-rw-rw-r-- 1 root   utmp 292584 Oct  2 19:57 lastlog                            
-rw-rw-r-- 1 root   utmp    384 Oct  2 19:57 wtmp                               
-rw-r----- 1 syslog adm     106 Oct  2 19:57 kern.log                           
-rw-r--r-- 1 root   root  18047 Dec 20  2017 alternatives.log                   
-rw-r--r-- 1 root   root  32064 Dec 20  2017 faillog                            
-rw-r----- 1 root   adm   85083 Dec 20  2017 dmesg                              
-rw-r--r-- 1 root   root 325238 Dec 20  2017 dpkg.log                           
drwxr-x--- 2 root   adm    4096 Dec 20  2017 apache2                            
drwxr-xr-x 1 root   root   4096 Dec 20  2017 apt                                
-rw-r--r-- 1 root   root  47816 Dec  7  2017 bootstrap.log                      
drwxr-xr-x 2 root   root   4096 Dec  7  2017 fsck                               
-rw-rw---- 1 root   utmp      0 Dec  7  2017 btmp                               
drwxr-xr-x 2 root   root   4096 Apr 11  2014 upstart
```          
The -S option will sort the files by file size:
```console
sysadmin@localhost:~$ ls -l -S /var/log                                         
total 844                                                                       
-rw-r--r-- 1 root   root 325238 Dec 20  2017 dpkg.log                           
-rw-rw-r-- 1 root   utmp 292584 Oct  2 19:57 lastlog                            
-rw-r----- 1 root   adm   85083 Dec 20  2017 dmesg                              
-rw-r--r-- 1 root   root  47816 Dec  7  2017 bootstrap.log                      
-rw-r--r-- 1 root   root  32064 Dec 20  2017 faillog                            
-rw-r----- 1 syslog adm   19573 Oct  2 22:57 syslog                             
-rw-r--r-- 1 root   root  18047 Dec 20  2017 alternatives.log                   
drwxr-x--- 2 root   adm    4096 Dec 20  2017 apache2                            
drwxr-xr-x 1 root   root   4096 Dec 20  2017 apt                                
drwxr-xr-x 2 root   root   4096 Dec  7  2017 fsck                               
drwxr-xr-x 2 root   root   4096 Apr 11  2014 upstart                            
-rw-r----- 1 syslog adm    1346 Oct  2 22:17 auth.log                           
-rw-r----- 1 syslog adm     547 Oct  2 22:17 cron.log                           
-rw-rw-r-- 1 root   utmp    384 Oct  2 19:57 wtmp                               
-rw-r----- 1 syslog adm     106 Oct  2 19:57 kern.log                           
-rw-rw---- 1 root   utmp      0 Dec  7  2017 btmp
```
The -r option will reverse the order of any type of sort. Notice the difference when it is added to the previous example:
```console
sysadmin@localhost:~$ ls -lSr /var/log
total 844                                                                       
-rw-rw---- 1 root   utmp      0 Dec  7  2017 btmp                               
-rw-r----- 1 syslog adm     106 Oct  2 19:57 kern.log                           
-rw-rw-r-- 1 root   utmp    384 Oct  2 19:57 wtmp                               
-rw-r----- 1 syslog adm     654 Oct  2 23:17 cron.log                           
-rw-r----- 1 syslog adm    1669 Oct  2 23:17 auth.log                           
drwxr-xr-x 2 root   root   4096 Apr 11  2014 upstart                            
drwxr-xr-x 2 root   root   4096 Dec  7  2017 fsck                               
drwxr-xr-x 1 root   root   4096 Dec 20  2017 apt                                
drwxr-x--- 2 root   adm    4096 Dec 20  2017 apache2                            
-rw-r--r-- 1 root   root  18047 Dec 20  2017 alternatives.log                   
-rw-r----- 1 syslog adm   19680 Oct  2 23:17 syslog                             
-rw-r--r-- 1 root   root  32064 Dec 20  2017 faillog                            
-rw-r--r-- 1 root   root  47816 Dec  7  2017 bootstrap.log                      
-rw-r----- 1 root   adm   85083 Dec 20  2017 dmesg                              
-rw-rw-r-- 1 root   utmp 292584 Oct  2 19:57 lastlog                            
-rw-r--r-- 1 root   root 325238 Dec 20  2017 dpkg.log
```  
The numbers in file size field switch from descending to ascending.

Used alone the -r option with list the files in reverse alphabetical order:
```console
sysadmin@localhost:~$ ls -r /var/log                                            
wtmp     lastlog   faillog   cron.log       auth.log  alternatives.log
upstart  kern.log  dpkg.log  btmp           apt
syslog   fsck      dmesg     bootstrap.log  apache2
```


# Administrative Access
There are many Linux commands which deal with sensitive information like passwords, system hardware, or otherwise operate under other exceptional circumstances. Preventing regular users from executing these commands helps to protect the system. Logging in as the root user provides administrative access, allowing for the execution of some of the privileged commands.
The **su** Command
**su OPTIONS USERNAME**
The su command allows you to temporarily act as a different user. It does this by creating a new shell. The shell is simply a text input console that lets you type in commands. By default, if a user account is not specified, the su command will open a new shell as the root user, which provides administrative privileges.
```console
sysadmin@localhost:~$ su  -
Password:
root@localhost:~#
```

Note the command prompt has changed to reflect that you are now logged in as the root user. To logout and return to the sysadmin account, use the exit command. Note the prompt changes back:
```console
root@localhost:~# exit
logout
sysadmin@localhost:~$
```
## The **sudo** Command (super user **do**)
**sudo [OPTIONS] COMMAND**

The sudo command allows a user to execute a command as another user without creating a new shell. Instead, to execute a command with administrative privileges, use it as an argument to the sudo command. Like the su command, the sudo command assumes by default the root user account should be used to execute commands.

Note: The prompt for the password will not appear again as long as the user continues to execute sudo commands less than five minutes apart.

```console
sysadmin@localhost:~$  sudo sl
[sudo] password for sysadmin:

                             (@@) (  ) (@)  ( )  @@    ()    @     O     @
                         (   )
                     (@@@@)
                  (    )

                (@@@)
            ====        ________                ___________
        _D _|  |_______/        \__I_I_____===__|_________|
         |(_)---  |   H\________/ |   |        =|___ ___|      _________________
         /     |  |   H  |  |     |   |         ||_| |_||     _|
        |      |  |   H  |__--------------------| [___] |   =|
        | ________|___H__/__|_____/[][]~\_______|       |   -|
        |/ |   |-----------I_____I [][] []  D   |=======|____|__________________
      __/ =| o |=-~~\  /~~\  /~~\  /~~\ ____Y___________|__|____________________
       |/-=|___|=    ||    ||    ||    |_____/~\___/          |_D__D__D_|  |_D__
        \_/      \_O=====O=====O=====O/      \_/               \_/   \_/    \_/
```
Once the command has completed, notice the prompt has not changed, you are still logged in as sysadmin. The sudo command only provides administrative access for the execution of the specified command. This is an advantage as it reduces the risk that a user accidentally executes a command as root. The intention to execute a command is clear; the command is executed as root if prefixed with the sudo command. Otherwise, the command is executed as a regular user.

Now we can notice the difference between "su" and "sudo," or superuser and superuser do. When using "su," we switch completely to root to execute commands that require permissions. On the other hand, with "sudo," we will use it to execute a command that requires permissions while still remaining the same user, only the superuser, like a third party, will handle that command.


# Permissions
Permissions determine the ways different users can interact with a file or directory. When listing a file with the ls -l command, the output includes permission information. 
```console
sysadmin@localhost:~/Documents$ ls -l hello.sh                                  
-rw-r--r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh
```
## Permissions Field
-**rw-r--r--** 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh
After the first character (the file type character), the permissions are displayed. The permissions are broken into three sets of three characters:
### Owner
- **rw-** r--r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh
The first set is for the user who owns the file. If your current account is the user owner of the file, then the first set of the three permissions will apply and the other permissions have no effect.

The user who owns the file, and who these permissions apply to, can be determined by the user owner field:

-rw-r--r-- 1 **sysadmin** sysadmin 647 Dec 20  2017 hello.sh

### Group
-rw- **r--** r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh
The second set is for the group that owns the file. If your current account is not the user owner of the file and you are a member of the group that owns the file, then the group permissions will apply and the other permissions have no effect.

The group for this file can be determined by the group owner field:

-rw-r--r-- 1 sysadmin **sysadmin** 647 Dec 20  2017 hello.sh

### Other
-rw-r-- **r--** 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh
The last set is for everyone else, any one who that first two sets of permissions do not apply to. If you are not the user who owns the file or a member of the group that owns the file, the third set of permissions applies to you.

## Permission Types
There are three different permissions that can be placed on a file or directory: read, write, and execute. The manner in which these permissions apply differs for files and directories, as shown in the chart below:

| Permission | Effects on File	| Effects on Directory |
| :---------:|------------------| ---------------------|
| read (r)	 | Allows for file contents to be read or copied.	| Without execute permission on the directory, allows for a non-detailed listing of files. With execute permission, ls -l can provide a detailed listing. |
| write (w)	 | Allows for contents to be modified or overwritten. Allows for files to be added or removed from a directory. |	For this permission to work, the directory must also have execute permission. |
| execute (x)| Allows for a file to be run as a process, although script files require read permission, as well. |	Allows a user to change to the directory if parent directories have execute permission as well. |


# Changing File Permissions
The __chmod__ command is used to change the permissions of a file or directory. Only the root user or the user who owns the file is able to change the permissions of a file.
chmod (change the modes of access).

There are two techniques for changing permissions with the chmod command: symbolic and octal. The symbolic method is good for changing one set of permissions at a time. The octal or numeric method requires knowledge of the octal value of each of the permissions and requires all three sets of permissions (user, group, other) to be specified every time.

## The Symbolic Method
chmod [<SET><ACTION><PERMISSIONS>]... FILE
To use the symbolic method of chmod first indicate which set of permissions is being changed:

| Symbol |	Meaning |
| :-----:|----------|
| u |	User: The user who owns the file. |
| g |	Group: The group who owns the file. |
| o |	Others: Anyone other than the user owner or member of the group owner. |
| a |	All: Refers to the user, group and others. |

Next, specify an action symbol:
| Symbol |	Meaning |
| :-----:|----------|
| + |	Add the permission, if necessary|
| = |	Specify the exact permission |
| -	| Remove the permission, if necessary|

After an action symbol, specify one or more permissions to be acted upon.
| Symbol |	Meaning |
| :-----:|----------|
| r | read |
| w |	write |
| x |	execute |

Finally, a space and the pathnames for the files to assign those permissions.
-rw-r--r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh 

```console
sysadmin@localhost:~/Documents$ ./hello.sh                                      
-bash: ./hello.sh: Permission denied
```

Since the system is currently logged in as the sysadmin user, and sysadmin is the owner of this file, giving the user owner the execute permission should allow you to execute this script. Using the chmod command with the u character to represent the user owner permission set, the + character to indicate a permission is being added, and the x character to represent the execute permission, the command should be executed as follows:
```console
sysadmin@localhost:~/Documents$ chmod u+x hello.sh
```
No output indicates the command succeeded. Confirm by checking the permissions using the ls -l command.
The user owner now has the execute permission listed:
```console
sysadmin@localhost:~/Documents$ ./hello.sh   
-bash: ./hello.sh: Permission denied                                            
sysadmin@localhost:~/Documents$ ls -l hello.sh                                  
-rw-r--r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh                        
sysadmin@localhost:~/Documents$ chmod u+x hello.sh                              
sysadmin@localhost:~/Documents$ ls -l hello.sh                                  
-rwxr--r-- 1 sysadmin sysadmin 647 Dec 20  2017 hello.sh                        
sysadmin@localhost:~/Documents$ ./hello.sh                                      
 ______________                                                                 
( Hello World! )                                                                
 --------------                                                                 
        \                                                                       
         \                                                                      
           <(^)                                                                 
            ( )                                                                 
```
## The OCtal Method
To learn more about the octal method check out NDG Linux Essentials!

Note: "./" This indicates the "command" should be run from the current directory.
