##########################
# Objective: SELinux File and Process Context
##########################

# Purpose:
# SELinux (Security-Enhanced Linux) enforces mandatory access control policies, enhancing system security by controlling access based on policies defined by file and process contexts.

# Details:
# Each file and process in SELinux is labeled with a context that includes security-relevant information such as user, role, type, and optionally, sensitivity level. Understanding and managing these contexts is crucial for configuring SELinux policies and troubleshooting access issues.

# Examples and Commands:
# Display SELinux context of files and processes:
ls -Z             # List files with their SELinux context
ps -eZ            # Show processes and their SELinux context

# Change SELinux context of a file:
chcon -t httpd_sys_content_t /var/www/html/index.html   # Change context type for Apache web server content

# Use semanage to manage SELinux policy:
semanage fcontext -l                   # List file context mappings
semanage user -l                       # List SELinux user mappings
semanage login -l                      # List SELinux login mappings

# Use Cases:
# - Setting file contexts for directories used by web servers to serve content.
# - Troubleshooting permission denied errors by checking SELinux contexts.
# - Customizing SELinux policies to meet specific security requirements for applications.

# ELI5 (Explain Like I'm 5):
# SELinux uses special tags on files and programs to keep them safe. It's like putting different colored tags on toys so only certain kids can play with them.

# Practice Tips:
# - Practice listing SELinux contexts regularly with ls -Z and ps -eZ.
# - Experiment with changing contexts using chcon and managing policies with semanage.
# - Understand common use cases where SELinux context management is critical, such as web server configurations and user home directories.


