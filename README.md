# 🧬 Simple Genetic Algorithm for the N-Queens Problem (N = 4)

This project was developed for the **Computational Artificial Intelligence** course.  
It implements a **Genetic Algorithm (GA)** in **C** to solve the **N-Queens problem**, demonstrating key evolutionary computing concepts.

---

## 🧠 Problem Overview

The **N-Queens problem** aims to place `N` queens on an `N×N` chessboard so that none attack each other — meaning no two queens share the same row, column, or diagonal.  
For `N = 4`, the optimal solution has **fitness = 6** (all queens safe).

---

## ⚙️ Genetic Algorithm Structure

- **Encoding:** Integer vector of size `N`, where each position represents a row and the value represents the column.  
  Example: `[1, 3, 0, 2]`
- **Fitness:** Number of non-attacking pairs of queens.
- **Selection:** Tournament of size `k`.
- **Crossover:** One-point crossover with probability `pc`.
- **Mutation:** Random column change per gene with probability `pm`.
- **Elitism:** Best individuals are preserved between generations.

---

## 🧩 Parameters

| Parameter | Symbol | Default |
|------------|----------|----------|
| Board size | N | 4 |
| Population size | P | 100 |
| Max generations | MAX_GEN | 1000 |
| Crossover rate | pc | 0.80 |
| Mutation rate | pm | 0.10 |
| Elites | E | 2 |
| Tournament size | k | 3 |

---

## 🚀 How to Run

### Compile:
```bash
gcc -Wall -O2 nqueens_ga_min.c -o nqueens
