# Linux Command Line Cheatsheet

- `whoami`: to display the username of the currently logged-in user.
- `passwd`: to change the user's password.
- `man <command>`: to display the manual pages of a command and their available options.
   - To search for a specific keyword inside the man page, press '/' key followed by the keyword.
- `type <command>`: to display the information about command type.
- `<command> --help`: to find documentation for those commands whose man pages do not exist.
- `pwd`: to print the path of the current working directory starting frorm the root.
- `ls`: to list the contents (files and folders) of a directory.
- `ls -a` or `ls --all`: to list all the contents of a directory including the hidden contents.
- `ls -l`: to list the contents of a directory in long listing format.
- `cd`: to change the current working directory in the terminal.
- `cd ..`: to move one level up from current working directory into the parent directory.
> Note: In linux, '~' (tilde character) is used to represent the current user's home directory, and '/' (forward slash) is used to represent the user's root directory.
- `echo <message>`: to display text or output to terminal.
- `touch <file.txt>`: to create new empty files or to update the access and modification date to current time if the file already exists.
- `file <fileName>`: to determine the file type of a specified file.
- `mkdir <newDirectoryName>`: to create a new working directory.
- `nano <fileName>`: to open a file in the text editor from the terminal.
- `nano +[lineNumber] <fileName>`: to open the file at a specific line.
- `rm <fileName>`: to remove/ delete a file.
- `rm -d <folderName>`: to delete an empty folders.
- `rm -r <folderName>`: to delete non-empty folders.
   - Tip: "-i" (iterative) option can be used to confirm the deleteion of files and folders. It also works with nested directories.
- `mv <source> <destination>`: to move a file/files and directories from one location to another.
- `mv <currentName> <newName>`: to rename the files and folders.
- `cp <source> <destination>`: to create copies of files and folders/directories.
- `cat <file1> [<file2>]`: to read the contents of a file and print them out.
- `tac <fileName>`: to print the contents of a file in reverse, i.e. the last line in the file will be printed first and so on.
- `rev <fileName>`: to print the contents of a file in reverse order "horizontally". Ex. "abc" will be printed as "cba".
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
- `sort -n <fileName>`: to sort numbers based on their numerical values rather than the character order.
- `sort -u <fileName>`: to sort only unique values and ignore duplicates.
- `sort -k'n' <fileName>`: to sort by field. 'n' denotes the coloumn number that needs to be sorted. It can also be used with numeric values by using the appropriate options.
- `history`: to display the previously executed shell commands in the order they were executed. To reuse the command without typing it again, we can reference its number with '!' symbol. Ex. `!420`.
- `tr`: to translate, delete or merge characters or words. Refer the man page of explore all the options of 'tr' command.
- `tee`: to redirect output of the command to both, terminal (standard ouput) and file simultaneously.
- `locate <fileName/ Path>`: to quickly locate files and directories on the system. `locate` command uses pre-generated database for searching.
   - Useful options often used with `locate` command:
     1) '-i' to ignore the casing.
     2) '-l' or '--limit' to limit the number of entries that locate retrives.
     3) '-e' prints only the entries that are present at the time locate is run.
- `sudo updatedb`: to update the database used by locate command.
- `find`: to list all the files and folders in the present directory.
- `find <filePath>/`: to find files and folders by path.
- `find -type f`: to search and list only the rexular files within the current directory and its sub-directories.
- `find -type d`: to search and list for directories within the current directory and its sub-directories.
- `find -name "<fileName>"` to search for a file with a specific pattern.
   - `-i` option can be used with `-name` option to avoid casing.
- `find -size ±<fileSize>`: to find files with a specific file size. We can search for exact file size or use '+' or '-' symbols to specify a range of values. Ex. `find -size +20M` will list all the files whose sizes are greater than 20 MB.
- `find -user <Username>`: to search for files and directories owned by specific user.
> Note: All the options mentioned above for `find` command can be combined together to further narrow down the search and get more specific results.
- Commonly used `find` options to filter the results based on time are:
  - `-amin n`: to find files that were last accessed (when the file was last read or opened). n minutes ago. We can specify +n for "greater than n minutes
     ago" and -n for "less than n minutes ago".
  - `-mmin n`: to find files that were last modified (when the content of the file was last modified) n minutes ago.
  - `-cmin n`: to find files that were last changed (when the file was last modified or had its attributes changed) n minutes ago.
