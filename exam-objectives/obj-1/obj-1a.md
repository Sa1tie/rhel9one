##########################
# Objective: Access a shell prompt and issue commands with correct syntax
##########################

# Purpose:
# This objective ensures that you can effectively use the command line interface (CLI) in RHEL9 to manage and interact with the operating system. It's fundamental for system administrators to navigate, execute commands, and troubleshoot issues efficiently.

# Details:
# Accessing a shell prompt allows administrators to interact directly with the system, execute commands, manage files, configure settings, and diagnose problems. Understanding correct syntax ensures commands are executed properly without errors.

# Examples and Commands:
# Displaying the shell prompt and issuing basic commands.

# Displaying the current shell prompt:
$ echo $PS1
[\u@\h \W]\$

# Listing files in the current directory:
$ ls
file1.txt  file2.txt  directory/

# Checking system uptime:
$ uptime

# Use Cases:
# - Checking system status and resource usage.
# - Managing files and directories, such as creating, copying, moving, and deleting.
# - Configuring system settings through command line utilities.
# - Troubleshooting system issues and errors.

# ELI5 (Explain Like I'm 5):
# Imagine the shell prompt as your magic wand to talk to the computer. You type commands like "show me my files" or "tell me how long you've been awake," and the computer answers back.

# Practice Tips:
# - Practice navigating directories using `cd` and listing files with `ls`.
# - Experiment with basic commands like `echo`, `cat`, `pwd`, and `whoami`.
# - Learn to use command options (e.g., `ls -l` for detailed file listing).
# - Familiarize yourself with redirection and piping commands for more advanced operations.

# End of Objective

