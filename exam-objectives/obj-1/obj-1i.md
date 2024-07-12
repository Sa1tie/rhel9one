# Title / Objective: Create Hard and Soft Links

# Purpose:
# This objective focuses on understanding and creating hard and soft (symbolic) links in Linux.
# Links are essential for file management and efficient storage usage, enabling multiple
# references to a single file and creating shortcuts.

# Details:
# In Linux, there are two types of links: hard links and soft links (also known as symbolic links).
# - Hard links point directly to the inode of a file, making them indistinguishable from the original file.
# - Soft links are pointers to the path of the original file, acting as shortcuts and can span across filesystems.

# Examples and Commands:

# Creating a Hard Link:
# The ln command creates hard links.
# Syntax: ln <target_file> <link_name>
ln original.txt hardlink.txt

# Example: 
# Create a hard link named hardlink.txt to a file named original.txt.
# This means both hardlink.txt and original.txt point to the same data.
# Changes to one will reflect in the other.
ln original.txt hardlink.txt

# Listing Hard Links:
# Use the ls command with -l option to view hard links.
# Syntax: ls -l <file_name>
ls -l original.txt hardlink.txt

# Creating a Soft Link:
# The ln command with -s option creates soft links.
# Syntax: ln -s <target_file> <link_name>
ln -s original.txt softlink.txt

# Example: 
# Create a soft link named softlink.txt to a file named original.txt.
# This means softlink.txt is a pointer to original.txt, and deleting original.txt breaks the link.
ln -s original.txt softlink.txt

# Listing Soft Links:
# Use the ls command with -l option to view soft links.
# Syntax: ls -l <file_name>
ls -l original.txt softlink.txt

# Use Cases:
# Hard Links:
# - Efficiently manage storage by avoiding duplication of files.
# - Ensure data consistency by having multiple references to a single file.
# Soft Links:
# - Create shortcuts to files or directories.
# - Easily manage and navigate complex directory structures.
# - Link files across different filesystems.

# ELI5 (Explain Like I'm 5):
# Imagine you have a book (file). A hard link is like having multiple copies of the same book
# that are all kept in sync. A soft link is like having a bookmark (

