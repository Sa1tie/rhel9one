##############################################
# Objective: Add new partitions and logical volumes, and swap to a system non-destructively
##############################################

# Purpose:
# This objective focuses on expanding storage capabilities on a RHEL 9 system without
# losing existing data. It involves adding new partitions, creating logical volumes,
# and configuring swap space to improve system performance and flexibility.

# Details:
# Adding new partitions allows you to allocate additional storage space from available
# disk resources. Logical volumes provide a flexible way to manage storage, enabling
# resizing and snapshot capabilities. Configuring swap space enhances system performance
# by providing extra memory resources when physical RAM is exhausted.

# Examples and Commands:

# 1. Add a new partition:
sudo fdisk /dev/sdb
# Create a new partition (e.g., /dev/sdb1) using the fdisk utility.
# Write changes and exit.

# 2. Create a physical volume (PV):
sudo pvcreate /dev/sdb1
# Initialize the new partition as a physical volume.

# 3. Extend volume group (VG):
sudo vgextend rhel /dev/sdb1
# Add the new physical volume to an existing volume group (e.g., 'rhel').

# 4. Create a logical volume (LV):
sudo lvcreate -n lv_storage -L 10G rhel
# Create a logical volume named 'lv_storage' of 10GB within the 'rhel' volume group.

# 5. Format the logical volume:
sudo mkfs.ext4 /dev/rhel/lv_storage
# Format the logical volume with the ext4 filesystem.

# 6. Configure swap space:
sudo lvcreate -L 4G -n lv_swap rhel
# Create a logical volume 'lv_swap' of 4GB within the 'rhel' volume group for swap.

sudo mkswap /dev/rhel/lv_swap
# Set up 'lv_swap' as swap space.

# 7. Activate the swap space:
sudo swapon /dev/rhel/lv_swap
# Enable the swap space for immediate use.

# Use Cases:
# - Adding storage for database servers without disrupting ongoing operations.
# - Scaling up virtual machine environments by dynamically allocating storage resources.
# - Enhancing system reliability by separating swap space from critical data partitions.

# ELI5 (Explain Like I'm 5):
# Imagine your computer is a toy box. Adding partitions is like getting a new section
# in the box for different types of toys. Swap space is like having extra storage
# boxes nearby where you can quickly put toys you're not playing with to make room
# for new ones.

# Practice Tips:
# - Practice using fdisk and lvcreate commands in a test environment.
# - Experiment with different sizes and configurations to understand their impacts.
# - Review how to monitor and manage logical volumes and swap space using commands like lvdisplay and swapon.

