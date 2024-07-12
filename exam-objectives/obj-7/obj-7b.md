# Objective: Configure Hostname Resolution

# Purpose:
# Hostname resolution is essential for mapping hostnames to IP addresses and vice versa. It ensures
# that networked devices can communicate with each other using meaningful names instead of just IP addresses.

# Details:
# Hostname resolution is managed by the system's DNS (Domain Name System) configuration. This involves
# configuring DNS servers, domain search lists, and local hostname resolution through /etc/hosts.

# Examples and Commands:
# Set the hostname permanently:
sudo hostnamectl set-hostname myhost.example.com

# Edit the /etc/hosts file to configure static hostname/IP mappings:
sudo nano /etc/hosts

# Example /etc/hosts file:
127.0.0.1   localhost
::1         localhost
192.168.1.10   myhost.example.com   myhost

# Use the `hostname` command to check the current hostname:
hostname

# Use `nslookup` or `dig` to query DNS servers for hostname resolution:
nslookup myhost.example.com
dig myhost.example.com

# Use `systemctl` to manage the systemd-resolved service for DNS resolution:
sudo systemctl start systemd-resolved
sudo systemctl enable systemd-resolved

# Use Cases:
# - Ensuring servers and clients can communicate using meaningful names.
# - Setting up local development environments without a DNS server.
# - Troubleshooting network connectivity by verifying hostname resolution.

# ELI5 (Explain Like I'm 5):
# Think of hostname resolution like a phonebook for computers. When you want to call a friend, you look up
# their name to get their phone number. Hostname resolution helps computers find each other on the network
# using names (like myhost.example.com) instead of just numbers (like IP addresses).

# Practice Tips:
# - Practice editing /etc/hosts to configure static hostname/IP mappings.
# - Experiment with different DNS lookup tools (`nslookup`, `dig`) to understand how they work.
# - Set up a lab environment to simulate DNS server configurations and troubleshoot hostname resolution issues.

