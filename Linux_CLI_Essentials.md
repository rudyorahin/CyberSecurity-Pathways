
# Linux Command Line Interface (CLI) Essentials

## SSH (Secure SHell)
- **Description**: SSH is a protocol for securely accessing one computer from another. It allows you to run command line and graphical programs, transfer files, and even create secure virtual private networks over the Internet.
- **Usage**:
  - **Connect**: `$ ssh <username>@<remote-address> (-p <port>)`
  - **Copy file to remote**: `$ scp /local/path/file.txt <username>@<remote>:/remote/path`
  - **Copy file from remote**: `$ scp <username>@<remote>:/remote/path/file.txt /local/path`
- **SSH Keys**:
  - **Generate keys**: `$ ssh-keygen -t rsa`
  - **Set permissions for private key**: `$ chmod 600 ~/.ssh/id_rsa`
  - **Copy public key to remote server**: `$ scp ~/.ssh/id_rsa.pub <username>@<remote>:`
  - **Install public key on remote server**:
    - `$ mkdir .ssh`
    - `$ cat id_rsa.pub >> .ssh/authorized_keys`
    - `$ chmod 700 .ssh`
  - **Connect with key**: `$ ssh -i ~/.ssh/id_rsa <username>@<remote>`

## Basic Linux Commands
- **ls**: List directory contents.
- **cd**: Change the current directory.
- **cat**: Concatenate and display file content.
- **grep**: Search text using patterns.
- **pwd**: Print the current working directory.
- **cp**: Copy files and directories.
  - `$ cp source.txt destination.txt`
- **mv**: Move or rename files and directories.
  - `$ mv old_name.txt new_name.txt`
- **rm**: Remove files or directories.
  - `$ rm file.txt`
- **chmod**: Change file mode bits.
  - `$ chmod 755 script.sh`
- **mkdir**: Create new directories.
  - `$ mkdir new_directory`
- **man**: Display manual pages for commands.
  - `$ man ls`
- **file**: Determine file type.
  - `$ file script.sh`
- **du**: Estimate file space usage.
  - `$ du file.txt`
- **find**: Search for files in a directory hierarchy.
  - `$ find . -name "file.txt"`
- **sort**: Sort lines of text files.
- **uniq**: Report or omit repeated lines.
- **strings**: Print the strings of printable characters in files.
- **diff**: Compare files line by line.
- **sh**: Execute commands from a file.
- **reset**: Reset terminal when it gets into an undesirable state.
- **base64**: Encode and decode data in base64 format.
- **xxd**: Create a hex dump or reverse a hex dump.
  - `$ xxd -r data.txt > data.bin`
- **gunzip**: Decompress files compressed by gzip.
- **bunzip2**: Decompress files compressed by bzip2.
- **tr**: Translate or delete characters.
- **tar**: Archive files into a tar file or extract them.
- **s_client**: OpenSSL tool for connecting to SSL/TLS servers.
- **nmap**: Network exploration tool and security scanner.
- **nslookup**: Query Internet domain name servers.
- **hostname**: Show or set the system's host name.
- **whois**: Query information about a domain name.
- **nc (netcat)**: Networking utility for reading from and writing to network connections.
- **telnet**: Interact with remote servers or local services on specific ports.
- **bash**: Command language interpreter.
- **screen**: Full-screen window manager.
- **tmux**: Terminal multiplexer.
- **cron**: Time-based job scheduler.
- **crontab**: Manage cron jobs.
- **vim**: Text editor.
- **git**: Version control system.

## Additional Resources
- For detailed usage and examples of each command, refer to the Linux manual pages or online tutorials.
