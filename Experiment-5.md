# Experiment 5

## Question
Implement ps, top, kill command with their options.
Installing, updating, and removing software by apt-get
command.

## Approach

1. To demonstrate the ps command, I'll show how to use it with various commonly used options to display information about processes running on a Linux system.

2. The top command provides a dynamic real-time view of the running system. I'll demonstrate how to use it with various options to customize the output and behavior.

3. The kill command is used to send signals to processes. I'll show how to use it with different options to terminate or control processes.

4. The apt-get command is used for package management in Debian-based Linux distributions such as Ubuntu. I'll demonstrate how to use it for installing, updating, and removing software.

## Code

### 1. ps Command

```bash
# Display all running processes
ps aux

# Display processes for the current user
ps -u $(whoami)

# Display detailed information about a specific process
ps -fp 2224
```

### 2. top Command

```bash
# Start top
top

# Monitor processes for a specific user
top -u jhon

# Monitor a specific process
top -p 1332
```

### 3. kill Command

```bash
# Terminate a process gracefully
kill 2198

# Forcefully terminate a process
kill -9 1980

# Terminate all instances of a process
killall firefox
```

### 4. apt-get Command

```bash
# Install a package (e.g., Vim)
sudo apt-get install vim

# Update the package list
sudo apt-get update

# Upgrade all installed packages
sudo apt-get upgrade

# Remove a package (e.g., Vim)
sudo apt-get remove vim

# Remove a package and its configuration files
sudo apt-get purge vim

# Remove unused packages
sudo apt-get autoremove
```

## Code Snippet

### 1. The ps command is used to display information about running processes.

Display all running processes

![Screenshot 2025-03-22 145357](https://github.com/user-attachments/assets/31dca5b7-cbae-4747-bde7-23b4c7bc4ee4)

Display processes for the current user

![Screenshot 2025-03-22 145416](https://github.com/user-attachments/assets/f98ee8da-8ef4-4ba7-8406-e4af40259115)

Display detailed information about a specific process

![Screenshot 2025-03-22 145430](https://github.com/user-attachments/assets/b3e22a3c-d0f9-464f-9636-28940c1112c5)


### 2. The top command provides a real-time view of system processes and resource usage.

Start top

![Screenshot 2025-03-22 145924](https://github.com/user-attachments/assets/f255401a-344a-4938-9457-4521ad49e985)

Monitor processes for a specific user

![Screenshot 2025-03-22 150004](https://github.com/user-attachments/assets/be4c30a3-bc10-40b1-b0f1-faf1a2f3b674)

Monitor a specific process

![Screenshot 2025-03-22 150043](https://github.com/user-attachments/assets/a486954c-8d05-4ffc-88d6-e32a5013ea86)


### 3. The kill command is used to terminate processes.

![Screenshot 2025-03-22 150931](https://github.com/user-attachments/assets/b4eb8824-c3b1-4120-a538-e270b4a51c81)


### 4. The apt-get command is used for package management in Ubuntu.

Install a package (e.g., Vim)

![Screenshot 2025-03-22 151316](https://github.com/user-attachments/assets/1e965a83-09d9-49b4-bc9d-4e22e9ebdd0e)

Update the package list

![Screenshot 2025-03-22 151330](https://github.com/user-attachments/assets/f62b6d27-5eee-4628-8305-0323bb774bdf)

Upgrade all installed packages

![Screenshot 2025-03-22 151420](https://github.com/user-attachments/assets/ccc108ce-7353-4e7d-8fba-53c00a143de4)

Remove a package (e.g., Vim)

![Screenshot 2025-03-22 151514](https://github.com/user-attachments/assets/df1b7735-0f10-4a14-b341-b3b5adee9786)

Remove a package and its configuration files

![Screenshot 2025-03-22 151542](https://github.com/user-attachments/assets/9c945d2d-2117-4d08-9578-2c4abc1f379e)

Remove unused packages

![Screenshot 2025-03-22 151707](https://github.com/user-attachments/assets/5291f730-d318-4db1-88be-8bf5e591fd39)
