# Heuristic Analysis
In this analysis the results of running different search stratigies on the 3 cargo problems are presented. The search is performed without heuristics. The metrics prvided are number of node expansions, number of goal test, teim elapsed, and optimality of solution.

## Problem 1
| Algorithm | Nodes | Goal Tests | Time | Optimality |
| ---       | ---   | ---        | ---  | ---:       |
| BFS graph | 43    | 56         | 0.03 | Yes         |
| BFS tree  | 1458  | 1459       | 0.9  | Yes        |
| DFS graph | 21    | 22         | 0.01 | No         |
| Depth limited | 101    | 271         | 0.08 | No         |
| Uniform Cost | 55    | 57         | 0.04 | Yes         |

