#####################################################################
# Objective: Configure IPv4 and IPv6 addresses
#####################################################################

# Purpose:
#   Configuring IPv4 and IPv6 addresses is essential for networking on
#   RHEL systems. It enables communication with other devices on the
#   network and internet using both IPv4 and IPv6 protocols.

# Details:
#   IPv4 addresses are the traditional numerical addresses (e.g., 192.168.1.1)
#   used to identify devices on a network. IPv6 addresses are longer and
#   hexadecimal (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334), offering
#   a larger address space.

# Examples and Commands:
#   To configure IPv4 address using `nmcli`:
nmcli connection modify eth0 ipv4.addresses 192.168.1.10/24
nmcli connection up eth0

#   To configure IPv6 address using `nmcli`:
nmcli connection modify eth0 ipv6.addresses "2001:db8::1234/64"
nmcli connection up eth0

#   To configure IPv4 address manually using `ip` command:
ip addr add 192.168.1.10/24 dev eth0
ip link set dev eth0 up

#   To configure IPv6 address manually using `ip` command:
ip addr add 2001:db8::1234/64 dev eth0
ip link set dev eth0 up

# Use Cases:
#   - Setting up a server with a static IP address.
#   - Configuring multiple IPv6 addresses for different services.
#   - Troubleshooting network connectivity by verifying correct IP settings.

# ELI5 (Explain Like I'm 5):
#   Imagine your computer needs a phone number to talk to other computers. IPv4
#   is like a short phone number, and IPv6 is like a longer phone number that
#   can handle more devices talking at once.

# Practice Tips:
#   - Practice configuring both IPv4 and IPv6 addresses using `nmcli` and `ip`.
#   - Experiment with different subnet masks and address ranges.
#   - Test connectivity between machines with configured addresses to ensure
#     communication works correctly.


