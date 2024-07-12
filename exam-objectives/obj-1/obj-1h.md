# Title / Objective: Create, delete, copy, and move files and directories

# Purpose:
# This objective covers the fundamental file management operations in Linux.
# It is crucial for maintaining an organized file system and performing everyday tasks
# as a system administrator.

# Details:
# In Linux, managing files and directories is essential for effective system administration.
# You need to be proficient in creating, deleting, copying, and moving files and directories
# to manage user data, system files, and backups efficiently.
#
# Key commands:
# - `touch`: Create an empty file
# - `mkdir`: Create a directory
# - `rm`: Remove files or directories
# - `cp`: Copy files or directories
# - `mv`: Move or rename files or directories

# Examples and Commands:
# Creating a file:
touch myfile.txt
# Creating multiple files:
touch file1.txt file2.txt file3.txt

# Creating a directory:
mkdir mydir
# Creating nested directories:
mkdir -p parentdir/childdir/grandchilddir

# Deleting a file:
rm myfile.txt
# Deleting multiple files:
rm file1.txt file2.txt
# Deleting a directory and its contents recursively:
rm -r mydir

# Copying a file:
cp source.txt destination.txt
# Copying a directory recursively:
cp -r sourcedir destinationdir

# Moving a file (or renaming):
mv oldname.txt newname.txt
# Moving a file to a different directory:
mv file.txt /path/to/destination/
# Moving a directory:
mv mydir /path/to/destination/

# Use Cases:
# 1. Organizing project files into directories for better structure.
# 2. Backing up important configuration files before making changes.
# 3. Cleaning up old or unnecessary files to free up disk space.
# 4. Renaming files to follow a consistent naming convention.

# ELI5 (Explain Like I'm 5):
# Imagine your computer is a big filing cabinet. Each file is a piece of paper,
# and each directory (or folder) is a drawer or a folder in the cabinet.
# You need to know how to add new papers (files), create new folders (directories),
# throw away papers you don't need (delete), make copies of papers (copy),
# and move papers from one folder to another (move).

# Practice Tips:
# 1. Create a practice directory and perform all the file and directory operations within it.
#    mkdir practice && cd practice
# 2. Experiment with different command options and see their effects.
# 3. Use `man` pages (e.g., `man cp`, `man mv`) to explore more options and understand command usage.
# 4. Practice with nested directories and multiple files to get comfortable with various scenarios.
# 5. Use the `-i` (interactive) option with `rm`, `cp`, and `mv` to prevent accidental deletions or overwrites.
#    rm -i myfile.txt
#    cp -i source.txt destination.txt
#    mv -i oldname.txt newname.txt

