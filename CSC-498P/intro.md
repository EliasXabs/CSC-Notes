url : bioinfo.lau.edu.lb
lau server : my username
lau server pass : my id as pass

shell commands:
    To connect to the server:
        ssh server@url
        password: my id
        
        ssh stands for secure shell
        server@url is the server address
    
    To disconnect from the server:
        exit

    echo $SHELL : to print the shell name
    echo $path : to print the path

    chsh -s "shell": to change the shell

    cd directory : to change directory
    cd .. : to go to the parent directory

    man command : to print the manual of a command
    info command : to print the manual of a command

    . : means any character
    * : means any number of characters
    | : to redirect the output of a command to another command
    > file : to redirect the output of a command to a file
    >> file : to redirect the output of a command to a file and append it to the end of the file   
    < file : to redirect the input of a command from a file
    2> file : to redirect the error output of a command to a file
    2>> file : to redirect the error output of a command to a file and append it to the end of the file
    &> file : to redirect the output and error output of a command to a file
    &>> file : to redirect the output and error output of a command to a file and append it to the end of the file
    2>&1 : to redirect the error output of a command to the output of the command

    wc -l file : to count the number of lines in a file
    wc -w file : to count the number of words in a file
    wc -c file : to count the number of characters in a file
    
    ls : to list all files in a directory
    ls -l : to list all files in a directory with their permissions
    ls -a : to list all files in a directory including hidden files
    ls -t : to list all files in a directory sorted by time
    ls -r : to list all files in a directory sorted in reverse order
    ls -S : to list all files in a directory sorted by size
    ls -R : to list all files in a directory and subdirectories
    ls -d : to list all directories in a directory
    ls -F : to list all files in a directory with a symbol after each file
    ls -1 : to list all files in a directory in one column
    ls -i : to list all files in a directory with their inode number
    ls -s : to list all files in a directory with their size
    ls -u : to list all files in a directory with their last access time

    pwd : to print the current directory

    cut -f n file : to print the nth column of a file
    cut -d " " -f n file : to print the nth column of a file with a delimiter

    cat file : to print the content of a file
    cat file1 file2 : to print the content of two files
    cat file1 file2 > file3 : to print the content of two files in a new file
    cat file1 file2 >> file3 : to print the content of two files in a new file3 and append it to the end of the file3

    head -n n file : to print the first n lines of a file
    tail -n n file : to print the last n lines of a file

    mkdir directory : to create a new directory
    mkdir -p directory : to create a new directory and all its parent directories
    mkdir -m mode directory : to create a new directory with a specific mode
    mkdir -v directory : to create a new directory and print a message for each created directory

    rmdir directory : to remove an empty directory
    rmdir -p directory : to remove an empty directory and all its parent directories
    rmdir -v directory : to remove an empty directory and print a message for each removed directory
    
    rm file : to remove a file
    rm -i file : to remove a file and ask for confirmation
    rm -f file : to remove a file without asking for confirmation
    rm -r directory : to remove a directory and all its content

    cp file1 file2 : to copy file1 to file2
    cp -i file1 file2 : to copy file1 to file2 and ask for confirmation
    cp -f file1 file2 : to copy file1 to file2 without asking for confirmation

    mv file directory : to move file to directory
    mv file1 file2 : to move file1 to file2
    mv -i file1 file2 : to move file1 to file2 and ask for confirmation
    mv -f file1 file2 : to move file1 to file2 without asking for confirmation

    touch file : to create a new file
    touch -a file : to change the access time of a file
    touch -m file : to change the modification time of a file

    chmod mode file : to change the mode of a file
    chmod ugo+rwx file : to change the mode of a file
    chmod ugo+rwx file : to change the mode of a file

    chown user file : to change the owner of a file
    chown user:group file : to change the owner and group of a file

    chgrp group file : to change the group of a file

    ln -s file link : to create a symbolic link
    ln file link : to create a hard link

    find directory -name "pattern" : to find files in a directory with a specific pattern
    find directory -type f : to find files in a directory
    find directory -type d : to find directories in a directory

    grep "pattern" file : to search for a pattern in a file
    grep -i "pattern" file : to search for a pattern in a file ignoring the case
    grep -v "pattern" file : to search for a pattern in a file and print all lines that do not match the pattern
    grep -n "pattern" file : to search for a pattern in a file and print the line number of each matching line

    sort file : to sort the lines of a file
    sort -r file : to sort the lines of a file in reverse order
    sort -n file : to sort the lines of a file numerically
    sort -k n file : to sort the lines of a file based on the nth column
    sort -t " " -k n file : to sort the lines of a file based on the nth column with a delimiter

    uniq file : to remove duplicate lines in a file

    diff file1 file2 : to compare two files
    diff -q file1 file2 : to compare two files and print a message if they are different
    diff -s file1 file2 : to compare two files and print a message if they are different

    history : to print the history of commands