# Basic command lines
Chosen linux commands and how to use them ! (not all options are listed)

### cat
To concatenate files or print files.
* cat [file]

### chmod
Change file or folder access rights.
* chmod g-w [file_name] -> remove write permission to group
* chmod u-wr [file_name] -> remove read and write permission to user

### chown
Change file owner.
* chown root [file_name] -> make root the owner of the file

### docker
Access a bash shell inside a docker container
* docker exec -it [container_name] bash

### grep
Filter folders, files or text based on a given set of characters.
* grep -n "[characters]" [file_name]
* grep -o "[pattern]" [path/to/file] | wc -l -> count occurences of a pattern in a file

### ln
Create a symlink.
* ln -s [target_file] [symlink_name]

### ls
List files and folder at given path.
* ls -l (one file one line view) -a (list all files, even hidden ones) [path/to/file-folder]

### mv
Move a file or a folder into a target folder.

mv [source_folder/file] [target_folder]

### nano
Command line text editor.

nano [file_name]

^X -> Exit

### netstat
Access server information: ports, processess, PID
netstat -laputen

### rm
Remove some specified files.
rm -f (force) -r (recursive) -v (verbose)

### scp
Exchange files between servers and computers.
* scp -i [key_path] [path/file_to_be_transfered] [path/file_destination]
* for instance, when connecting to AWS ubuntu instance : ubuntu@[server_public_DNS]:[path_in_server] 

### sed
(among others) remove first lines of a file
* sed -i [startIndex],[endIndex]d [file_name]

### sudo
Change users and rights.
* sudo su -> activate superuser
type 'exit' to exit

### ssh
Connect to another machine.
* ssh -i [path/key] [user_name]@[other_machine_DNS]
* ssh [server_name]

### tar
To create or decompress an archive.
* options:
  * c create
  * x decompress
  * f use a specified file
  * v verbose mode
  * z for Gzip archives
* tar xzfv [path/to/file] -> decompress a given archive in the current directory

### timux
Manage several terminal windows.
* tmux -> start a new session
  * In tmux, ctrl+b and then % -> vertical split
  * In tmux, ctrl+b and then " -> horizontal split
  * In tmux, ctrl+b and then c -> new window
  * In tmux, ctrl+b and then d -> return to classic shell (dettach)
* tmux kill-session -t [session_id]

See https://gist.github.com/henrik/1967800

### VBoxManage
Obviously, manage VirtualBox.
* VBoxManage list runningvms
* VBoxManage list vms
* VBoxManage controlvm \<name|uuid\> savestate -> gently power off vm (saving data)
* VBoxManage controlvm \<name|uuid\> poweroff -> not-gently power off

### vim
Use vim text editor.
* :q! -> exit without saving
* :wq -> write and quit
* :%s/\<pattern\>/&/gn -> count the number of occurences of \<pattern\> in the file
* :%s/\<word1\>.*\<word2\>/&/gn -> count the number of occurences for a pattern word1...(any sequence of characters)...word2, the order word1 word2 matters

## Configure new computer
- update

    sudo apt-get update && sudo apt-get upgrade

- git (required for oh my zsh)

    sudo apt-get install git

- zsh

    sudo apt-get install zsh

- oh-my-zsh

    sh -c "$(wget -O- https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

- vim

    sudo apt-get install vim
    
- tmux

    sudo apt-get install tmux

- docker [install doc ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/) and proceed with [postinstall](https://docs.docker.com/install/linux/linux-postinstall/)
- docker compose [install doc](https://docs.docker.com/compose/install/)
