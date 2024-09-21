# Bash Scripting Programs

This repository contains Bash scripts to perform various tasks such as printing prime numbers, and even/odd numbers, generating the Fibonacci series, printing multiplication tables, and checking if numbers are greater than or less than a given value.

## Table of Contents

- [Prime Numbers](#prime-numbers)
- [Even and Odd Numbers](#even-and-odd-numbers)
- [Fibonacci Series](#fibonacci-series)
- [Multiplication Table](#multiplication-table)
- [Less Than / Greater Than](#less-than--greater-than)
- [How to Run the Scripts](#how-to-run-the-scripts)

---

## Prime Numbers

This script prints all prime numbers between 2 and 100. A number is prime if it is only divisible by 1 and itself.

### Code:

```bash
#!/bin/bash

for ((num=2; num<=100; num++))
do
    is_prime=1
    for ((i=2; i*i<=num; i++))
    do
        if ((num % i == 0))
        then
            is_prime=0
            break
        fi
    done
    if ((is_prime == 1))
    then
        echo "$num is a prime number"
    fi
done
```
Even and Odd Numbers
This script prints all even and odd numbers between ranges (e.g., 1 to 100).

### Code:

```bash
#!/bin/bash

echo "Even numbers between 1 and 100:"
for ((num=1; num<=100; num++))
do
    if ((num % 2 == 0))
    then
        echo "$num"
    fi
done

echo "Odd numbers between 1 and 100:"
for ((num=1; num<=100; num++))
do
    if ((num % 2 != 0))
    then
        echo "$num"
    fi
done
```
Fibonacci Series
This script prints the Fibonacci series up to a given number of terms (e.g., 10 terms).

### Code:

```bash
#!/bin/bash

n=10 # Number of terms

a=0
b=1

echo "Fibonacci series up to $n terms:"

for ((i=0; i<n; i++))
do
    echo -n "$a "
    fn=$((a + b)) 
    a=$b
    b=$fn
done

echo
```
Multiplication Table
This script prints the multiplication table for a given number (e.g., 5).
### Code:

```bash
#!/bin/bash

num=5 # Number to print the multiplication table for

echo "Multiplication table for $num:"

for ((i=1; i<=10; i++))
do
    echo "$num x $i = $((num * i))"
done
```
Less Than / Greater Than
This script checks if a number is greater than, less than, or equal to a given value (e.g., 50).
### Code:

```bash
#!/bin/bash

read -p "Enter a number: " num
threshold=50

if ((num > threshold))
then
    echo "$num is greater than $threshold"
elif ((num < threshold))
then
    echo "$num is less than $threshold"
else
    echo "$num is equal to $threshold"
fi
```
How to Run the Scripts
Clone this repository:
### Code:

```bash
git clone https://github.com/MaryamMairaj123/Shell-Scripting/.git
cd Shell-Scripting
```
Give Permission to script executable: 
### Code:

```bash
chmod 777 anybovecode.sh
```
Run the script:
### Code:

```bash
./script-name.sh
```
For any Query DM me at: maryammairaj53@gmail.com 


