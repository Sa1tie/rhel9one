##################################################
# Manage containers - Inspect container images
##################################################

# Purpose:
#   Inspecting container images allows administrators to review
#   and understand the contents and configuration of images
#   before deploying them into production environments.

# Details:
#   When managing containers, it's crucial to inspect images
#   to verify their integrity, check for security vulnerabilities,
#   and understand the software and configurations they include.
#   Inspection includes viewing metadata, layer information,
#   and running commands within a temporary container instance.

# Examples and Commands:
#   1. List images on the system:
docker images

#   2. Inspect details of a specific image:
docker image inspect <image_name_or_id>

#   3. View image history and layers:
docker history <image_name_or_id>

#   4. Run a temporary container to explore image contents:
docker run -it --rm <image_name_or_id> /bin/bash

# Use Cases:
#   - Before deploying a new version of an application, inspect
#     the container image to ensure it includes the necessary
#     dependencies and configuration changes.
#   - Troubleshoot issues by examining the environment and
#     configuration inside the container image.

# ELI5 (Explain Like I'm 5):
#   Imagine you have a magic box (container image) that contains
#   all the toys you need to play with. Before opening the box
#   and playing, you want to make sure all your favorite toys
#   are inside and nothing strange is hidden inside.

# Practice Tips:
#   - Practice using `docker images`, `docker image inspect`,
#     and `docker history` commands regularly to become familiar
#     with viewing and understanding container images.
#   - Experiment with running temporary containers to interact
#     with the file system and environment of different images.


