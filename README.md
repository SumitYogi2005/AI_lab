# Artificial Intelligence Lab Programs

A collection of Python implementations of three classic Artificial Intelligence problems. The programs demonstrate problem-solving techniques such as **Backtracking**, **Breadth-First Search (BFS)**, and **State-Space Search**.

## 📌 Project Overview

This repository contains the following AI lab programs:

| No. | Program | Technique Used |
|---|---|---|
| 1 | Basic Sudoku Solver | Backtracking |
| 2 | Missionaries and Cannibals Problem | Breadth-First Search (BFS) |
| 3 | Water Jug Problem | Breadth-First Search (BFS) and State-Space Search |

## 🛠️ Technologies Used

- **Programming Language:** Python 3
- **Concepts:** Artificial Intelligence, Search Algorithms, State-Space Representation, Backtracking
- **Libraries:** Python standard library only (no external packages required)

## 📂 Project Structure

```text
AI-Lab-Programs/
│
├── Basic _Sudoku_ Solver
├── Missionaries_ and_Cannibals Problem
├── Water_jug_problem
└── README.md
```

> The program files in this repository do not have `.py` extensions. You can run them with Python by specifying their exact filenames, or rename them with a `.py` extension for convenience.

## 1. Basic Sudoku Solver

### Description
This program solves a 9×9 Sudoku puzzle. Empty cells are represented by `0`. It fills the empty cells with numbers from 1 to 9 while following standard Sudoku rules.

### Algorithm: Backtracking
Backtracking tries a valid number in an empty cell and recursively attempts to solve the remaining puzzle. If a choice leads to a dead end, it removes that number and tries another possibility.

### Sudoku Rules
- Each row must contain the digits 1 to 9 without repetition.
- Each column must contain the digits 1 to 9 without repetition.
- Each 3×3 subgrid must contain the digits 1 to 9 without repetition.

### Working
1. Find an empty cell in the grid.
2. Try numbers from 1 to 9.
3. Check whether the selected number is valid in its row, column, and 3×3 subgrid.
4. If valid, place the number and recursively solve the remaining grid.
5. If no number works, reset the cell to `0` and backtrack.
6. Continue until the puzzle is solved or no solution exists.

### Output
The program displays the solved Sudoku grid or prints `No solution exists!` if the puzzle cannot be solved.

**Note:** To solve another puzzle, update the `grid` variable in the program. Use `0` for empty cells.

## 2. Missionaries and Cannibals Problem

### Description
The Missionaries and Cannibals problem is a classic AI search problem. Missionaries and cannibals must cross a river using a boat that has a limited capacity. At no point can cannibals outnumber missionaries on either riverbank when missionaries are present.

### Algorithm: Breadth-First Search (BFS)
BFS explores states level by level using a queue. It records each state's parent so that the solution path can be reconstructed once the goal state is reached.

### State Representation
A state is represented as:

```text
(M, C, B)
```

Where:
- `M` = Number of missionaries on the starting bank.
- `C` = Number of cannibals on the starting bank.
- `B` = Boat position (`0` = starting bank, `1` = opposite bank).

### Input
The program asks the user to enter:
- Number of missionaries.
- Number of cannibals.
- Boat capacity.

### Working
1. Define the initial state and goal state.
2. Generate all possible boat movements within the boat capacity.
3. Check whether each resulting state is valid.
4. Add unvisited valid states to the BFS queue.
5. Store parent states to reconstruct the path.
6. Stop when the goal state is reached or no solution is available.

### Output
The program prints the sequence of states from the initial state to the goal state, followed by `Goal Achieved!`. If no valid path is found, it prints `No solution possible!`.

## 3. Water Jug Problem

### Description
The Water Jug problem is a classic AI problem in which two jugs of different capacities are used to measure a specified quantity of water. The program starts with both jugs empty and searches for a sequence of operations that produces the target amount in either jug.

### Algorithm: Breadth-First Search (BFS)
The program uses BFS to explore possible water-level states. Each state represents the amount of water currently present in the two jugs.

### State Representation
A state is represented as:

```text
(X, Y)
```

Where:
- `X` = Current amount of water in Jug 1.
- `Y` = Current amount of water in Jug 2.

### Available Operations
The program supports eight operations:

1. Fill Jug 1 completely.
2. Fill Jug 2 completely.
3. Transfer all water from Jug 1 to Jug 2, if it fits.
4. Transfer all water from Jug 2 to Jug 1, if it fits.
5. Pour water from Jug 1 to Jug 2 until Jug 1 is empty or Jug 2 is full.
6. Pour water from Jug 2 to Jug 1 until Jug 2 is empty or Jug 1 is full.
7. Empty Jug 1.
8. Empty Jug 2.

### Input
The program asks the user to enter:
- Capacity of Jug 1.
- Capacity of Jug 2.
- Target amount of water to be measured.

### Working
1. Start with the initial state `(0, 0)`.
2. Add the initial state to the BFS queue.
3. Generate new states by applying the eight operations.
4. Ignore unchanged and previously visited states.
5. Store parent states to reconstruct the solution path.
6. Stop when the target amount is present in either jug.
7. Print the sequence of states leading to the goal.

### Output
The program displays each step, the final goal state, and `GOAL ACHIEVED!`. If no solution is found, it prints `No solution possible!`.

## 👩‍💻 Project Information

**Project:** Artificial Intelligence Lab Programs  
**Language:** Python 3  
**Domain:** Artificial Intelligence  

---

*This repository is intended for learning and demonstrating fundamental Artificial Intelligence problem-solving and search algorithms.*
