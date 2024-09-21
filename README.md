# Bash Scripting Programs

This repository contains a collection of Bash scripts that demonstrate different operations such as printing prime numbers, even/odd numbers, Fibonacci series, and more. These scripts are intended for practicing Bash scripting, especially for DevOps tasks.

## Table of Contents

- [Prime Numbers](#prime-numbers)
- [Even and Odd Numbers](#even-and-odd-numbers)
- [Fibonacci Series](#fibonacci-series)
- [Disk Space Monitoring](#disk-space-monitoring)
- [How to Run](#how-to-run)

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
