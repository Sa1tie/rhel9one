##################################################
# Configure systems to mount file systems at boot by universally unique ID (UUID) or label
##################################################

# Purpose:
# This objective ensures that file systems can be reliably mounted at boot time using unique identifiers (UUIDs) or labels instead of device names, which can change.

# Details:
# Mounting file systems by UUID or label helps ensure consistency and reliability in system boot processes. UUIDs and labels are static identifiers associated with each file system, unlike device names (e.g., /dev/sda1) that may vary if hardware configurations change.

# Examples and Commands:
# To configure mounting by UUID, edit the /etc/fstab file and use the UUID instead of the device name.

# Example of an /etc/fstab entry using UUID:
UUID=12345678-9abc-def0-1234-56789abcdef0 /mnt/data ext4 defaults 0 0

# Example of an /etc/fstab entry using a label:
LABEL=mydata /mnt/data ext4 defaults 0 0

# Use Cases:
# - When migrating storage devices, ensuring that file systems mount correctly without manual intervention.
# - In environments where hardware configurations are dynamic, ensuring consistent file system mounting regardless of device names.

# ELI5 (Explain Like I'm 5):
# Think of UUIDs or labels as special names for each drawer (file system) in a cabinet (storage device). Even if you move the drawers around or change the cabinet, you can still find each drawer easily because of its special name.

# Practice Tips:
# - Practice editing /etc/fstab to use UUIDs and labels instead of device names.
# - Simulate hardware changes in virtual environments to see how UUIDs and labels maintain consistency during system boots.

