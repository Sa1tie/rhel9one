##############################################################
# RHCSA Exam Objective: Preserve system journals
##############################################################

# Purpose:
# System journals contain critical logs that help administrators troubleshoot issues, monitor system performance, and maintain security. Preserving these journals ensures historical data availability for analysis and audit purposes.

# Details:
# Systemd manages journals in RHEL. Journals are stored in /var/log/journal/ and are rotated automatically based on configured settings. Preserving journals prevents data loss due to rotation or other cleanup operations.

# Examples and Commands:
# View journal storage settings:
journalctl --disk-usage

# Preserve journals permanently (persist across reboots):
mkdir -p /var/log/journal/backup
cp -a /var/log/journal/* /var/log/journal/backup/

# Clean journals to free up disk space (if needed):
journalctl --vacuum-size=100M

# Use Cases:
# - After a system upgrade or critical maintenance, preserving journals ensures that any unexpected issues can be traced back accurately.
# - Compliance and security audits often require maintaining journal logs for specific periods.

# ELI5 (Explain Like I'm 5):
# Imagine journals are like storybooks that tell us everything that happened in our system. Preserving them means we keep these storybooks safe so we can always go back and check if something went wrong.

# Practice Tips:
# - Practice using journalctl to view logs and understand the contents.
# - Experiment with preserving and cleaning journals in a test environment to become comfortable with the commands and their effects.
# - Understand the impact of journal preservation on disk space and system performance.

# End of File

