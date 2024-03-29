# Common macOS Commands

macOS, being a UNIX-based operating system, shares many commands with Linux and other UNIX-like systems. The Terminal app in macOS provides access to the UNIX command line to perform various tasks. Here are some commonly used macOS Terminal commands:

## File and Directory Management

- `ls`: Lists the contents of a directory.
  - `ls -l`: Lists with detailed information.
  - `ls -a`: Shows all files, including hidden ones.

- `cd <directory>`: Changes the current directory.
  - `cd ~`: Goes to the home directory.
  - `cd /`: Goes to the root directory.

- `pwd`: Prints the current working directory path.

- `mkdir <directory>`: Creates a new directory.

- `rmdir <directory>`: Deletes an empty directory.

- `rm <file>`: Deletes a file.
  - `rm -r <directory>`: Deletes a directory and its contents.

- `cp <source> <destination>`: Copies files or directories.
  - `cp -R <source> <destination>`: Recursively copies directories.

- `mv <source> <destination>`: Moves or renames files or directories.

## File Viewing and Editing

- `cat <file>`: Displays the content of a file.

- `less <file>`: Views the content of a file page by page.

- `head <file>`: Shows the first 10 lines of a file.
  - `head -n <number> <file>`: Shows the first <number> lines.

- `tail <file>`: Displays the last 10 lines of a file.
  - `tail -n <number> <file>`: Shows the last <number> lines.

- `nano <file>`: Opens the Nano text editor.
- `vim <file>`: Opens the file in Vim, an advanced text editor.

## System and Process Management

- `top`: Displays ongoing processes and system resource usage.

- `ps`: Lists current processes.
  - `ps aux`: Provides a detailed list of all running processes.

- `kill <PID>`: Terminates a process with the specified PID (Process ID).

- `sudo <command>`: Executes a command with administrator privileges.

- `diskutil`: Manages disks and storage devices, similar to `fdisk` in Linux.

## Network Utilities

- `ping <hostname>`: Tests connectivity with the specified hostname or IP address.

- `ifconfig`: Displays network interface configurations. For newer macOS versions, `ifconfig` is being replaced by `ipconfig` and other commands.
  
- `curl <URL>`: Retrieves content from the web.

- `wget <URL>`: Downloads files from the web. `wget` may need to be installed using Homebrew (`brew install wget`).

- `ssh <username>@<hostname>`: Connects to a remote host via SSH.

- `scp <source> <destination>`: Securely copies files between hosts over SSH.

## Disk Usage and Management

- `df`: Shows disk space usage of file systems.
  - `df -h`: Displays disk space in a human-readable format.

- `du`: Estimates file space usage.
  - `du -sh <directory>`: Shows the total size of a directory.

## Software Management

- `brew install <package>`: Installs a package using Homebrew, macOS's package manager (Homebrew needs to be installed first).

These commands form the foundation of interacting with macOS through the Terminal, providing control over file management, system monitoring, network operations, and more.
