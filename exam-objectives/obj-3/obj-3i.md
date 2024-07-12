# Objective: Start, stop, and check the status of network services

# Purpose:
# Managing network services is crucial for ensuring network connectivity, security,
# and overall system functionality. This objective tests your ability to start,
# stop, and verify the status of network services on a Red Hat Enterprise Linux 9 system.

# Details:
# Network services include essential processes that handle network communication,
# such as web servers (httpd), DNS servers (named), SSH (sshd), and others.
# You need to be able to start these services when they're needed, stop them safely
# when necessary, and check if they are running to troubleshoot connectivity issues.

# Examples and Commands:
# Start a service:
sudo systemctl start <service_name>

# Stop a service:
sudo systemctl stop <service_name>

# Restart a service:
sudo systemctl restart <service_name>

# Check the status of a service:
sudo systemctl status <service_name>

# Enable a service to start on boot:
sudo systemctl enable <service_name>

# Disable a service from starting on boot:
sudo systemctl disable <service_name>

# Use Cases:
# Example 1: Starting and checking the status of the SSH service
sudo systemctl start sshd
sudo systemctl status sshd

# Example 2: Stopping and restarting the Apache HTTP server
sudo systemctl stop httpd
sudo systemctl restart httpd

# ELI5 (Explain Like I'm 5):
# Imagine your computer has little helpers that manage its ability to talk to other computers.
# Sometimes, you need to tell these helpers to start working, stop for a break, or check if they're
# doing their job properly. This is what you do with network services: start them when needed,
# stop them when not, and check they're working well.

# Practice Tips:
# 1. Practice starting, stopping, and checking the status of common network services like SSH, Apache HTTP Server.
# 2. Experiment with enabling and disabling services to start automatically on boot.
# 3. Use `systemctl` commands frequently in your practice sessions to become comfortable with their syntax and options.
# 4. Explore troubleshooting scenarios where knowing the status of network services is critical to resolving issues.
