##########################################################
# Objective: Configure systems to boot into a specific target automatically
##########################################################

# Purpose:
# This objective ensures that the system boots into a desired target runlevel or systemd target automatically after reboot, ensuring the system starts with the required services and configurations.

# Details:
# In RHEL 9, system boot behavior is managed primarily through systemd targets. Targets replace the traditional runlevels (like runlevel 3 for multi-user mode and runlevel 5 for graphical mode) found in SysVinit systems. Setting the default target determines which systemd target the system boots into by default.

# Examples and Commands:
# Display current default target
systemctl get-default

# Set default target to multi-user.target (equivalent to runlevel 3)
sudo systemctl set-default multi-user.target

# Set default target to graphical.target (equivalent to runlevel 5)
sudo systemctl set-default graphical.target

# Use Cases:
# Example 1: Server without GUI
# Purpose: Configure a server to boot into multi-user mode (text-based console) by default.
sudo systemctl set-default multi-user.target

# Example 2: Workstation with GUI
# Purpose: Configure a workstation to boot into graphical mode by default.
sudo systemctl set-default graphical.target

# ELI5 (Explain Like I'm 5):
# Think of setting the default target like choosing what kind of clothes you wear every day. If you need to do a lot of work and don't need fancy stuff, you wear comfortable clothes (multi-user mode). If you're going out and need to look good (using a graphical interface), you wear something nice (graphical mode).

# Practice Tips:
# - Practice switching between different targets using systemctl commands.
# - Understand the differences between multi-user.target and graphical.target.
# - Learn how to troubleshoot boot issues related to incorrect default targets.

