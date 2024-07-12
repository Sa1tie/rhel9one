##############################################################
# Objective: Restrict network access using firewall-cmd/firewall
##############################################################

# Purpose:
# This objective focuses on using firewall-cmd/firewall to manage firewall rules
# in Red Hat Enterprise Linux (RHEL) systems. It's essential for securing
# network access and controlling which services and ports are accessible
# from various network zones.

# Details:
# The firewall-cmd utility is used to manage firewall rules dynamically in RHEL.
# It provides a command-line interface to configure and query the firewall
# rules for IPv4 and IPv6 networks. Understanding how to add, remove, and
# list rules using firewall-cmd is crucial for securing network communication
# on RHEL systems.

# Examples and Commands:

# Enable the firewall and reload settings:
sudo systemctl start firewalld
sudo systemctl enable firewalld
sudo firewall-cmd --reload

# Check the current default zone:
sudo firewall-cmd --get-default-zone

# List all zones:
sudo firewall-cmd --get-zones

# List all services available in the default zone:
sudo firewall-cmd --list-services

# Allow SSH (port 22) in the default zone:
sudo firewall-cmd --zone=public --add-service=ssh --permanent

# Reload firewall settings to apply changes:
sudo firewall-cmd --reload

# Remove HTTP (port 80) from allowed services:
sudo firewall-cmd --zone=public --remove-service=http --permanent

# List all rules in the public zone:
sudo firewall-cmd --zone=public --list-all

# Use Cases:
# - Restricting access to services like SSH or HTTP based on network zones.
# - Defining custom rules to allow specific traffic while blocking others.
# - Securing servers by limiting access to specific ports from certain IP ranges.

# ELI5 (Explain Like I'm 5):
# Think of firewall-cmd as a gatekeeper for your computer. It decides which
# doors (ports) can be open to allow friends (services) to come in and which
# doors stay closed to keep strangers (unwanted traffic) out.

# Practice Tips:
# - Practice adding and removing different services from firewall zones.
# - Experiment with creating custom rules to allow or block specific ports.
# - Understand the difference between --add-service and --add-port options
#   in firewall-cmd for managing services and ports, respectively.
# - Simulate scenarios where you need to restrict access from certain IPs
#   while allowing access from others using firewall-cmd rules.


