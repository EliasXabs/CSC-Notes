# Scripting using bash
## Must know
- use `#!/bin/bash` to specify the interpreter
- the script is case, and space sensitive
- u can use every command that u can use in the terminal
- to declare a variable use `VAR=VALUE`
- to declare an array use `VAR=(VALUE1 VALUE2 VALUE3)`
- use `chmod u+x FILENAME` to make the file executable
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



