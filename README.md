
# Faculty Renovation Scheduler and Budget Optimizer

This project implements solutions for optimizing renovation schedules and budget allocations during the Faculty of Computer and Informatics Engineering's relocation. It applies dynamic programming techniques, including Weighted Interval Scheduling and Knapsack Problem, to maximize efficiency.

## Overview

The system creates optimal schedules for renovation tasks in faculty rooms based on time intervals and priority values. It also determines the most valuable items to purchase within a fixed budget of 200,000 TL.

### Key Features

1. **Scheduling Optimization**:
   - Utilizes the Weighted Interval Scheduling algorithm to prioritize renovations.
   - Maximizes the total priority gain for each floor.

2. **Budget Optimization**:
   - Solves the Knapsack Problem to select items with the highest necessity value within the budget.

3. **Comprehensive Testing**:
   - Memory usage analysis with Valgrind.
   - Functionality verification using Calico.

### Input Files

1. `room_time_intervals.txt`: Specifies room availability intervals.
2. `priority.txt`: Contains priority values for each room.
3. `items.txt`: Lists items, their prices, and necessity values.

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

## Technologies Used

- **C++**: For implementation.
- **Dynamic Programming**: Algorithms for scheduling and budget optimization.
- **Testing Tools**: Valgrind and Calico.

## Project Highlights

- Employs efficient algorithms for renovation scheduling and budget allocation.
- Handles complex constraints such as non-overlapping time intervals and budget limits.
- Fully tested for memory safety and correctness.

## Privacy Note

This repository adheres to academic integrity policies and reflects individual effort in solving the assigned problem for the BLG 336E - Analysis of Algorithms II course at ITU.
