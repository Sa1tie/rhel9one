##############################################################
# Objective: Build a container from a Containerfile
##############################################################

# Purpose:
# Building containers from a Containerfile allows system administrators
# to define and customize container environments using a declarative
# format, facilitating reproducibility and consistency in container deployments.

# Details:
# A Containerfile is similar to a Dockerfile and specifies the steps and
# dependencies required to build a container image. This file typically
# includes instructions for installing packages, copying files, setting
# environment variables, and defining runtime commands.

# Examples and Commands:
# Example of a Containerfile to build an Apache HTTP Server container:

# Start of Containerfile
FROM registry.access.redhat.com/ubi8/ubi-minimal

RUN microdnf install httpd \
    && echo "Apache HTTP Server installed."

COPY index.html /var/www/html/

CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
# End of Containerfile

# Use Cases:
# - Building a customized application environment encapsulated in a container.
# - Deploying consistent development, testing, and production environments.

# ELI5 (Explain Like I'm 5):
# Imagine a recipe for making your favorite toy out of building blocks.
# A Containerfile is like that recipe, telling the computer exactly how
# to put together all the parts (software, settings) needed to create a
# container that runs your applications.

# Practice Tips:
# - Practice writing and building Containerfiles for different applications.
# - Understand how to use Docker or Podman commands to build images from Containerfiles.
# - Experiment with adding different packages, files, and configurations in Containerfiles to
#   understand their impact on the resulting container image.

