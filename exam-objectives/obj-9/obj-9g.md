###########################################################
# Manage SELinux Port Labels
###########################################################

# Title / Objective:
## Manage SELinux port labels

# Purpose:
SELinux port labels help manage network ports and services on RHEL systems, enhancing security by controlling access based on port contexts.

# Details:
SELinux uses port labels to define permissions for network services. Ports are categorized into different types (e.g., tcp, udp) and labeled accordingly in SELinux policy. This ensures that network communication adheres to security policies even if the firewall allows access.

# Examples and Commands:
# Display SELinux port types and labels
semanage port -l

# Add a new port label (e.g., TCP port 8080)
semanage port -a -t http_port_t -p tcp 8080

# Remove an existing port label (e.g., UDP port 123)
semanage port -d -p udp 123

# Use restorecon to apply context changes
restorecon -R -v /path/to/directory_or_file

# Use semanage to add or modify port labels
semanage port -a -t http_port_t -p tcp 8080

# Use Cases:
# Example: Allow Apache to use non-standard HTTP ports
semanage port -a -t http_port_t -p tcp 8080

# Example: Restrict access to specific UDP ports
semanage port -d -p udp 123

# ELI5 (Explain Like I'm 5):
SELinux port labels are like name tags for doors in a house. Each tag tells who can use the door and how. SELinux makes sure only the right people (or programs) can use each door (or port) in your computer.

# Practice Tips:
- Practice adding and removing port labels using `semanage`.
- Understand how SELinux interacts with firewall settings.
- Experiment with different port types (tcp, udp) and services (http, ssh) to see how SELinux affects access.

###########################################################

