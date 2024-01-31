
# Bash Scripting – Linux Shell Script

## Introduction to Bash Scripting
Bash scripts are files containing a series of commands executed by the bash program. They are essential for process automation in Linux, allowing multiple commands to be executed together. Different types of shells include Bash, Korn (ksh), C (csh), and Z (zsh).

### Bash Shell Usage
- **Prompt Indicators**: `$` for regular users, `#` for root users.
- **Commands Examples**:
  - `ps` to display the type of shell.
  - `date` to display the current date.
  - `read variable` to read input into a variable.

### Reading from a File
```bash
while read line
do
  echo $line
done < file.txt
```

### File Handling and Echo Command
- Creating files with `touch`.
- Searching with `grep`.
- Displaying disk space with `df`.
- Reviewing history with `history`.
- Checking processes with `ps`.

### Script File Extensions
- Use `.sh` or no extension.
- Shebang line `#!/bin/bash` is necessary at the start of each script.

### Running Scripts
- Make script executable: `chmod u+x script.sh`.
- Execute script: `sh script.sh`, `bash script.sh`, or `./script.sh`.

### Comments and Variables
- Use `#` for comments.
- No strict data types in Bash.
- Accessing variables: `echo $variable`.
- Positional parameters: `$1` for the first argument, `$2` for the second, etc.

### Conditional Statements
Example of an if-else statement in bash:
```bash
if [ $num -gt 0 -a $num -lt 100 ]; then
  echo "positive"
elif [ $num -lt 0 -o $num -eq 0 ]; then
  echo "negative"
else
  echo "zero"
fi
```

### Looping Constructs
- **While Loop**:
  ```bash
  while [[ $i -le 10 ]]; do
    echo "$i"
    (( i += 1 ))
  done
  ```
- **For Loop**:
  ```bash
  for i in {1..5}
  do
    echo $i
  done
  ```

### Case Statement
Example of a case statement:
```bash
case $fruit in
  "apple")
    echo "red"
    ;;
  "banana")
    echo "yellow"
    ;;
  *)
    echo "unknown"
    ;;
esac
```

## Scheduling Scripts with Cron
Cron is a job scheduling utility in Unix-like systems. It allows setting up automated jobs on a specified schedule.

### Cron Syntax
- `M H D M W command`
- Examples:
  - `0 0 * * * /path/to/script.sh` for daily at midnight.
  - `*/5 * * * * /path/to/script.sh` every 5 minutes.
  - `0 6 * * 1-5 /path/to/script.sh` weekdays at 6 am.

### Crontab Usage
- `crontab -l` to list scheduled scripts.
- `crontab -e` to edit cron jobs.

## Debugging and Troubleshooting
- `set -x` for debugging mode.
- `set -e` to exit on command failure.
- Check exit code with `$?`.
- Use `echo` for variable values.
- Troubleshoot crons using `/var/log/syslog` (Ubuntu).

## Additional Notes
- This document covers the basics of bash scripting and its application in automating tasks and managing Linux systems.
