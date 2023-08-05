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
