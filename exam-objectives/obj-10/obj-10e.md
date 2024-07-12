###########################################################
# Objective: Manage containers
###########################################################

# Purpose:
# Containers are used to deploy and run applications in isolated environments,
# allowing for efficient resource utilization and consistent application behavior.

# Details:
# Basic container management involves starting, stopping, and listing containers
# on a system. This objective ensures administrators can handle containerized
# applications effectively in a production environment.

# Examples and Commands:
# Start a container:
podman start <container_name_or_id>

# Stop a container:
podman stop <container_name_or_id>

# List running containers:
podman ps

# Use Cases:
# - Ensuring specific applications are running or stopped as required.
# - Managing resource allocation by starting or stopping containers as needed.

# ELI5 (Explain Like I'm 5):
# Imagine each container as a small box where an application lives. Starting a
# container turns on the box so the application inside can run. Stopping it
# turns off the box.

# Practice Tips:
# - Practice starting, stopping, and listing containers frequently.
# - Understand how to identify containers by name or ID for management.
# - Experiment with different containerized applications to get familiar
#   with their behavior and management commands.

