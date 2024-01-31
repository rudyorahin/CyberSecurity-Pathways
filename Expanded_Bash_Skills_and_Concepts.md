
# Bash Skills and Concepts

## Linux General

### Dashed Filename
- **Usage**: Dash (-) character at the end of a command typically refers to “stdin” or “stdout”. 
- **Example**: 
  - To remove a file named '-testfile': `$ rm -f -- -testfile`
  - To use Vim with stdin: `$ vim -- -`

### Spaces in Files
- **Usage**: In macOS, use a backslash (\) before each space in file names.
- **Example**: `$ cat spaces\ in\ the\ filename`

### Temporary Files
- **Usage**: `/tmp/filename123` is a temporary file, used for isolating actions from the rest of the system.
- **Example**: `$ touch /tmp/filename123` to create a temporary file.

### Piping and Redirection
- **Usage**: Piping (`|`) is used to pass the output of one command as input to another. Redirection (`>`, `>>`, `<`) is used to redirect input and output streams.
- **Example**: `$ echo "hello" | grep "h" > output.txt`

### Base64
- **Usage**: Base64 encoding is used to encode binary data into ASCII characters.
- **Example**: `$ echo 'Hello' | base64` to encode and `$ echo 'SGVsbG8=' | base64 --decode` to decode.

### Rot13
- **Usage**: Rot13 is a simple letter substitution cipher that replaces a letter with the 13th letter after it in the alphabet.
- **Example**: `$ echo 'Hello' | tr 'A-Za-z' 'N-ZA-Mn-za-m'` to encode and decode.

### Hex Dump
- **Usage**: Hex dump is used to view binary data in a human-readable hexadecimal format.
- **Example**: `$ echo 'Hello' | xxd` to create a hex dump.

### SSH/OpenSSH/Keys
- **Usage**: SSH is used for secure remote login. OpenSSH is an SSH protocol implementation. Keys are used for authentication.
- **Example**: `$ ssh-keygen` to generate a new SSH key pair.

### IP Addresses
- **Usage**: IP addresses uniquely identify each device on a network.
- **Example**: `$ ifconfig` or `$ ip addr show` to view your machine's IP address.

### Localhost
- **Usage**: Localhost refers to the local computer running a network service.
- **Example**: Accessing a locally hosted website via `http://localhost`.

### Ports and Port Scanner
- **Usage**: Ports are virtual points where network connections start and end. Port scanners are used to identify open ports on a host.
- **Example**: Using a tool like Nmap to scan for open ports: `$ nmap localhost`.

### Secure Socket Layer/Transport Layer Security
- **Usage**: SSL/TLS are protocols for securing internet connections.
- **Example**: Visiting a website with `https` in the URL uses TLS.

### OpenSSL Cookbook & Testing with OpenSSL
- **Usage**: OpenSSL is a toolkit for SSL/TLS. The OpenSSL Cookbook is a guide to using OpenSSL.
- **Example**: `$ openssl version` to check the installed version.

### Setuid
- **Usage**: Setuid is a Unix permission that allows users to run an executable with the permissions of the executable's owner.
- **Example**: `$ chmod u+s filename` to set the setuid bit on a file.

### Unix 'Job Control'
- **Usage**: Commands like `bg`, `fg`, `jobs`, `&`, `CTRL-Z`, etc., are used for controlling processes in Unix.
- **Example**: `$ sleep 100 &` to run a process in the background.

## How the Internet Works

### The Client-Server Model
... [Content continues as before] ...
