# ================================================
# Title / Objective: List, set, and change standard ugo/rwx permissions
# ================================================

# Purpose:
# This objective is crucial for managing file security and access in Linux. Understanding 
# and manipulating file permissions ensures that users have appropriate access while 
# protecting sensitive data from unauthorized access.

# Details:
# In Linux, every file and directory has an associated set of permissions that determines 
# who can read, write, or execute it. Permissions are divided into three categories:
# - User (u): The owner of the file.
# - Group (g): Users who are members of the file's group.
# - Others (o): All other users.
# Permissions are represented as:
# - r: read
# - w: write
# - x: execute
# The 'chmod' command is used to change file permissions, while 'ls -l' lists them.

# Examples and Commands:
# Listing permissions
ls -l filename
# Output: -rwxr-xr--
# -: file type
# rwx: user permissions (read, write, execute)
# r-x: group permissions (read, execute)
# r--: others permissions (read)

# Setting permissions using symbolic mode
chmod u=rwx,g=rx,o=r filename
# Explanation: User has read, write, and execute; Group has read and execute; Others have read.

# Setting permissions using numeric mode
chmod 755 filename
# Explanation: 7 (rwx for user), 5 (rx for group), 5 (rx for others)

# Changing ownership
chown user:group filename
# Explanation: Change the owner and group of the file.

# Use Cases:
# - Securing scripts: Ensure only the owner can modify a script.
chmod 700 script.sh
# - Shared directories: Allow a group to collaborate on files.
chmod 770 shared_dir

# ELI5 (Explain Like I'm 5):
# Imagine you have a box (a file) and you put a lock on it (permissions). 
# You have three keys (read, write, execute) for yourself, your friends (group), 
# and strangers (others). Setting permissions is like deciding who gets which keys.

# Practice Tips:
# - Use 'ls -l' frequently to check permissions.
# - Practice changing permissions in both symbolic and numeric modes.
# - Create different files and directories and try setting various permission scenarios.
# - Understand default permissions (umask) and how they apply to new files.
# - Remember to use 'sudo' for changing permissions/ownership of system files.

