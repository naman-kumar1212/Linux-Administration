# Experiment: 7

## Question
Implement chown, chmod command with their options.

## Approach

1. **CHOWN Command**: The chown (change owner) command is used to change the owner and group of files and directories. I'll demonstrate how to use it with various options to modify ownership of files and directories.

2. **CHMOD Command**: The chmod (change mode) command is used to change the access permissions of files and directories. I'll show how to use it with different options and notations to modify file permissions.

## Code

### 1. chown Command

```bash
# Change owner of a file
sudo chown user1 file.txt

# Change owner and group of a file
sudo chown user1:group1 file.txt

# Change only the group of a file
sudo chown :group1 file.txt

# Change ownership recursively for a directory
sudo chown -R user1:group1 directory/

# Change ownership but follow symbolic links
sudo chown -L user1:group1 symlink

# Change ownership reference (same as another file)
sudo chown --reference=reference_file.txt target_file.txt
```

### 2. chmod Command

```bash
# Change permissions using octal notation
chmod 755 file.txt

# Change permissions using symbolic notation
chmod u+x file.txt

# Add execute permission for all users
chmod +x file.txt

# Remove write permission for group and others
chmod go-w file.txt

# Change permissions recursively for a directory
chmod -R 755 directory/

# Change permissions but don't affect symbolic links
chmod -h 755 symlink

# Apply the same permissions as another file
chmod --reference=reference_file.txt target_file.txt
```

## Code Snippets with Screenshots

### 1. The chown command - Change file ownership

![Screenshot 2025-03-23 140932](https://github.com/user-attachments/assets/4d857648-898c-4b38-bd73-858ff181c2e0)

### 2. The chmod command - Change file permissions

![Screenshot 2025-03-23 141311](https://github.com/user-attachments/assets/1caaea08-3bf3-4f8a-a6d3-a7b6676e4917)
