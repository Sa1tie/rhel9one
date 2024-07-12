###########################################################
# Objective: Find and retrieve container images from a remote registry
###########################################################

# Purpose:
# This objective focuses on the ability to locate and download container images
# from remote registries, which is essential for deploying and managing containers
# in a production environment.

# Details:
# Container images are stored in remote registries like Docker Hub, Quay.io,
# or private registries. System administrators need to find specific images
# and pull them onto their systems to use them for containerized applications.

# Examples and Commands:
# Command to pull an image from Docker Hub:
$ sudo podman pull docker.io/library/nginx

# Command to pull an image from Quay.io (requires authentication):
$ sudo podman pull quay.io/username/image-name

# Use Cases:
# Example: Pulling a MySQL container image for database deployment.
# $ sudo podman pull docker.io/library/mysql

# ELI5 (Explain Like I'm 5):
# Imagine you're shopping online for toys. You look up a specific toy you want,
# and then you click "Add to Cart" to bring it home. Similarly, finding and
# pulling a container image is like searching for a specific toy and then
# downloading it to use on your computer.

# Practice Tips:
# 1. Familiarize yourself with different container registries and their usage.
# 2. Practice pulling popular container images like NGINX, MySQL, or Redis.
# 3. Understand authentication and security considerations when pulling images
#    from private registries.
# 4. Use `podman search` command to find available images before pulling.
# 5. Experiment with different versions of the same image to understand versioning.

# Remember to practice these commands on your RHEL9 system to ensure
# familiarity and readiness for the exam.

