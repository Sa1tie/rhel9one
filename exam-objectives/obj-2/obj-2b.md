# Title / Objective: Use Looping Constructs (for, etc.) to Process File, Command Line Input

# Purpose:
# The purpose of this objective is to understand how to use looping constructs,
# such as 'for' loops, to automate repetitive tasks, process multiple files,
# and handle command line inputs efficiently. Mastering loops is essential for
# effective system administration and scripting.

# Details:
# Looping constructs allow you to execute a block of code multiple times.
# In shell scripting, the 'for' loop is commonly used to iterate over a list of items,
# such as files, command line arguments, or output from a command. This helps automate
# tasks like batch processing of files, repetitive system checks, and data manipulation.

# Examples and Commands:
# 1. Basic 'for' loop to print numbers 1 to 5:
for i in {1..5}; do
    echo "Number: $i"
done

# 2. Loop through command line arguments:
for arg in "$@"; do
    echo "Argument: $arg"
done

# 3. Loop through files in a directory and display their names:
for file in /path/to/directory/*; do
    echo "File: $file"
done

# 4. Loop through the output of a command:
for user in $(cut -d: -f1 /etc/passwd); do
    echo "User: $user"
done

# Use Cases:
# 1. Batch Renaming Files:
# Rename all .txt files to .bak in a directory.
for file in *.txt; do
    mv "$file" "${file%.txt}.bak"
done

# 2. Monitoring System Usage:
# Check disk usage for multiple directories.
for dir in /home /var /usr; do
    du -sh "$dir"
done

# 3. Processing Command Line Arguments:
# Create directories from a list of names passed as arguments.
for dir in "$@"; do
    mkdir -p "$dir"
done

# ELI5 (Explain Like I'm 5):
# A 'for' loop is like a game where you go through a list of your toys one by one,
# and do something with each toy. For example, if you have five toy cars, you can
# pick each car up and put it in a toy box, one after the other.

# Practice Tips:
# 1. Write simple 'for' loops to print elements of a list.
# 2. Experiment with different ways to generate lists, like brace expansion ({1..10}),
#    command substitution ($(command)), and globbing (/path/to/files/*).
# 3. Combine 'for' loops with conditionals (if statements) to perform more complex tasks.
# 4. Practice processing files and command line arguments with 'for' loops.
# 5. Test your scripts in a safe environment to avoid unintended changes to important files.

# Example Practice Exercise:
# Write a script that takes a list of filenames as arguments and appends the current
# date to each filename.
# Example solution:
for file in "$@"; do
    mv "$file" "${file}_$(date +%Y%m%d)"
done

