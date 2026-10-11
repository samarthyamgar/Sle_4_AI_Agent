# AI-Augmented Workflow – Maze Solving System

**Course:** 02AML204 – Introduction to Artificial Intelligence  
**Student:** Samarth Sanjay Yamgar  
**PRN:** 25UAM122  
**Division:** B.Tech CSE (AI & ML), Division B

## Project Overview

This project demonstrates the use of AI-assisted development, search algorithms, performance profiling, and software architecture design through a Maze Solving System.

The system solves a 6×6 grid maze by finding a path from the start position `(0, 0)` to the goal position `(5, 5)`.

- `0` represents an open path.
- `1` represents a wall.

The project explores Breadth-First Search (BFS) and Depth-First Search (DFS), compares their performance, and documents an architecture decision based on the results.

## SLE Journey

### SLE-1: AI-Augmented Workflow
- Developed a simple rule-based chatbot agent in Python.
- Used GitHub Copilot to assist with the chatbot structure and responses.
- Maintained a README and AI Contribution Log.

### SLE-2: Empirical Performance Analysis
- Implemented BFS and DFS for maze solving.
- Profiled both algorithms using Python's `time.perf_counter()`.
- Compared execution time, expanded nodes, and path length.

### SLE-3: C4 Architecture Model
- Designed the Context, Container, Component, and Code views of the Maze Solving System.
- Identified the search engine, BFS, DFS, visited set, goal test, and path reconstruction components.

### SLE-4: Final Viva and Architecture Decision Record
- Created an Architecture Decision Record (ADR).
- Documented why BFS is selected when the shortest path is required.
- Considered execution time, path length, memory usage, and alternative algorithms.

## Algorithms Used

**Breadth-First Search (BFS)**

BFS explores the maze level by level using a queue. For an unweighted maze where every move has the same cost, BFS guarantees a shortest path if one exists.

**Depth-First Search (DFS)**

DFS explores one path deeply before backtracking, using a stack or recursive traversal. It may find a path faster, but it does not guarantee the shortest path.

## Performance Comparison

The following results were collected during SLE-2 profiling:

| Metric | BFS | DFS |
|---|---:|---:|
| Path length (steps) | 10 | 16 |
| Nodes expanded | 21 | 17 |
| Average time – Run 1 | 0.021834 ms | 0.017401 ms |
| Average time – Run 2 | 0.020059 ms | 0.015957 ms |
| Average time – Run 3 | 0.019603 ms | 0.015723 ms |

Each timing measurement represents the average of 20,000 runs.

**Observation:** DFS was slightly faster in this test, but BFS found a path with 10 steps compared with DFS's 16 steps.

## Architecture Decision

**Decision:** Use BFS when the shortest path is required.

BFS is selected because finding the shortest path is more important than the tiny execution-time difference observed in this small maze. DFS remains available for comparison and profiling.

The decision is documented in the SLE-4 Architecture Decision Record.

## AI Tools Used

- **GitHub Copilot:** Assisted with SLE-1 chatbot development.
- **Claude:** Assisted with SLE-2, SLE-3, and SLE-4 work.
- **ChatGPT:** Assisted with understanding and explaining the SLE-3 C4 architecture model.

AI tools supported development and documentation. The student ran the code, collected performance results, reviewed the findings, and made the final architecture decision.

## Conclusion

This project demonstrates how search algorithms can be implemented and evaluated, how software architecture can be documented using the C4 model, and how measured results can support an Architecture Decision Record.

The main conclusion is that **BFS is the preferred algorithm when the shortest path is required in an unweighted maze**.

## Repository

GitHub: https://github.com/samarthyamgar/AI_Augmented_Workflow.git
