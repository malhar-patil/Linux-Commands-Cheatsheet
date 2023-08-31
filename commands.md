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
