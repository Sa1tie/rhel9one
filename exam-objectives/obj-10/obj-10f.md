##########################
# Objective: Run a service inside a container
##########################

# Purpose:
# Running services inside containers provides a lightweight and isolated environment 
# for applications, improving scalability and consistency in deployments.

# Details:
# Containers encapsulate an application and its dependencies, ensuring they run 
# consistently across different environments. Running services inside containers 
# allows for easier management, deployment, and scaling of applications.

# Examples and Commands:
# Create a Docker container running an NGINX web server:

# 1. Pull the NGINX container image from Docker Hub:
docker pull nginx

# 2. Run a container named 'nginx-server' from the NGINX image:
docker run -d --name nginx-server -p 80:80 nginx

# 3. Check the status of the container:
docker ps

# Use Cases:
# - Hosting web applications: Running a web server like NGINX or Apache inside 
#   containers for serving web content.
# - Microservices architecture: Running each service of a complex application in 
#   separate containers for modularity and scalability.

# ELI5 (Explain Like I'm 5):
# Imagine containers as lunchboxes for apps. You put all the food (app + its stuff) 
# in the box (container). Running a service inside means opening the lunchbox 
# (starting the container) and letting the food (app) do its job.

# Practice Tips:
# - Practice creating and running containers using Docker with various applications 
#   (e.g., NGINX, MySQL) to get comfortable with different scenarios.
# - Experiment with networking options (e.g., port mapping, linking containers) 
#   to understand how services communicate inside and outside containers.
# - Learn Dockerfile basics to create custom container images tailored to specific 
#   application requirements.

