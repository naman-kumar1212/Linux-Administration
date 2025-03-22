# Experiment: 6

## Question
Create the operator1 user and confirm that it exists in the system. Set the password for operator1. Create the additional operator2 and operator3 users. Set their passwords as well. Run the usermod -c command to update the comments of the operator1 user account. Remove the operator3 user from the system.

## Approach

1. **Create User**: To create users in Linux, we'll use the useradd command and confirm existence by checking the /etc/passwd file.

2. **Set Password**: We'll set passwords for newly created users with the passwd command.

3. **Update User Information**: The usermod command with the -c option will be used to update the comment field for a user.

4. **Remove User**: The userdel command will be used to remove a user from the system.

## Code

### 1. Creating Users and Confirming Existence

```bash
# Create the operator1 user
sudo useradd operator1

# Confirm that operator1 exists in the system
grep operator1 /etc/passwd
```

### 2. Setting Passwords

```bash
# Set password for operator1
sudo passwd operator1

# Create and set password for operator2
sudo useradd operator2
sudo passwd operator2

# Create and set password for operator3
sudo useradd operator3
sudo passwd operator3
```

### 3. Updating User Comments

```bash
# Update the comment field for operator1
sudo usermod -c "System Operator 1" operator1

# Verify the comment was updated
grep operator1 /etc/passwd
```

### 4. Removing a User

```bash
# Remove operator3 from the system
sudo userdel operator3

# Verify user was removed
grep operator3 /etc/passwd
```

## Code Snippets with Screenshots

### 1. Creating operator1 user and confirming existence

#### Create operator1 and check existence
![Screenshot 2025-03-22 152730](https://github.com/user-attachments/assets/c3a0d622-ec42-4a4e-80bb-4374d0e995bc)

### 2. Setting passwords for users

![Screenshot 2025-03-22 153014](https://github.com/user-attachments/assets/e622b9cd-9902-4aad-920a-8ea5a7510611)

### 3. Update comment for operator1 user account

#### Update comment with usermod -c
![Screenshot 2025-03-22 153215](https://github.com/user-attachments/assets/3f162309-fd77-41b6-b428-eea442de21af)

### 4. Remove operator3 user from the system

#### Remove operator3 and verify removal
![Screenshot 2025-03-22 153303](https://github.com/user-attachments/assets/cce589d2-b4cd-478e-96f3-360ae3b3ca43)
