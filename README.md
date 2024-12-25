# Faculty Renovation Scheduler and Budget Optimizer

This project implements solutions for optimizing renovation schedules and budget allocations during the Faculty of Computer and Informatics Engineering's relocation. It applies dynamic programming techniques, including Weighted Interval Scheduling and Knapsack Problem, to maximize efficiency.

## Overview

This system handles two major tasks:
1. **Room Renovation Scheduling**: Creates daily schedules for room renovations by maximizing priority values, ensuring that the most important tasks are completed first.
2. **Budget Allocation**: Selects the most essential items to purchase under a fixed budget of 200,000 TL, ensuring maximum value.

Key techniques used:
- **Weighted Interval Scheduling**: For scheduling tasks efficiently.
- - **Knapsack Problem**: For optimal resource allocation within the budget.

## How It Works

1. **Input Files**:
   - `room_time_intervals.txt`: Contains room availability intervals (e.g., Floor_1, Room_2, 09:00–12:00).
   - `priority.txt`: Specifies the priority values of each room (higher values indicate greater importance).
   - `items.txt`: Lists items with their prices and necessity values.

2. **Processing**:
   - The system reads these input files and combines the data into schedules and purchase plans.
   - Algorithms are applied to find the best possible schedules and budget usage.

3. **Output**:
   - **Optimal Schedules**: Displays the renovation schedule for each floor, highlighting total priority gains.
   - **Budget Usage**: Lists selected items and their total necessity value.

## Features

- **Scheduling**: Maximizes priority gains for all floors using dynamic programming.
- **Budget Optimization**: Ensures the most critical items are purchased within the budget constraints.
- **Robust Testing**: Memory safety and functional accuracy validated with Valgrind and Calico.

## Example Workflow

### Inputs:
- **room_time_intervals.txt**:
  ```
  Floor_1 Room_2 09:00 12:00
  Floor_2 Room_1 14:00 17:00
  ```

- **priority.txt**:
  ```
  Floor_1 Room_2 50
  Floor_2 Room_1 40
  ```

- **items.txt**:
  ```
  Desk 15000 80
  Chair 10000 50
  ```

### Outputs:
- **Schedules**:
  ```
  Best Schedule for Each Floor
  Floor_1 --> Priority Gain: 50
  Floor_1 Room_2 09:00 12:00
  ```

- **Budget Usage**:
  ```
  Best Use of Budget
  Total Value --> 80.0
  Desk
  ```

## Technologies Used

- **C++**: Core implementation of algorithms.
- **Dynamic Programming**: For solving scheduling and budget allocation problems.
- **Testing Tools**:
  - **Valgrind**: For memory leak detection.
  - **Calico**: For functional testing.

## How to Run

### Prerequisites

- **Compiler**: Requires `g++` for compilation.
- **Environment**: Developed and tested on Ubuntu.

### Compilation

```bash
g++ 7024253.cpp -o renovation_optimizer -Wall -Werror
```

### Execution

Run the program with a test case number:

```bash
./renovation_optimizer <case_number>
```

### Example Commands

- To run for test case 1:
  ```bash
  ./renovation_optimizer 1
  ```

- To run for test case 2:
  ```bash
  ./renovation_optimizer 2
  ```

### Testing

#### Memory Check with Valgrind:

```bash
valgrind --tool=memcheck --leak-check=full ./renovation_optimizer <case_number>
```

#### Functionality Check with Calico:

```bash
calico test.yaml |& tee calico_log.txt
```

## Key Skills Demonstrated

- **Algorithm Design**: Mastery of Weighted Interval Scheduling and Knapsack Problem.
- **Memory Management**: Validated with Valgrind for safety.
- **Testing and Debugging**: Automated testing using Calico.
- **Optimization**: Tackling real-world resource allocation problems.

## Project Highlights

- Employs efficient algorithms for renovation scheduling and budget allocation.
- Handles complex constraints such as non-overlapping time intervals and budget limits.
- Fully tested for memory safety and correctness.

## Privacy Note

**Note**: Details specific to individuals and professors have been omitted to maintain privacy.  
This project complies with academic integrity policies and demonstrates individual effort in addressing the assigned problem for the BLG 336E - Analysis of Algorithms II course at ITU.
