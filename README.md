# Rubik's Cube Solver in C++

A Rubik's Cube Solver implemented in C++ using multiple cube representations and search algorithms such as BFS, DFS, IDDFS and IDA*.

## Demo Video
  https://github.com/user-attachments/assets/3227cee5-82f4-47d8-9bfb-90581b7e78cc
  
## Why I Built This Project ?

I wanted to understand how search algorithms work in real-world problems. The Rubik's Cube is a classic state-space search problem, making it a great way to learn about graph traversal, heuristics, optimization techniques, data structures and algorithms with their implementation.

Through this project, I explored different cube representations and compared the performance of various solving algorithms.

## Features

- Multiple Rubik's Cube representations
  - 1D Array Representation
  - 3D Array Representation
  - Bitboard Representation

- Search Algorithms
  - DFS
  - BFS
  - IDDFS
  - IDA*

- Pattern Database Heuristic

- Generic Rubik's Cube Interface

- Scramble and Solve Functionality


## Project Structure

```text
RubiksCubeSolver/
│
├── Model
│   ├── RubiksCube1dArray.cpp
│   ├── RubiksCube3dArray.cpp
│   └── RubiksCubeBitboard.cpp
│
├── Solver
│   ├── BFSSolver.h
│   ├── DFSSolver.h
│   ├── IDDFSSolver.h
│   └── IDAstarSolver.h
│
├── PatternDatabases
│   └── CornerPatternDatabase.h
│
├── Databases
│   └── cornerDepth5V1.txt
│
└── main.cpp
```
## Cube Representations

### 1D Array

Stores all stickers in a single array.

Advantages:
- Simple implementation
- Easy indexing

### 3D Array

Represents the cube as a 3D structure.

Advantages:
- More intuitive mapping to a real cube
- Easier visualization


### Bitboard

Stores cube information using bit manipulation.

Advantages:
- Memory efficient
- Faster state operations


## Algorithms Implemented

### DFS (Depth First Search)

Explores states deeply before backtracking.

### BFS (Breadth First Search)

Explores states level by level and guarantees the shortest solution.

### IDDFS (Iterative Deepening DFS)

Combines DFS memory efficiency with BFS optimality.

### IDA* (Iterative Deepening A*)

Uses heuristic information to reduce the search space and solves the cube more efficiently.

## Pattern Database Heuristic

To improve the performance of IDA*, I implemented a Corner Pattern Database.

The pattern database stores precomputed distances for corner configurations and provides an admissible heuristic.

Benefits:
- Faster solving
- Reduced search space
- Better scalability

## What I Learned

This project helped me understand:

- State space search
- Graph traversal algorithms
- Heuristic search
- Pattern databases
- Bit manipulation
- Memory-performance tradeoffs
- Object-oriented design in C++
