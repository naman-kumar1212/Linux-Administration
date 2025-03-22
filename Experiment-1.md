# Experiment 1

## Question
Use the touch command to create sets of empty practice files to use during this lab. In each set, replace X with the numbers 1 through 6. Create six files with names of the form songX.mp3, snapX.jpg, filmX.avi. Create three subdirectories for organizing your files, and name the subdirectories friends, family, and work. Use a single command to create all three subdirectories at the same time.

## Approach
1. Use the touch command to create multiple files in a loop.
2. Utilize brace expansion {} in the shell to generate numbered files efficiently.
3. Use the mkdir command to create multiple directories in a single step.

## Code

# Create the empty files
touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi

# Create the subdirectories
mkdir -p friends family work


# Verify the files and directories
ls

## Code Snippet
