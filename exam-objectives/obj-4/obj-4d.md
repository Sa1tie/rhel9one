######################################################
# Objective: Create and delete logical volumes
######################################################

# Purpose:
# Logical volumes provide flexible and efficient management of storage in RHEL systems. They allow system administrators to dynamically allocate and resize storage as needed without disrupting services.

# Details:
# Logical volumes (LVs) are virtual block devices created from physical volumes (PVs). They can span across multiple physical disks and provide features like snapshots and resizable filesystems. Creating and deleting LVs involves configuring the LV size, filesystem type, and mount points.

# Examples and Commands:
# Create a logical volume named `lv_data` with a size of 2GB in volume group `vg_data`:
sudo lvcreate -n lv_data -L 2G vg_data

# Delete a logical volume `lv_data`:
sudo lvremove /dev/vg_data/lv_data

# Extend an existing logical volume `lv_data` to 4GB:
sudo lvextend -L +2G /dev/vg_data/lv_data

# Resize the filesystem on `lv_data` after extending:
sudo resize2fs /dev/vg_data/lv_data

# Use Cases:
# - Adding storage to a database server without downtime.
# - Resizing storage for virtual machines as their disk space requirements change.
# - Creating snapshots for backup purposes.

# ELI5 (Explain Like I'm 5):
# Think of logical volumes as customizable containers where you can put your files. You can make these containers bigger or smaller without having to take everything out and start over.

# Practice Tips:
# - Practice creating, resizing, and deleting logical volumes in a virtual environment.
# - Understand the relationship between physical volumes, volume groups, and logical volumes.
# - Familiarize yourself with the commands `lvcreate`, `lvremove`, `lvextend`, and `resize2fs` and their options.


