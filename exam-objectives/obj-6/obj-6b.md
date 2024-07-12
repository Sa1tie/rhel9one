[200~###############################################################
# Objective: Start and stop services and configure services to start automatically at boot
###############################################################

# Purpose:
# Managing services is crucial for maintaining system functionality and ensuring
# essential processes are running. Configuring services to start automatically
# at boot time ensures continuity and reliability of system operations.

# Details:
# In Linux, services are managed using systemd, the system and service manager.
# System administrators can start, stop, enable (start at boot), disable (stop at boot),
# and check the status of services using systemctl command.

# Examples and Commands:

# Start a service immediately
sudo systemctl start <service_name>

# Stop a service immediately
sudo systemctl stop <service_name>

# Restart a service
sudo systemctl restart <service_name>

# Enable a service to start on boot
sudo systemctl enable <service_name>

# Disable a service from starting on boot
sudo systemctl disable <service_name>

# Check status of a service
sudo systemctl status <service_name>

# Use Cases:
# Example 1: Starting and Stopping Apache HTTP Server
# Apache service management:
sudo systemctl start httpd
sudo systemctl stop httpd
sudo systemctl enable httpd    # Enable Apache to start on boot
sudo systemctl disable httpd   # Disable Apache from starting on boot
sudo systemctl status httpd    # Check status of Apache service

# Example 2: Managing SSH Service
# SSH service management:
sudo systemctl start sshd
sudo systemctl stop sshd
sudo systemctl enable sshd     # Enable SSH to start on boot
sudo systemctl disable sshd    # Disable SSH from starting on boot
sudo systemctl status sshd     # Check status of SSH service

# ELI5 (Explain Like I'm 5):
# Imagine services are like toys in your room. You can start playing (start),
# stop playing (stop), and decide if you want to keep a toy ready for the next day (enable at boot)
# or put it away (disable at boot).

# Practice Tips:
# - Practice starting, stopping, enabling, disabling, and checking status of various services.
# - Understand the dependencies and relationships between services.
# - Experiment with different scenarios to reinforce your understanding.


