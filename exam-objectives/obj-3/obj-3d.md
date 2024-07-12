###############################################################
# RHCSA RHEL9 Exam Objective: Identify CPU/memory intensive processes and kill processes
###############################################################

# Purpose:
#   This objective tests your ability to manage system resources efficiently by identifying and managing processes that consume excessive CPU or memory resources.

# Details:
#   As a system administrator, you often need to monitor and optimize system performance. Identifying and terminating processes that are consuming too many resources helps maintain system stability and responsiveness.

# Examples and Commands:
#   Use the following commands and options to identify and terminate resource-intensive processes:

#   Identify top CPU-consuming processes:
$ top

#   Identify top memory-consuming processes:
$ top -o %MEM

#   Identify specific process using PID:
$ ps aux | grep <process_name>

#   Kill a process by PID:
$ kill <PID>

#   Forcefully kill a process by PID:
$ kill -9 <PID>

# Use Cases:
#   Scenario 1: Server experiencing high CPU load due to a runaway process. Use `top` to identify the culprit and `kill` to terminate it.
#   Scenario 2: Memory usage spikes on a database server. Use `top -o %MEM` to find the memory-intensive process and `kill` to release memory.

# ELI5 (Explain Like I'm 5):
#   Imagine your computer has many workers (processes) doing different tasks. Sometimes, one worker starts eating too much food (CPU or memory), making the computer slow. We use tools to find these greedy workers and tell them to stop.

# Practice Tips:
#   - Practice using `top` and `ps` commands regularly to familiarize yourself with process management.
#   - Create scenarios where you deliberately start processes that consume resources and practice terminating them.
#   - Understand the difference between regular termination (`kill`) and forceful termination (`kill -9`) and when each is appropriate.

###############################################################

