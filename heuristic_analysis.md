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
| Greedy BFS | 7    | 9         | 0.005 | Yes         |
| A* h_1 | 55    | 57         | 0.04 | Yes         |
| A* Ignore Pre | 41    | 43         | 0.035 | Yes         |
| A* Level Sum | 11    | 13         | 0.6 | Yes         |

### Optimal Plan
_Length:_ 6
Load(C2, P2, JFK)
Load(C1, P1, SFO)
Fly(P2, JFK, SFO)
Unload(C2, P2, SFO)
Fly(P1, SFO, JFK)
Unload(C1, P1, JFK)

## Problem 2
| Algorithm | Nodes | Goal Tests | Time | Optimality |
| ---       | ---   | ---        | ---  | ---:       |
| BFS graph | 3343    | 4609         | 8.5 | Yes         |
| BFS tree  | N/A  | N/A       | N/A  | N/A        |
| DFS graph | 101    | 271         | 3.3 | No         |
| Depth limited | N/A  | N/A       | N/A  | N/A        |
| Uniform Cost | 4852    | 4854         | 12 | Yes         |

### Optimal Plan
_Length:_ 9
Load(C1, P1, SFO)
Load(C2, P2, JFK)
Load(C3, P3, ATL)
Fly(P2, JFK, SFO)
Unload(C2, P2, SFO)
Fly(P1, SFO, JFK)
Unload(C1, P1, JFK)
Fly(P3, ATL, SFO)
Unload(C3, P3, SFO)

## Problem 3
| Algorithm | Nodes | Goal Tests | Time | Optimality |
| ---       | ---   | ---        | ---  | ---:       |
| BFS graph | 14663    | 18098         | 42.2 | Yes         |
| BFS tree  | N/A  | N/A       | N/A  | N/A        |
| DFS graph | 408    | 409         | 1.7 | No         |
| Depth limited | N/A  | N/A       | N/A  | N/A        |
| Uniform Cost | 18235    | 18237         | 52 | Yes         |

### Optimal Plan
_Length:_ 12
Load(C1, P1, SFO)
Load(C2, P2, JFK)
Fly(P2, JFK, ORD)
Load(C4, P2, ORD)
Fly(P1, SFO, ATL)
Load(C3, P1, ATL)
Fly(P1, ATL, JFK)
Unload(C1, P1, JFK)
Unload(C3, P1, JFK)
Fly(P2, ORD, SFO)
Unload(C2, P2, SFO)
Unload(C4, P2, SFO)

