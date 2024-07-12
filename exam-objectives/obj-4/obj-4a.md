##############################
# RHCSA Exam Objective: Configure local storage
##############################

## Objective: List, create, delete partitions on MBR and GPT disks

### Purpose:
Understanding how to manage disk partitions is crucial for system administrators to effectively utilize storage resources, install operating systems, and manage data.

### Details:
Partitions divide a disk into separate areas that can be independently managed. Master Boot Record (MBR) and GUID Partition Table (GPT) are two different partitioning schemes commonly used on Linux systems.

### Examples and Commands:

#### List partitions on a disk (MBR or GPT):
$ sudo fdisk -l /dev/sda

#### Create a new partition using fdisk (MBR):
$ sudo fdisk /dev/sda
Command (m for help): n
Partition type:
   p   primary (0 primary, 0 extended, 4 free)
   e   extended (container for logical partitions)
Select (default p): p
Partition number (1-4, default 1): 1
First sector (2048-2097151, default 2048): 
Last sector, +sectors or +size{K,M,G,T,P} (2048-2097151, default 2097151): 
Command (m for help): w

#### Create a new partition using parted (GPT):
$ sudo parted /dev/sda
(parted) mkpart primary ext4 0% 50%
(parted) print
(parted) quit

#### Delete a partition:
$ sudo fdisk /dev/sda
Command (m for help): d
Partition number (1-4): 1
Command (m for help): w

### Use Cases:
1. **Installation:** Partitioning disks during OS installation to allocate space for root (/), /home, and swap partitions.
2. **Data Management:** Creating separate partitions for data storage to enhance performance and simplify backup processes.

### ELI5 (Explain Like I'm 5):
Partitioning is like dividing your toy box into different sections for Lego, dolls, and cars so you can find them easily when you want to play.

### Practice Tips:
- Practice partitioning both MBR and GPT disks using virtual machines or spare hardware.
- Familiarize yourself with commands like `fdisk`, `parted`, and `gdisk` for managing partitions.
- Understand the differences between MBR and GPT, including limitations and benefits of each.

##############################
# End of RHCSA Exam Objective
##############################

