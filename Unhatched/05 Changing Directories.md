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
