#######################################
# Objective: Configure key-based authentication for SSH
#######################################

# Purpose:
# Key-based authentication enhances SSH security by replacing password-based authentication with cryptographic keys.

# Details:
Key-based authentication involves generating a public/private key pair. The public key is placed on the server, while the private key remains secure on the client. When SSHing into the server, the client proves its identity by presenting the private key, and the server verifies this identity using the corresponding public key.

# Examples and Commands:

## 1. Generate SSH key pair on the client
$ ssh-keygen -t rsa -b 2048
# Follow prompts to generate keys in default location (~/.ssh/id_rsa).

## 2. Copy the public key to the server
$ ssh-copy-id username@server_ip
# This command copies the public key to the server's ~/.ssh/authorized_keys file.

## 3. Verify key-based authentication works
$ ssh username@server_ip
# You should be logged in without a password prompt, using the private key for authentication.

# Use Cases:
Key-based authentication is crucial in environments where security is paramount, such as enterprise networks, cloud environments, and any system accessible via SSH over the internet. It reduces the risk of brute-force attacks targeting password authentication.

# ELI5 (Explain Like I'm 5):
Imagine you have a special key (private key) to open a secret door (server). The door has a copy of the key's picture (public key). When you want to open the door, you show your key, and the door checks the picture to see if they match.

# Practice Tips:
- Practice generating key pairs and copying keys to servers using different methods (ssh-copy-id, manual copying).
- Understand file permissions (e.g., ~/.ssh/authorized_keys should be restricted to the user) to ensure secure key storage.
- Experiment with different key types (RSA, ECDSA, ED25519) to understand their strengths and weaknesses in different scenarios.

