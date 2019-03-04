# terminal-cheatsheet

## Shortcuts
|  Shortcut                       | Description |
| ------------------------------- | ----------- |
| `ctrl c`                        | Halts current command
| `ctrl d`                        | Deletes on character forwards or logs out of session (like exit)
| `ctrl g`                        | Aborts the current command
| `ctrl j`                        | Same as return
| `ctrl l`                        | Clear the terminal
| `ctrl m`                        | Same as return
| `ctrl n`                        | Next line in command history
| `ctrl p`                        | Previous line in comman history
| `ctrl r`                        | Reverse search of history
| `ctrl s`                        | Search forwards in history
| `ctrl z`                        | Stops current command (resume with fg in foreground or bg in background)
| `!!`                            | Repeat last command

## Movement
|  Movement                       | Description |
| ------------------------------- | ----------- |
| `ctrl a`                        | Move cursor to start of line
| `ctrl b`                        | Move cursor back one character
| `ctrl e`                        | Move cursor to end of line
| `ctrl f`                        | Move cursor forwards one character
| `option b`                      | Move backwords one word
| `option f`                      | Move forwards one word

## Cut and paste (‘Kill and yank’ for old schoolers)
|  Shortcut                       | Description |
| ------------------------------- | ----------- |
| `ctrl k`                        | Cut from cursor to the end of line.
| `option d`                      | Cut from cursor to the end of word.
| `option backspace`              | Cut from cursor to the start of word.
| `ctrl w`                        | Cut from cursor to previous whitespace.
| `ctrl y`                        | Paste the last cut text.
| `option y`                      | Loop through and paste previously cut text. Meta + y (use it after Ctrl + y)
| `option +`                      | Loop through and paste the last argument of previous commands. Meta + .

## Basic
|  Command                        | Description |
| ------------------------------- | ----------- |
| `export`                        | Displays all environment variables or sets environment variable if used with value
| `clear`                         | Clears the terminal window

## File commands
|  Command                        | Description |
| ------------------------------- | ----------- |
| `ls`                            | lists your files
| `ls -l`                         | lists your files in 'long format', which contains the exact size of the file, who owns the file and who has the right to look at it, and when it was last modified
| `ls -a`                         | lists all files, including hidden files
| `ll`                            | list directiry contents |
| `ln -s <filename> <link>`       | creates symbolic link to file
| `touch <filename>`              | creates or updates your file
| `cat`                           | prints out all file contents
| `cat > <filename>`              | places standard input into file
| `less <filename>`               |
| `more <filename>`               | shows the first part of a file (move with space and type q to quit)
| `head <filename>`               | outputs the first 10 lines of file
| `tail <filename>`               | outputs the last 10 lines of file (useful with -f option)
| `mv <filename1> <filename2>`    | moves a file
| `cp <filename1> <filename2>`    | copies a file
| `rm <filename>`                 | removes a file
| `diff <filename1> <filename2>`  | compares files, and shows where they differ
| `wc <filename>`                 | tells you how many lines, words and characters there are in a file
| `chown`                         |
| `chmod -options <filename>`     | lets you change the read, write, and execute permissions on your files
| `gzip <filename>`               | compresses files
| `gunzip <filename>`             | uncompresses files compressed by gzip
| `gzcat <filename>`              | lets you look at gzipped file without actually having to gunzip it


## Folder commands
|  Command                        | Description |
| ------------------------------- | ----------- |
| `mkdir <dirname>`               | makes a new directory
| `cd`                            | changes to home
| `cd <dirname>`                  | changes directory
| `pwd`                           | tells you where you currently are
| `find <dirname>`                | list all contents of directory and subdirectories


## Misc
|  Command                        | Description |
| ------------------------------- | ----------- |
| `&&`                            | Run next command if previous command succeeded
| `;`                             | Run multiple commands
| `Pipe`                          | Pipe command to another command
| `*`                             |
| `say`                           | Say text out loud
| `exit`                          |
| `echo`                          |
| `sudo`                          |


## Search / Grep
|  Command                        | Description |
| ------------------------------- | ----------- |
| `grep <pattern> <filenames>`    | looks for the string in the files
| `grep -r <pattern> <dir>`       | search recursively for pattern in directory

## Curl
|  Command                        | Description |
| ------------------------------- | ----------- |
| `curl <url>`                    | retireves content
| `curl -o <filename> <url>`      | retireves content and save it to given filename
| `curl -O <filename> <url>`      | retireves content and save it with its original filename
| `curl -I <url>`                 | retireves only the HTTP headers of specified resource


## Input/Output Redirectors.
|  Command                        | Description |
| ------------------------------- | ----------- |
| `cmd1|cmd2`                     | pipe; takes standard output of cmd1 as standard input to cmd2
| `> file`                        | directs standard output to file
| `< file`                        | takes standard input from file
| `>> file`                       | directs standard output to file; append to file if it already exists
| `>|file`                        | forces standard output to file even if noclobber is set
| `n>|file`                       | forces output to file from file descriptor n even if noclobber is set
| `<> file`                       | uses file as both standard input and standard output
| `n<>file`                       | uses file as both input and output for file descriptor n
| `<<label`                       | here-document
| `n>file`                        | directs file descriptor n to file
| `n<file`                        | takes file descriptor n from file
| `n>>file`                       | directs file description n to file; append to file if it already exists
| `n>&`                           | duplicates standard output to file descriptor n
| `n<&`                           | duplicates standard input from file descriptor n
| `n>&m`                          | file descriptor n is made to be a copy of the output file descriptor
| `n<&m`                          | file descriptor n is made to be a copy of the input file descriptor
| `&>file`                        | directs standard output and standard error to file
| `<&-`                           | closes the standard input
| `>&-`                           | closes the standard output
| `n>&-`                          | closes the ouput from file descriptor n
| `n<&-`                          | closes the input from file descripor n
