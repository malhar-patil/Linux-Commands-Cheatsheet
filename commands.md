# Linux Command Line Cheatsheet

- `whoami`: to display the username of the currently logged-in user.
- `passwd`: to change the user's password.
- `man <command>`: to display the manual pages of a command and their available options.
> Tip: To search for a specific keyword inside the man page, press '/' key followed by the keyword.
- `type <command>`: to display the information about command type.
- `<command> --help`: to find documentation for those commands whose man pages do not exist.
- `pwd`: to print the path of the current working directory starting frorm the root.
- `ls`: to list the contents (files and folders) of a directory.
- `ls -a` or `ls --all`: to list all the contents of a directory including the hidden contents.
- `ls -l`: to list the contents of a directory in long listing format.
- `cd`: to change the current working directory in the terminal.
- `cd ..`: to move one level up from current working directory into the parent directory.
> Note:
> In linux, '~' (tilde character) is used to represent the current user's home directory, and '/' (forward slash) is used to represent the user's root directory.
- `touch <file.txt>`: to create new empty files or to update the access and modification date to current time if the file already exists.
- `file <fileName>`: to determine the file type of a specified file.
- `mkdir <newDirectoryName>`: to create a new working directory.
- `nano <fileName>`: to open a file in the text editor from the terminal.
- `nano +[lineNumber] <fileName>`: to open the file at a specific line.
- `rm <fileName>`: to remove/ delete a file.
- `rm -d <folderName>`: to delete an empty folders.
- `rm -r <folderName>`: to delete non-empty folders.
> Tip: "-i" option can be used to confirm the deleteion of files and folders. It also works with nested directories.
- `mv <source> <destination>`: to move a file/files and directories from one location to another.
- `mv <currentName> <newName>`: to rename the files and folders.
- `cp <source> <destination>`: to create copies of files and folders/directories.
- `cat <file1> [<file2>]`: to read the contents of a file and print them out.
- `tac <fileName>`: to print the contents of a file in reverse, i.e. the last line in the file will be printed first and so on.
- `rev <fileName>`: to print the contents of a file in reverse order "horizontally". eg. "abc" will be printed as "cba".
- `less <fileName>`: to display the contents of a file one page at a time. (Use 'f' and 'b' keys to go one page forward or backward. Alternatively "up" and "down" arrow keys can be used to scroll by one line.)
- `head <fileName>`: to print the first 10 lines of a file.
- `head -n <fileName>`: to print first n lines of a file.
- `head -c <fileName>`: to print 'c' bytes of data from the specified file.
- `tail <fileName>`: to print the last 10 lines of the file.
> Note: "-n" and "-c" options also work with "tail" command.
- `wc <fileName>`: to print no. of lines, words and characters present in a file.
- `wc -l <fileName>`: to print the no. of lines of a file.
- `wc -w <fileName>`: to print total words in a file.
- `sort <fileName>`: to sort the contents of a file alphabetically.
- `sort -r <fileName>`: to sort the contents of a file alphabetically, but in reverse order.
- `sort -n <fileName>`: to sort numbers based on their numberical values rather than the character order.
- `sort -u <fileName>`: to sort only unique values and ignore duplicates.
- `sort -k'n' <fileName>`: to sort by field. 'n' denotes the coloumn number that needs to be sorted. It can also be used with numeric values by using the appropriate options.
