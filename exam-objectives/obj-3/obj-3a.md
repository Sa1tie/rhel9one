##################################################
# Boot, reboot, and shut down a system normally #
##################################################

# Purpose:
# To understand and execute the commands necessary to start, restart, and shut down a Red Hat Enterprise Linux (RHEL) system properly.

# Details:
# Properly managing system startup and shutdown procedures is fundamental for maintaining system integrity, applying updates, and ensuring service availability. This objective covers the essential commands and practices for initiating these operations.

# Examples and Commands:
# To boot the system:
$ sudo systemctl start systemd-logind.service

# To reboot the system:
$ sudo systemctl reboot

# To shut down the system:
$ sudo systemctl poweroff

# Use Cases:
# - Restarting the system after applying updates or configuration changes.
# - Shutting down the system gracefully to prevent data loss or corruption.
# - Booting into different run levels or troubleshooting modes as needed.

# ELI5 (Explain Like I'm 5):
# Booting means turning on the computer to make it work. Rebooting is like pressing reset to fix problems. Shutting down is like turning it off nicely so nothing breaks.

# Practice Tips:
# - Practice these commands in a lab environment to become familiar with their usage.
# - Understand the difference between reboot and poweroff commands.
# - Learn to interpret system logs to troubleshoot startup or shutdown issues effectively.


