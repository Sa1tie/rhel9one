#######################################
# Boot systems into different targets manually
#######################################

# Purpose:
# This objective tests your ability to manage systemd targets manually, allowing you to understand how to control the boot behavior and system state.

# Details:
# Systemd targets are units that group services and other units together based on similar functionality. Targets define the system state, such as multi-user, graphical interface, or rescue mode. Understanding how to switch between these targets manually is crucial for system administrators to troubleshoot and manage system resources effectively.

# Examples and Commands:
# To manually switch between systemd targets, use the `systemctl` command. Here are some common examples:

# View current target
systemctl get-default

# List available targets
systemctl list-units --type=target

# Change default target (runlevel)
sudo systemctl set-default graphical.target

# Switch to a different target for the current session
sudo systemctl isolate multi-user.target

# Use Cases:
# Example 1: Switching to rescue.target to troubleshoot and recover from system failures.
# Example 2: Setting default.target to multi-user.target for servers to boot into CLI mode instead of graphical mode for resource efficiency.

# ELI5 (Explain Like I'm 5):
# Think of systemd targets like different modes your computer can start in. You can choose to start with lots of windows (graphical mode) or just a black screen with words (CLI mode) depending on what you need to do.

# Practice Tips:
# - Practice switching between different targets using both `isolate` and `set-default` commands.
# - Understand the differences between graphical.target, multi-user.target, and other commonly used targets.
# - Explore how each target affects system services and performance to better manage system resources.


