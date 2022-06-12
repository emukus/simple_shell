
0x16. C - Simple Shell

Description
Implementing a simple shell that display a prompt and waits for the user to type a command that is to be executed

Requirements
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
A README.md file, at the root of the folder of the project is mandatory
Your code should use the Betty style.
Your shell should not have any memory leaks
No more than 5 functions per file
All your header files should be include guarded
Write a README with the description of your project
You should have an AUTHORS file at the root of your repository, listing all individuals having contributed content to the repository.

Allowed functions and system calls
access (man 2 access)
chdir (man 2 chdir)
close (man 2 close)
closedir (man 3 closedir)
execve (man 2 execve)
exit (man 3 exit)
_exit (man 2 _exit)
fflush (man 3 fflush)
fork (man 2 fork)
free (man 3 free)
getcwd (man 3 getcwd)
getline (man 3 getline)
getpid (man 2 getpid)
isatty (man 3 isatty)
kill (man 2 kill)
malloc (man 3 malloc)
open (man 2 open)
opendir (man 3 opendir)
perror (man 3 perror)
read (man 2 read)
readdir (man 3 readdir)
signal (man 2 signal)
stat (__xstat) (man 2 stat)
lstat (__lxstat) (man 2 lstat)
fstat (__fxstat) (man 2 fstat)
strtok (man 3 strtok)
wait (man 2 wait)
waitpid (man 2 waitpid)
wait3 (man 2 wait3)
wait4 (man 2 wait4)
write (man 2 write



Compilation

gcc -Wall -Werror -Wextra -pedantic 

Testing
Interactive Mode

$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$

Non-interactive Mode
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$

Features
Display a prompt and wait for the user to type a command
The prompt is displayed again each time a command has been executed.
Handles command lines with arguments
Implements the exit built-in, that exits the shell
Implements the env built-in, that prints the current environment
Implements PATH variable to find executable command


Authors
Jedidah Mweru
Eugene Mukuna



