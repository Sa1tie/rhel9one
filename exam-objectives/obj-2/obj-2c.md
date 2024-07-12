# Title / Objective: Process script inputs ($1, $2, etc.)
#
# Purpose:
# The purpose of this objective is to understand how to handle and process 
# positional parameters in shell scripts. Positional parameters allow scripts 
# to accept input values and use them to perform various tasks, making scripts 
# more flexible and dynamic.
#
# Details:
# In shell scripting, positional parameters are used to pass arguments to a script. 
# These arguments are accessed using the special variables $1, $2, $3, etc., where 
# $1 is the first argument, $2 is the second, and so on. The variable $0 contains 
# the name of the script itself. By using positional parameters, scripts can be 
# designed to take different actions based on the inputs provided.
#
# Examples and Commands:
# Here is a basic example of a script that takes two arguments and prints them:
#
# Example script: print_args.sh
# ---------------------------------
# #!/bin/bash
# 
# # Check if at least two arguments are provided
# if [ $# -lt 2 ]; then
#   echo "Usage: $0 <arg1> <arg2>"
#   exit 1
# fi
# 
# # Print the arguments
# echo "First argument: $1"
# echo "Second argument: $2"
# ---------------------------------
#
# To run this script:
# $ chmod +x print_args.sh
# $ ./print_args.sh hello world
# Output:
# First argument: hello
# Second argument: world
#
# Use Cases:
# 1. Automation scripts that need to perform tasks based on user input.
# 2. Scripts that process files provided as arguments.
# 3. Command-line utilities that require multiple options.
#
# Example Use Case: Renaming Files
# ---------------------------------
# #!/bin/bash
# 
# if [ $# -ne 2 ]; then
#   echo "Usage: $0 <source_filename> <destination_filename>"
#   exit 1
# fi
# 
# mv $1 $2
# echo "File renamed from $1 to $2"
# ---------------------------------
#
# To run this script:
# $ chmod +x rename_file.sh
# $ ./rename_file.sh oldname.txt newname.txt
#
# ELI5 (Explain Like I'm 5):
# Think of a shell script as a recipe. The ingredients (inputs) are given 
# when you start the recipe. $1, $2, $3, etc., are like labels on the bowls 
# that hold each ingredient. The script uses these labels to know which 
# ingredient to use at each step of the recipe.
#
# Practice Tips:
# 1. Create simple scripts that take multiple arguments and perform different 
#    actions based on these arguments.
# 2. Experiment with different numbers of arguments and use conditional 
#    statements to handle varying input scenarios.
# 3. Use `shift` to iterate over all provided arguments in a script.
# 4. Check the value of special variables like $#, $*, and $@ to understand 
#    how they change with different inputs.
#
# Example Practice Script: list_args.sh
# ---------------------------------
# #!/bin/bash
# 
# echo "Total number of arguments: $#"
# echo "All arguments as a single string: $*"
# echo "All arguments as separate strings: $@"
# 
# count=1
# for arg in "$@"; do
#   echo "Argument $count: $arg"
#   count=$((count + 1))
# done
# ---------------------------------
#
# Run and experiment with this script to understand how different input 
# arguments are handled.
#
# To run this script:
# $ chmod +x list_args.sh
# $ ./list_args.sh one two three
# Output:
# Total number of arguments: 3
# All arguments as a single string: one two three
# All arguments as separate strings: one two three
# Argument 1: one
# Argument 2: two
# Argument 3: three

