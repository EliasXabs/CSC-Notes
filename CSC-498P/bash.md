# Scripting using bash
## Syntax
- `#!/bin/bash` is the shebang line
## Must know
- use `#!/bin/bash` to specify the interpreter
- the script is case, and space sensitive
- u can use every command that u can use in the terminal
- to declare a variable use `VAR=VALUE`
- to declare an array use `VAR=(VALUE1 VALUE2 VALUE3)`
- use `chmod u+x FILENAME` to make the file executable
- use g to make the file executable for the group
- use o to make the file executable for others
- use a to make the file executable for all
- use `export PATH=$PATH:/path/to/file` to add the file to the path temporarily
- use `nano bash_profile` to add the file to the path permanently
- use `alias NAME='SCRIPT.sh'` to create an alias
## Types of variable 
1. Scalar variable:
   - is a variable that can hold only one value at a time.
   - we use `$` sign to access the value of the variable.
2. Array variable :
   - is a variable that can hold multiple values at a time.
   - we use `@` sign to access the value of the variable.
   - u can use `${VAR[0]}` to access the first value of the array.
   - u can use `${VAR[@]}` or `${VAR[*]}` to access all the values of the array.
### Global and local variables
- global variables are accessible from anywhere in the script
- local variables are accessible only from the function in which they are declared
#### Some global variables
- `$0` is the name of the script
- `$n` is the nth argument
- `$HOME` is the home directory of the user 
- `$HOSTNAME` is the name of the host
- `$SHELL` is the shell that is used
- `$PATH` is the path to the executable files
## Strings
- if u use `''` the string is treated as a raw string, u can use `""` to use variables inside the string
- `${#VAR}` returns the length of the string
- `${VAR:START:LENGTH}` returns the substring of the string without the trailing spaces
- u can use negative indexes to access the string from the end
- `${VAR#?}` returns the string without the first character
- `${VAR%?}` returns the string without the last character
## Arguments
- `$#` returns the number of arguments
- use `$@` to access all the arguments
- `$n` returns the nth argument

## If statement
- `if [ condition ]; then` is the if statement
- `elif [ condition ]; then` is the else if statement
- `else` is the else statement
- use `fi` to close the if stateme
- we have five types of conditions:
  - `-eq` : equal
  - `-ne` : not equal
  - `-gt` : greater than
  - `-lt` : less than
  - `-ge` : greater than or equal
  - `-le` : less than or equal
- operators:
  - `-a` : and
  - `-o` : or
  - `!` : not
> Example:
> ```bash
> if [ $1 -gt 10 ]; then
>   echo "greater than 10"
> elif [ $1 -eq 10 ]; then
>   echo "equal to 10"
> else
>   echo "less than 10"
> fi
>```

## For loop
- use `for VAR in LIST; do` to start the for loop
- use `done` to end the for loop
- use `break` to break the loop
- use `{1..10}` to create a list from 1 to 10
> Example:
> ```bash
> for i in 1 2 3 4 5; do
>   echo $i
> done
> ```

> Exercise 1:
> How to print all files using a for loop?
> ```bash
> for i in *; do
>   echo $i
> done
> ```
- The star `*` specifies all the files in the current directory
- To specify all the files in the current directory and all the subdirectories use `**/*`
- To sepcify a certain type of files use `*.txt`

## While loop
- use `while [ condition ]; do` to start the while loop
- use `done` to end the while loop
- use `shift` to shift the arguments
> Example:
> ```bash
> while [ $i -le 10 ]; do
>   echo $i
>   i=$((i+1))
> done
> ```

## Switch case
- use `case $VAR in` to start the switch case
- use `*)` to specify the default case
- use `anything)` to specify a case
- use `;;` to end the case
- use `esac` to end the switch case
> Example:
> ```bash
> case $1 in
>   -f) echo "one" ;;
>   -v) echo "two" ;;
>   *) echo "other" ;;
> esac
>
> ```


