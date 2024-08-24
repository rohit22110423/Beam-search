This is Beam Search Algorithm.
Beam Search is a heuristic search algorithm that navigates a graph by systematically expanding the most promising nodes within a constrained set. This approach combines elements of breadth-first search to construct its search tree by generating all successors at each level. However, it only evaluates and expands a set number, W, of the best nodes at each level, based on their heuristic values. This selection process is repeated at each level of the tree.

Characteristics of Beam Search
Width of the Beam (W): This parameter defines the number of nodes considered at each level. The beam width W directly influences the number of nodes evaluated and hence the breadth of the search.
Branching Factor (B): If B is the branching factor, the algorithm evaluates 
W
×
B
W×B nodes at every depth but selects only W for further expansion.
Completeness and Optimality: The restrictive nature of beam search, due to a limited beam width, can compromise its ability to find the best solution as it may prune potentially optimal paths.
Memory Efficiency: The beam width bounds the memory required for the search, making beam search suitable for resource-constrained environments.
