# Introduction

## Credentials for the lau server

>url : bioinfo.lau.edu.lb\
lau server name : my username\
lau server pass : my id


## How to connect to the server:
> ### To connect to the server:
>       ssh username@url
>   It should then prompt you for the password fill it accordingly
> 
>ssh stands for secure shell\
>server@url is the server address
        
> ### To disconnect from the server:
>       exit

## Basic commands:
> ### Some globla variables:
> ----
> `$SHELL` is a variable that contains the name of the shell
> 
> `$PATH` is a variable that contains the list of directories that the shell searches for commands
>
> `$HOME` is a variable that contains the path to the home directory
>
>  ### Introduction to commands:
> ----
>`echo` is a command that prints the string given to the terminal
>
>       echo "Hello World"
> `chsh` is used to change the shell
>
>       chsh -s "shell"
>   You can use the command `echo $SHELL` to know your available shells\
>
> `history` is a command that prints the history of commands
>
>       history
>
> `man` and `info` are commands that are used to print the manual of a command
>
>       man command
>>
>       info command
> ### Directory commands:
> ----
>`ls` is a command that lists all the files in the current directory
>
>       ls
> some flags are:
> 
> - `-l` : to list all files in a directory with their permissions
> - `-d` : to list all directories in a directory
> - `-r` : to list all files in a directory sorted in reverse order
> - `-t` : to list all files in a directory sorted by time
> - `-S` : to list all files in a directory sorted by size
> - `-R` : to list all files in a directory and subdirectories
> - `-s` : to list all files in a directory with their size
> - `-u` : to list all files in a directory with their last access time
> - `-a` : to list all files in a directory including hidden files
>
> `pwd` is a command that prints the current directory
>
>       pwd
>
> `cd` is a command that changes the current directory
>
>       cd directory
> You can use the `./` to start from the current directory\
> as well as `../` to go to the parent directory 
>
> `mkdir` is a command that is used to create a new directory
>
>       mkdir directory
> creates a new directory
>
> some flags :
>
> `-p` : to create a new directory and all its parent directories
> `-v` : to create a new directory and print a message for each created directory
>
> `rmdir` is a command that is used to remove an empty directory
>
>       rmdir directory
>
> some flags:
>
>  - `-p` : to remove an empty directory and all its parent directories
>  - `-v` : to remove an empty directory and print a message for each removed directory
>
> `find` is a command that is used to find files in a directory
>
>       find directory -name "pattern"
>
> this will find files in directory with a specific pattern
>
> some flags :
>  - `-type f` : to find files in a directory
>  - `-type d` : to find directories in a directory
>
>
> ### File manipulation commands:
> ----
>
> `touch` is used to create a new file
>
>       touch file
> this will create a file named file
> 
> `wc` Stands for word count and its used to count the number of lines, words and characters in a file
>
>       wc -l file
> is used to count the number of lines in a file
>
>       wc -w file
> is used to count the number of words in a file
>
>       wc -c file
> is used to count the number of characters in a file
> 
> `cat` is a command that is used to print the content of a file
> 
>       cat file
> prints the content of file
>
>       cat file1 file2
> prints the content of file1 and file2
>
>       cat file1 file2 > file3
> prints the content of file1 and file2 in file3 if it doesn't exist it creates it
>
> `cut` is a command that is used to print selected parts of lines from each file to the standard output
> 
> some flags are:
> 
> - `f` : to print the nth column of a file
> - `d` : to print the nth column of a file with a delimiter
>
>       cut -f n file
>       cut -d " " -f n file
>
>
> `head` and `tail` are used to print the first and last lines of a file respectively.
>
>       head -n n file
> prints the first n lines of a file
>
>       tail -n n file
> prints the last n lines of a file
>
> `rm` is a command that is used to remove a file
>
>       rm file
>
> `cp` is a command that is used to copy a file to another file
>
>       cp file1 file2
> 
> this command fill copy file1 to file2
> 
> `mv` is a command that is used to move a file to another file or directory
>
>       mv file1 file2
>
> this will move file1 to file2
>
>       mv file directory
> 
> while this will move file form its current directory to directory
>
> `uniq` is a command that is used to remove duplicate lines from a file
>
>       uniq file
>
> `grep` is a command that is used to search for a pattern in a file
>
>       grep "pattern" file
> this will search for the pattern in the file
>
> some flags: 
>  - `-i` : to ignore the case of the pattern
>  - `-v` : to print the lines that don't match the pattern
>  - `-c` : to print the number of lines that match the pattern
>  - `-n` : to print the line number of the lines that match the pattern
>
> 

## Basic regex:
> - `.` : means any character
> - `*` : means any number of characters

## Well known redirections:
> - `|` : to redirect the output of a command to another command
> - `> file` : to redirect the output of a command to a file and erasing the old content of the file
> - `>> file` : to redirect the output of a command to a file and append it to the end of the file
> - `< file` : to redirect the input of a command from a file
> - `2> file` : to redirect the error output of a command to a file
> - `2>> file` : to redirect the error output of a command to a file and append it to the end of the file
> - `&> file` : to redirect the output and error output of a command to a file
> - `&>> file` : to redirect the output and error output of a command to a file and append it to the end of the file


## Extras:
> `sort` is a command that is used to sort the lines of a file in alphabetical order
>
>       sort file
> some flags:
> - `-r` : to sort the lines of a file in reverse order
> - `-n` : to sort the lines of a file numerically
> - `-k n` : to sort the lines of a file based on the nth column
> - `-t " "` : to sort the lines of a file based on the nth column with a delimiter
>
> `diff` is a command that is used to compare two files
>
>       diff file1 file2
>
> some flags:
>  - `-q` : to compare two files and print a message if they are different