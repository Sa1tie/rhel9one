# Title / Objective: Conditionally execute code (use of: if, test, [], etc.)

# Purpose:
# This objective focuses on understanding how to conditionally execute commands
# in a shell script. Conditional execution allows you to make decisions in 
# your scripts, enabling more dynamic and versatile operations.

# Details:
# Conditional execution is a fundamental aspect of scripting in Linux. 
# It allows you to execute certain parts of code based on whether specific 
# conditions are met. This is achieved using constructs like 'if', 'test', 
# and square brackets '[]'.
#
# The 'if' statement evaluates a condition and executes the associated block
# of code if the condition is true. The 'test' command and '[]' are used to 
# evaluate conditions such as file attributes, string comparisons, and 
# arithmetic operations.

# Examples and Commands:

# Example 1: Basic if statement
if [ condition ]; then
    # code to execute if condition is true
fi

# Example 2: if-else statement
if [ condition ]; then
    # code to execute if condition is true
else
    # code to execute if condition is false
fi

# Example 3: if-elif-else statement
if [ condition1 ]; then
    # code to execute if condition1 is true
elif [ condition2 ]; then
    # code to execute if condition2 is true
else
    # code to execute if none of the above conditions are true
fi

# Example 4: Using 'test' command
if test condition; then
    # code to execute if condition is true
fi

# Use Cases:

# Use Case 1: Checking if a file exists
FILE="/path/to/file"
if [ -f "$FILE" ]; then
    echo "File $FILE exists."
else
    echo "File $FILE does not exist."
fi

# Use Case 2: Comparing numbers
NUM1=5
NUM2=10
if [ "$NUM1" -lt "$NUM2" ]; then
    echo "$NUM1 is less than $NUM2"
else
    echo "$NUM1 is not less than $NUM2"
fi

# Use Case 3: String comparison
STR1="hello"
STR2="world"
if [ "$STR1" = "$STR2" ]; then
    echo "Strings are equal"
else
    echo "Strings are not equal"
fi

# ELI5 (Explain Like I'm 5):
# Imagine you want to decide what to wear based on the weather. 
# You look outside and see if it is raining. If it is raining, you wear a raincoat.
# If it is not raining, you wear a t-shirt. In scripting, we use 'if' to make such 
# decisions. If a condition is true (raining), we do one thing (wear a raincoat). 
# If it is false (not raining), we do something else (wear a t-shirt).

# Practice Tips:
# 1. Write simple scripts to practice the syntax of 'if', 'test', and '[]'.
# 2. Experiment with different conditions like file checks, string comparisons, 
#    and arithmetic operations.
# 3. Combine conditional statements with loops to create more complex scripts.
# 4. Practice debugging your scripts by adding 'echo' statements to print 
#    the values of variables and the flow of execution.
# 5. Use online resources and forums to find additional examples and explanations.
# 6. Set up small projects or tasks to automate using conditional statements, 
#    such as a script that checks system health or backups files based on 
#    certain conditions.

# End of File

