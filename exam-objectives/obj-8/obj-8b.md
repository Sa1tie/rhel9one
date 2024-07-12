#####################################################
# Objective: Change passwords and adjust password aging for local user accounts
#####################################################

# Purpose:
# Managing user passwords and their aging policies is crucial for security and compliance with organizational policies. This objective ensures that administrators can enforce strong password practices and manage user access securely.

# Details:
# Password management involves changing user passwords, setting password expiration policies, and configuring aging parameters such as minimum and maximum password ages. These practices help in maintaining system security and adhering to regulatory requirements.

# Examples and Commands:
# Change password for a user:
$ sudo passwd <username>

# Set password expiration for a user (set maximum age to 90 days):
$ sudo chage -M 90 <username>

# View password aging information for a user:
$ sudo chage -l <username>

# Use Cases:
# Example 1: Ensuring regular password updates for user 'john' to comply with security policies.
# Example 2: Setting maximum password age for 'mary' to ensure passwords are regularly updated.

# ELI5 (Explain Like I'm 5):
# Changing passwords is like giving your computer a new secret code to keep it safe, and making sure it gets a new code regularly so bad guys can't figure it out.

# Practice Tips:
# - Practice changing passwords and checking password aging regularly.
# - Experiment with different settings for password expiration using `chage`.
# - Understand how to troubleshoot password-related issues, such as forgotten passwords or locked accounts.


