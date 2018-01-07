# Research Review
In this report we explore three advancements in the field of planning highlighting the impact on the field of AI as a whole. We explore STRIPS; the first major planning system. Followed by Partial Order Planning, which dominated the research for 20 years. We finish by exploring Planning Graphs, which is orders of magnitude faster than partial order planning.
### STRIPS [1]
STRIPS (STanford Institute Problem Solver) was the first major planning system implemented in collaboration with SRI as the planning component for the Shakey robot project at SRI [2]. In STRIPS the world model is represented as by a set of first-order well-formed formulas. Operators(actions) are described with preconditions both positive and negative, and side effects as a set of add and delete lists [1]. The algorithmic approach for finding the plan was based on GPS (General Problem Solver).
The major influence of STRIPS to both planning, and AI generally was its representation language, which is close to "classical" language [2]. ADL (Action Description Language) then presented a more suitable representation for realistic problems, and PDDL (Planning Domain DEfinition Language) was introduced as a computer parsable syntax for describing planning problems.

### Partial Order Planning
Partial Order Planning was the dominant research approach for 20 years. Instead of constructing a plan at once like progression or regression search, partial order planning, also called non-linear planning specifies the all the actions needed to achieve a goal, but delays the action ordering till it is necessary following the principle of least commitment [3]. This gives the planner the advantage of the fact that many subproblems are independent [2]. The usual implementation of partial order planning is to maintain a queue of partial plans, then sort it via a ranking function [3].
The primary disadvantage  of partial order planning was its expensive computation cost. It fell out of favor in the late 1990s when faster methods were introduced [2].
### Planning Graphs
The problem with progressive search in planning is the exponential growth of the search space. Coming up with heuristics to guide the search can be domain dependent, and not genralizable. Simplifying the problem is a general approach to coming up with admissable heuristics, but can suffer from innacuracies.
Planning graphs can be used to give a better heuristic estimate by constructing an plynomial approximation to the search tree from inital state to goal. The graph cannot answer if the goal is reachable from initial state, but it can give an admissable estimate to the number of steps to reach the goal. GRAPHPLAN is an algorithm that uses planning graphs to effeciently find the action steps to reach the goal from initial state. GRAPHPLAN moved the field of planning forward, by raising the performance of planning systems, and the development of useful heuristics [2].

________
[1]: Fikes R. E., Nilsson N. J. STRIPS: A New Approach to the Application of Theorem Proving to
Problem Solving

[2]: Russel, Stewart, and Norvig. Artificial Intelligence: A Modern Approach 3rd Edition

[3]: Dyer, C. R. Partial Order Planning