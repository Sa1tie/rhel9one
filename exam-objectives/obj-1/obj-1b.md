#######################################
# RHCSA Exam Objective: Input-Output Redirection
#######################################

# Purpose:
# Input-output redirection is used to control where command output goes and where command input comes from.
# Understanding these operators is crucial for managing and manipulating command output efficiently.

# Details:
# - `>`: Redirects standard output (stdout) of a command to a file. If the file exists, it will be overwritten.
# - `>>`: Appends standard output (stdout) of a command to a file. If the file doesn't exist, it will be created.
# - `2>`: Redirects standard error (stderr) of a command to a file.
# - `2>&1`: Redirects standard error (stderr) to the same location as standard output (stdout).
# - `|`: Pipe operator redirects stdout of one command to stdin of another.

# Examples and Commands:
# Redirect stdout to a file:
echo "Hello, World!" > hello.txt

# Append stdout to a file:
echo "Goodbye, World!" >> hello.txt

# Redirect stderr to a file:
cat nonexistentfile 2> error.log

# Redirect stderr to stdout (combine both):
cat nonexistentfile 2>&1

# Pipe operator example:
ls -l | grep "file"

# Use Cases:
# - Logging: Redirect command output to log files.
# - Error Handling: Separate error messages from regular output for better troubleshooting.
# - Chaining Commands: Pass the output of one command as input to another using pipes.

# ELI5 (Explain Like I'm 5):
# Imagine you have a magic tube where things go in one end and come out the other. 
# These redirection symbols help you decide where things go when you use commands on a computer.

# Practice Tips:
# - Practice redirecting both stdout and stderr to files.
# - Use pipes to chain commands together and understand how data flows.
# - Experiment with different commands and redirections to get comfortable with the syntax.

# Remember:
# - `>` and `>>` for redirecting output to files.
# - `2>` and `2>&1` for handling errors.
# - `|` to connect multiple commands together.

