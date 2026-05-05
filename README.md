Service-Now-Project

This project is a Python implementation of two autonomous agents that navigate a graph network to collect coins from 
special nodes called slots. The agents compete by moving step by step through a network of connected nodes, 
trying to maximize their score before time runs out. SubmissionGhost is an explorer-first agent that spends the first 
third of its available steps building a complete map of the graph. As it explores, it tracks how far every node is 
from the starting point and records the location of any slots it discovers. Once it has explored enough of the graph, 
it identifies the slot that is farthest from the start and navigates there using BFS pathfinding. The strategy behind this 
is that farther slots are less likely to be contested by other agents. SubmissionBot is a greedy agent that does not bother 
mapping the entire graph. Instead it wanders toward high-numbered nodes while keeping track of the best slot it stumbles across. 
In the final 200 steps it stops exploring and rushes back to that best slot to farm as many coins as possible before time runs out. 
Both agents receive their current position, their neighbors, the current step number, the total steps available, and information 
about whether the current node has a slot. They also carry a persistent data object that stores their memory between steps. 
Each step they return the next node they want to move to, or negative one to stay in place.

Author
Nikita Shrivastav
