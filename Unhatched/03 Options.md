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
