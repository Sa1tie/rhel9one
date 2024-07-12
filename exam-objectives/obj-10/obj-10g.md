################################################################################
# Objective: Configure a container to start automatically as a systemd service #
################################################################################

# Purpose:
# This objective ensures that a containerized application can start automatically
# with the system, leveraging systemd for service management. It's crucial for
# maintaining uptime and automating the deployment of containerized services.

# Details:
# Systemd is the init system used in RHEL 9, responsible for managing services,
# including containers. By defining a systemd service unit for a container,
# administrators can specify how and when the container should start, stop,
# and interact with the system.

# Examples and Commands:
# 1. Create a systemd service unit file for the container:
sudo vi /etc/systemd/system/mycontainer.service

# 2. Add the following content to the mycontainer.service file:
[Unit]
Description=My Container Service
After=docker.service network.target

[Service]
Restart=always
ExecStart=/usr/bin/docker start -a mycontainer
ExecStop=/usr/bin/docker stop -t 2 mycontainer

[Install]
WantedBy=default.target

# 3. Save and close the file. Then, reload systemd to read the new unit:
sudo systemctl daemon-reload

# 4. Enable the service to start automatically at boot:
sudo systemctl enable mycontainer.service

# 5. Start the container service:
sudo systemctl start mycontainer.service

# Use Cases:
# - Running web applications or databases within Docker containers that need
#   to start automatically with the server reboot.
# - Automating deployment of microservices architecture where each service is
#   encapsulated in its container and managed as a systemd service.

# ELI5 (Explain Like I'm 5):
# Think of systemd as a manager for all the services (like containers) on your
# computer. When you create a service unit for a container, you're telling systemd
# how and when to turn on (start) and turn off (stop) your container automatically.

# Practice Tips:
# - Practice creating systemd service units for different types of containers
#   (e.g., databases, web servers) to understand different configuration options.
# - Test the automatic startup behavior by rebooting your system and ensuring
#   that your containerized services start as expected.

