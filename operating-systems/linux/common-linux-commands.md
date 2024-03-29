# Common Linux Commands

Linux commands are powerful tools used in the terminal to interact with the operating system and manage files, directories, processes, and more. Here's an overview of some commonly used commands:

## File and Directory Management

- `ls`: Lists the contents of a directory.
  - `ls -l`: Lists with detailed information.
  - `ls -a`: Includes hidden files.

- `cd <directory>`: Changes the current directory.
  - `cd ..`: Moves up one directory level.
  - `cd ~`: Goes to the home directory.

- `pwd`: Displays the current directory path.

- `mkdir <directory>`: Creates a new directory.

- `rmdir <directory>`: Deletes an empty directory.

- `rm <file>`: Removes a file.
  - `rm -r <directory>`: Recursively removes a directory and its contents.

- `cp <source> <destination>`: Copies files or directories.
  - `cp -r <source_directory> <destination_directory>`: Recursively copies a directory.

- `mv <source> <destination>`: Moves or renames files or directories.

## File Viewing and Manipulation

- `cat <file>`: Displays the content of a file.

- `less <file>`: Views the content of a file one page at a time.

- `head <file>`: Shows the first few lines of a file.
  - `head -n <number> <file>`: Specifies the number of lines to show.

- `tail <file>`: Displays the last few lines of a file.
  - `tail -n <number> <file>`: Specifies the number of lines to show.

- `grep '<pattern>' <file>`: Searches for a pattern in a file.

- `nano <file>`: Opens a file in the Nano text editor.
- `vi <file>`: Opens a file in the Vi text editor.

## System and Process Management

- `top`: Displays running processes and system resource usage.

- `ps`: Shows the current processes.
  - `ps aux`: Shows detailed information about all running processes.

- `kill <process_id>`: Terminates a process.

- `sudo <command>`: Executes a command with superuser privileges.

- `df`: Displays disk space usage.
  - `df -h`: Shows disk space in human-readable format.

- `du`: Shows the disk usage of a directory.
  - `du -sh <directory>`: Displays the total size of a directory.

## Networking

- `ping <host>`: Checks connectivity to a host.

- `ifconfig`: Displays network interface configurations (deprecated in many distros, replaced by `ip`).

- `ip a`: Shows IP addresses assigned to all network interfaces.

- `netstat`: Displays network connections, routing tables, and interface statistics.

- `curl <URL>`: Fetches content from a web page.

- `wget <URL>`: Downloads files from the internet.

This list covers only a fraction of the commands available in Linux, but these are among the most frequently used for daily tasks.
