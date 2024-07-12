# Objective: Adjust process scheduling

# Purpose:
Adjusting process scheduling allows administrators to prioritize or manage how processes utilize system resources, optimizing performance and responsiveness.

# Details:
Process scheduling involves assigning priorities to processes and determining how CPU resources are allocated among them. This can impact system responsiveness, throughput, and overall performance.

# Examples and Commands:
# View current scheduling policy and priority of processes
ps -eo pid,comm,nice,ni,pri,psr --sort=pri

# Change the priority of a running process
renice +10 1234  # Increases the priority of process with PID 1234 by 10
renice -5 5678   # Decreases the priority of process with PID 5678 by 5

# Set the scheduling policy for a process
chrt -r -p 20 1234  # Sets real-time scheduling priority 20 for process with PID 1234

# Use nice to start a process with modified priority
nice -n 10 command  # Starts 'command' with a niceness value of 10 (lower priority)

# Use Cases:
1. Ensure critical database processes have higher priority to maintain responsiveness.
2. Lower priority of background tasks to prevent them from impacting foreground application performance.
3. Adjust scheduling for real-time applications to meet strict timing requirements.

# ELI5 (Explain Like I'm 5):
Think of process scheduling like deciding who gets to talk first during playtime. Some kids (processes) have more important things to say, so they go first. Others might have to wait longer if their game isn't as important.

# Practice Tips:
- Practice using `ps`, `renice`, `chrt`, and `nice` commands to observe and modify process priorities.
- Experiment with different scenarios to understand how adjusting priorities impacts system performance.
- Familiarize yourself with real-world use cases to apply these concepts effectively during the exam.


