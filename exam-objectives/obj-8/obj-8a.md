# RHCSA Exam Objective: Manage users and groups
## Create, delete, and modify local user accounts

### Purpose:
Managing user accounts is essential for system security and access control. This objective ensures administrators can effectively create, modify, and remove user accounts as needed.

### Details:
User management involves tasks such as creating new accounts, adjusting account settings, and removing accounts that are no longer needed. These actions are crucial for maintaining system security and ensuring users have appropriate access privileges.

### Examples and Commands:
# Create a new user 'john' with default settings
sudo useradd john

# Set a password for the user 'john'
sudo passwd john

# Modify user 'john' to change their home directory
sudo usermod -d /home/newhome john

# Delete user 'john' and their home directory
sudo userdel -r john

### Use Cases:
- **Scenario 1:** Adding a new employee to the system.
  - Action: Create a new user account with appropriate permissions.
  
- **Scenario 2:** Revoking access for a contractor who has completed their project.
  - Action: Remove the user account and associated privileges.

### ELI5 (Explain Like I'm 5):
Managing users is like giving keys to different people for different rooms in a house. Sometimes, you need to make new keys, change where someone can go, or take keys away when someone doesn't need them anymore.

### Practice Tips:
- Practice creating, modifying, and deleting user accounts in a virtual machine environment.
- Explore different options and parameters available with commands like `useradd`, `usermod`, and `userdel`.
- Pay attention to user permissions and ensure that each action is performed securely and with appropriate access levels.


