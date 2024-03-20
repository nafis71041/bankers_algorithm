# Banker's Algorithm Implementation in C

This repository contains an implementation of the Banker's Algorithm in C. The Banker's Algorithm is a resource allocation and deadlock avoidance algorithm used in operating systems.

## Table of Contents

1. [Introduction](#introduction)
2. [Usage](#usage)
3. [Implementation Details](#implementation-details)
4. [Sample Input File Format](#sample-input-file-format)
5. [License](#license)

## Introduction

The Banker's Algorithm is a deadlock avoidance algorithm that helps in preventing deadlocks by ensuring that processes do not enter an unsafe state. It operates by maintaining a data structure that represents the current state of the system, including resource allocation, maximum resource requirements, and available resources. Based on this information, it determines if a resource request from a process can be safely granted without leading the system into an unsafe state, which could result in a deadlock.

## Usage

To use this implementation, follow these steps:

1. Compile the code using a C compiler (e.g., gcc).
   ```
   gcc banker.c -o banker
   ```
2. Prepare a data file containing information about the system state. Each line of the file should represent the allocation and maximum resource requirements of a process, followed by the available resources.
3. Execute the compiled program, providing the path to the data file as a command-line argument.
   ```
   ./banker datafile.txt
   ```
4. Follow the on-screen instructions to interact with the program. You can print the current system state, find if the system is in a safe state, request resources, release resources, or exit the program.

## Implementation Details

- The implementation includes functions for system initialization, printing the current state, checking if the system is in a safe state, requesting resources, and releasing resources.
- The `system_state` struct represents the state of the system, including resource allocation, maximum resource requirements, need, and available resources.
- The `initialization` function reads input data from a file and initializes the system state accordingly.
- The `is_safe` function implements the Banker's Algorithm to check if the system is in a safe state.
- The `request` function handles resource requests from processes, ensuring that the request does not lead to an unsafe state.
- The `release` function handles resource release requests from processes.

## Sample Input File Format

A sample input file should contain the following information:

```bash
<allocation_matrix>

<maximum_matrix>

<available_resources>
```

For example:

``` bash
0 1 0
2 0 0
3 0 2
2 1 1
0 0 2

7 5 3
3 2 2
9 0 2
2 2 2
4 3 3

3 3 2
```

Feel free to contribute to this project by submitting bug reports, feature requests, or pull requests. Enjoy using the Banker's Algorithm implementation in C!
