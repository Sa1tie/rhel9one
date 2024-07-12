##############################################################################
# Objective: Log in and switch users in multiuser targets
##############################################################################

# Purpose:
Logging into and switching users on a Linux system is fundamental for system administration. 
It allows administrators to manage different user sessions and access levels efficiently.

# Details:
In multiuser targets, such as runlevels 3 (multi-user mode with networking) and 5 (graphical),
users can log in and switch between different accounts using various commands.

# Examples and Commands:

# Log in as a different user
$ su - username

# Switch to root user
$ su -

# Log in as root directly
$ sudo su -

# Switch to another user session
$ su - user2

# Use 'exit' to return to the previous user session
$ exit

# Use 'su' without '-' to switch users without resetting environment variables
$ su username

# Use 'sudo' to execute commands as another user (if configured in sudoers)
$ sudo -u username command

# Use Cases:
- An administrator needs to perform administrative tasks as root.
- Troubleshooting user-specific issues by accessing their session.
- Testing user-specific configurations and permissions.

# ELI5 (Explain Like I'm 5):
Think of logging in and switching users like playing with different toys. Each toy (user) has its own set of rules and things it can do. 
You can switch between toys to play with different o

