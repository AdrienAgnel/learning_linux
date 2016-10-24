# Learning Linux
Chosen linux commands and how to use them ! (not all options are listed)

### mv
Move a file or a folder into a target folder.

mv [source_folder/file] [target_folder]

### cat
To concatenate files or print files.

cat [file]

### grep
Filter folders, files or text based on a given set of characters.
grep -n "[characters]" [file_name]

### ln
Create a symlink.

ln -s [target_file] [symlink_name]

### ls
List files and folder at given path.

ls -l (one file one line view) -a (list all files, even hidden ones) [path/to/file-folder]

### nano
Command line text editor.

nano [file_name]

^X -> Exit

### rm
Remove some specified files.
rm -f (force) -r (recursive) -v (verbose)

### chmod
Change file or folder access rights.
chmod g-w [file_name] -> remove write permission to group
chmod u-wr [file_name] -> remove read and write permission to user

### chown
Change file owner.
chown root [file_name] -> make root the owner of the file

### sed
(among others) remove first lines of a file
sed -i [startIndex],[endIndex]d [file_name]

### sudo
Change users and rights.
sudo su -> activate superuser
type 'exit' to exit

### timux
Manage several terminal windows.
tmux -> start a new session
In tmux, ctrl+b and then % -> vertical split
In tmux, ctrl+b and then " -> horizontal split
In tmux, ctrl+b and then c -> new window
In tmux, ctrl+b and then d -> return to classic shell (dettach)
tmux kill-session -t [session_id]
See https://gist.github.com/henrik/1967800
