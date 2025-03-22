# Experiment 1

## Question
Use the touch command to create sets of empty practice files to use during this lab. In each set, replace X with the numbers 1 through 6. Create six files with names of the form songX.mp3, snapX.jpg, filmX.avi. Create three subdirectories for organizing your files, and name the subdirectories friends, family, and work. Use a single command to create all three subdirectories at the same time.

## Approach
1. Use the touch command to create multiple files in a loop.
2. Utilize brace expansion {} in the shell to generate numbered files efficiently.
3. Use the mkdir command to create multiple directories in a single step.

## Code

### 1. Create the empty files
```bash
touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi
```

### 2. Create the subdirectories and verify
```bash
mkdir -p friends family work
ls
```

### 3. Organize files into subdirectories
```bash
mv song*.mp3 friends/
mv snap*.jpg family/
mv film*.avi work/
```

## Code Snippet

![Screenshot 2025-03-22 094903](https://github.com/user-attachments/assets/d2b6425d-e26f-4e38-b96e-bfa274446693)
