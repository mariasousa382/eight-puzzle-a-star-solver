# 8-Puzzle A* Search Solver

This project implements an A* search solver for the 8-puzzle and generalized n×n sliding puzzle. It compares two admissible heuristics, misplaced tiles and Manhattan distance, and tracks the number of expanded nodes and maximum frontier size.

The project was created for CS152: Harnessing Artificial Intelligence Algorithms at Minerva University.

## Overview

The n-puzzle is a single-agent shortest-path search problem where the goal is to move numbered tiles into the target configuration by sliding the blank tile.

This implementation uses A* search, where each node is evaluated using:

```text
f(n) = g(n) + h(n)
```

where `g(n)` is the number of moves so far and `h(n)` is the estimated distance to the goal.

## Features

* A* search implementation
* Priority queue frontier using `heapq`
* Puzzle state representation with a `PuzzleNode` class
* Path reconstruction using parent pointers
* Misplaced tiles heuristic
* Manhattan distance heuristic
* Solvability checking using inversions
* Support for 3x3 and 4x4 puzzle tests
* Performance comparison between heuristics

## Technologies Used

* Python
* Jupyter Notebook
* Standard Python libraries

## Heuristics

### Misplaced Tiles

Counts how many tiles are not in their goal position, ignoring the blank tile.

### Manhattan Distance

Sums the horizontal and vertical distance of each tile from its goal position. This heuristic is more informative than misplaced tiles and usually expands fewer nodes.

## How to Run

Open the notebook:

```bash
jupyter notebook eight_puzzle_astar.ipynb
```

Then run all cells from top to bottom.

## Future Improvements

* Convert the notebook into a standalone Python script
* Add a command-line interface
* Add visualization of the solution path
* Implement a stronger heuristic
* Add memoization for faster heuristic evaluation
* Improve input validation for arbitrary board shapes