- `find -exec {} ;`: to execute a specified command on each file or item found by the find command. Ex. `find -name "broken*" -exec rm '{}' ';'` will delete all the files that start with "broken" in the file name.
   - Note: We need to wrap the {} and ; in quotes because those characters have special meanings otherwise.
- `xargs`: xargs reads items from standard input, separated by blanks (spaces or newlines) and then executes a command using those items.
  - Ex. `echo "Folder1" "Folder2" | mkdir` will give an error as mkdir expects us to pass arguments and not standard inputs. Instead we can use `echo "Folder1" "Folder2" | xargs mkdir` command, which will create two directories "Folder1" and "Folder2".
- `grep <PATTERN> <FILENAME>`: to search and filter text based on the pattern provided within a file. Ex. `grep "indigo" colors.txt` will return all the instances of "indigo" inside the 'colors.txt' file.
  - Commonly used 'grep' options:
    - `i`: to make the search case insensitive.
    - `-w`: to ensure that 'grep' only matches words, rather than fragments locate inside of other words. Ex. `grep -w "ate" random.txt` will only match the word "ate" and not "donate", "abbreviate", etc.
    - `-r`: to perform a recursive search which will include all files under a directory, subdirectories and their files.
    - `-c`: to count and display the number of lines that match the specified pattern.
    - `-m<num>`: to limit the number of lines/matches 'grep' command will return. -m5 will display 5 results at max.
    - `-n`: to display line numbers along with matching lines when searching for a pattern in a specific file.
    - `-o`: to display only the matches instead of printing out the entire line containing each match.
    - `A<n>`: to display matching lines as well as n lines immediately following each matching line.
    - `B<n>`: to display matching lines as well as n lines preceding each matching line.
    - `C<n>`: to show matching lines as well as display n lines before and after each matching line.
- We can provide rexular expressions to grep. Rexular expressions helps us match complex patterns. The syntax for the same is as follows:
   - `.` - matches any single character.
   - `^` - matches the start of a line.
   - `$` - matches the end of a line.
   - `[abc]` - matches any character in the set.
   - `[^abc]` - matches any char NOT in set.
   - `[A-Z]` - matches characters in a range.
   - `*` - repeat previous expression 0 or more times.
   - `\` - escape meta-characters.
> Note: `-E` option must be used to enable the use of extended rexular expressions when specifying search patterns.
- `ps -aux`: to display list of all the running tasks in Unix/ Unix-Like Operating Systems.
- `su - <usename>`: to switch to another user's account. It initates a new login session with specified user's environment and privilexes.
- `chmod <mode> <fileName>`: to change the permissions (read/write/execute) of a file and directory.
  - Shorthand notations used with the `chmod` command to specify the catexory of users (owner, group, others, or all) for whom permissions are being modified are:
    - `u` - User (the owner of the file).
    - `g` - Group (members of the group a file belongs to).
    - `o` - Others (users who do not come under the catexory of user or group).
    - `a` - All of the above.
  - Notations to specify how permissions should be modified for a file or directory are:
    - `+` - Grants the permissions.
    - `-` - Removes/ Revokes the permissions.
    - `=` - Set a permission and remove others.
  - Notations to specify different types of permissions that can be assigned to files and directories are:
    - `r` - 'Read' permission.
    - `w` - 'Write' permission.
    - `x` - 'Execute' permission.
  - Ex. `chmod g+w <fileName>`: Grants 'write' permission to the 'group'.
- `Chmod` also supports another way of representing permission patterns using octal numbers (base 8):
   |Octal| Binary|File Mode|
   |-----|-------|---------|
   |0|000|---|
   |1|001|--x|
   |2|010|-w-|
   |3|011|-wx|
   |4|100|r--|
   |5|101|r-x|
   |6|110|rw-|
   |7|111|rwx|
  - Ex. `chmod 664 <fileName>` sets the permissions as -rw-rw-r--.
- `sudo`: to allow authorized users to execute commands with the privileges of the superuser (root).
- `sudo -l`: to list the permissions and privileges granted to the current user or a specific user.
- `chown <username> <fileName>`: to change the owner of a file or directory.
- `chown :<groupName> <fileName>`: to change the group owner of a file.
- `chown <username>:<groupName> <fileName>`: to change the owner and group owner of a file at the same time.
- `groups <username>`: to display the names of the groups to which a particular user belongs to.
- `addgroup <groupName>`: to create new groups.
- `adduser <username> <groupName>`: to add user to a group.
