##############################################################################
# Objective: Use boolean settings to modify system SELinux settings
##############################################################################

# Purpose:
# SELinux (Security-Enhanced Linux) enforces mandatory access control policies
# to restrict user and process access to system resources. Booleans are
# settings that can enable or disable specific SELinux policies.

# Details:
# Booleans in SELinux allow administrators to customize the security policy
# without disabling SELinux entirely. They control various aspects of system
# behavior such as network connectivity, file access, and application execution.

# Examples and Commands:
# Enable or disable a SELinux boolean using the `setsebool` command.

# Display a list of available booleans:
$ sudo semanage boolean -l

# View the status of a specific boolean:
$ sudo semanage boolean -l | grep httpd_can_network_connect

# Enable a boolean:
$ sudo setsebool -P httpd_can_network_connect on

# Disable a boolean:
$ sudo setsebool -P httpd_can_network_connect off

# Use Cases:
# Example: Enabling Apache HTTP Server to make network connections:
# - Use `httpd_can_network_connect` boolean to allow Apache to connect to
#   remote servers for backend operations.

# ELI5 (Explain Like I'm 5):
# Think of SELinux booleans like switches that control which activities
# your applications can do. If you want a program to talk to the internet
# or access specific files, you flip the switch on (enable) or off (disable).

# Practice Tips:
# - Practice enabling and disabling common SELinux booleans related to services
#   you manage (e.g., httpd, ftp).
# - Understand the impact of each boolean on system behavior and security.
# - Familiarize yourself with viewing current boolean settings and their
#   descriptions using `semanage boolean -l`.

##############################################################################

