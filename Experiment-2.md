# Experiment 2

## Question
View the gedit man page.
Use the man -k ext4 command to find the command to tune
ext4 file-system parameters.
Brace expansion is used to generate discretionary strings of
characters. Braces contain a comma-separated list of strings,
or a sequence expression. The result includes the text that
precedes or follows the brace definition

## Approach
1. To view the gedit man page, we use the man command followed by the program name.

2. To find the relevant command for tuning ext4 file-system parameters, we use the man -k command to search for related commands.

3. For brace expansion, we describe its syntax and provide an example to demonstrate how it generates strings.

## Code

### 1. View the gedit man page
```bash
man gedit
```

### 2. Find the command to tune ext4 file-system parameters
```bash
man -k ext4
man tune2fs
```

### 3. Examples of brace expansion
```bash
echo {apple,banana,cherry}
echo file{1..3}.txt
echo pre-{A,B}-post
```

## Code Snippet

### 1. View the gedit man page

![Screenshot 2025-03-22 102408](https://github.com/user-attachments/assets/8967c7fe-1986-4449-8b40-aeab95460735)

### 2. Find the command to tune ext4 file-system parameters

![WhatsApp Image 2025-03-22 at 10 22 15_540c7dc9](https://github.com/user-attachments/assets/3ca0fefe-f118-4d72-b693-7532e91d3f18)

### 3. Examples of brace expansion

![Screenshot 2025-03-22 102635](https://github.com/user-attachments/assets/4587f7fe-f571-4f7e-90e9-1b0e5069ef44)
