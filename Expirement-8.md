# Experiment: 8

## Question
Write shell scripts to print system information. Write shell script to perform basic mathematical calculation. Use redirection operators to store the output of commands.

## Approach

1. **System Information Script**: Create a shell script that gathers and displays various system information such as hostname, kernel version, CPU details, memory usage, and disk space.

2. **Mathematical Calculation Script**: Develop a shell script that performs basic arithmetic operations like addition, subtraction, multiplication, and division using bash capabilities.

3. **Redirection Operators**: Demonstrate how to use redirection operators to capture and store the output of commands and scripts in files.

## Code

### 1. Shell Script to Print System Information

```bash
#!/bin/bash

# system_info.sh - Script to display system information

echo "================= System Information ================="
echo "Hostname: $(hostname)"
echo "Kernel Version: $(uname -r)"
echo "System Date: $(date)"
echo "Uptime: $(uptime -p)"
echo

echo "================= CPU Information ===================="
echo "CPU Model: $(grep 'model name' /proc/cpuinfo | head -1 | cut -d':' -f2 | sed 's/^[ \t]*//')"
echo "Number of CPU Cores: $(grep -c 'processor' /proc/cpuinfo)"
echo "CPU Load Average: $(uptime | awk -F'load average:' '{print $2}')"
echo

echo "================= Memory Information ================="
free -h | grep -v total
echo

echo "================= Disk Usage ========================="
df -h | grep -v tmpfs | grep -v udev
echo

echo "================= Network Information ================"
ip -4 addr | grep inet | grep -v 127.0.0.1 | awk '{print $2,$NF}'
echo

echo "================= Logged In Users ===================="
who
echo
```

### 2. Shell Script to Perform Basic Mathematical Calculations

```bash
#!/bin/bash

# calculator.sh - Basic calculator script

if [ $# -lt 3 ]; then
    echo "Usage: $0 <number1> <operator> <number2>"
    echo "Operators: +, -, *, /, %"
    exit 1
fi

num1=$1
operator=$2
num2=$3

case $operator in
    +)
        result=$(echo "$num1 + $num2" | bc)
        operation="Addition"
        ;;
    -)
        result=$(echo "$num1 - $num2" | bc)
        operation="Subtraction"
        ;;
    \*)
        result=$(echo "$num1 * $num2" | bc)
        operation="Multiplication"
        ;;
    /)
        if [ "$num2" -eq 0 ]; then
            echo "Error: Division by zero is not allowed."
            exit 2
        fi
        result=$(echo "scale=2; $num1 / $num2" | bc)
        operation="Division"
        ;;
    %)
        if [ "$num2" -eq 0 ]; then
            echo "Error: Modulo by zero is not allowed."
            exit 2
        fi
        result=$(echo "$num1 % $num2" | bc)
        operation="Modulo"
        ;;
    *)
        echo "Error: Invalid operator. Use +, -, *, /, or %"
        exit 3
        ;;
esac

echo "$operation: $num1 $operator $num2 = $result"
```

### 3. Using Redirection Operators to Store Command Output

```bash
# Redirect output to a file (overwrite)
./system_info.sh > system_info.txt

# Append output to an existing file
./calculator.sh 10 + 5 >> calculation_results.txt

# Redirect errors to a file
./calculator.sh 10 / 0 2> errors.log

# Redirect both output and errors to different files
./calculator.sh 25 '*' 4 > results.txt 2> calc_errors.log

# Redirect both output and errors to the same file
./system_info.sh > full_output.log 2>&1

# Redirect output to a file and also display it on the screen
./system_info.sh | tee system_output.txt

# Append output to a file and also display it on the screen
./calculator.sh 100 - 45 | tee -a all_calculations.txt

# Redirect the output of one command as input to another command
grep "CPU" < system_info.txt > cpu_info_only.txt

# Redirect output from multiple commands
{
    echo "=== System Information ==="
    ./system_info.sh
    echo "=== Calculation Results ==="
    ./calculator.sh 15 + 27
    ./calculator.sh 100 - 35
    ./calculator.sh 8 '*' 7
    ./calculator.sh 100 / 4
} > combined_output.txt
```

## Code Snippets with Screenshots

### 1. System Information Script

#### Creating and making the script executable
```bash
nano system_info.sh
# Paste the system information script
chmod +x system_info.sh
```

#### Running the system information script
![Screenshot 2025-03-23 142204](https://github.com/user-attachments/assets/41c434b7-079b-48dd-9fc7-e8c089d99939)

### 2. Mathematical Calculation Script

#### Creating and making the script executable
```bash
nano calculator.sh
# Paste the calculator script
chmod +x calculator.sh
```

#### Running basic calculations
![Screenshot 2025-03-23 142800](https://github.com/user-attachments/assets/8dd1378a-8108-43c1-9598-e2e9f1347b25)

### 3. Using Redirection Operators

#### Redirecting output to files
![Screenshot 2025-03-23 143919](https://github.com/user-attachments/assets/8b943c88-f058-4d07-8429-82b0f20fd29c)

#### Using tee to display and save output
![Screenshot 2025-03-23 143945](https://github.com/user-attachments/assets/7ea83113-f440-4bd4-93f6-824750c1cf3d)

#### Combining multiple outputs
![Screenshot 2025-03-23 144331](https://github.com/user-attachments/assets/02780a8f-5373-4245-bea8-2de37295dc1e)
