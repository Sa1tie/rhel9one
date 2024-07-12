# Objective: Set enforcing and permissive modes for SELinux

# Purpose:
# SELinux (Security-Enhanced Linux) provides mandatory access control (MAC) security policies. 
# Understanding how to set SELinux modes (enforcing and permissive) is crucial for managing security policies effectively.

# Details:
# - Enforcing mode: SELinux policies are actively enforced, and access violations are logged and denied.
# - Permissive mode: SELinux policies are not enforced, but violations are logged for analysis without denying access.

# Examples and Commands:
# Set SELinux to enforcing mode:
sudo setenforce 1

# Set SELinux to permissive mode:
sudo setenforce 0

# Check SELinux mode:
sudo sestatus

# Use Cases:
# Example 1: Setting SELinux to permissive mode temporarily to troubleshoot access issues without denying access.
# Example 2: Setting SELinux to enforcing mode after confirming policies are correctly configured to enforce security.

# ELI5 (Explain Like I'm 5):
# Imagine SELinux as a security guard for your computer. In enforcing mode, the guard checks everyone coming in and out, making sure they follow all the rules. In permissive mode, the guard still watches, but only takes notes on rule violations without stopping anyone.

# Practice Tips:
# - Practice switching between enforcing and permissive modes using `setenforce`.
# - Learn to interpret SELinux status using `sestatus`.
# - Create scenarios where you need to troubleshoot access issues and decide whether to set SELinux to permissive or enforcing mode.


