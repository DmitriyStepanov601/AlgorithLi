# Theoretical aspects
## Finding the shortest path in the maze
The wave tracing algorithm (wave algorithm, Lie algorithm) is a path—finding algorithm, an algorithm for finding the shortest path on a planar graph. Belongs to algorithms based on breadth-first search methods.

It is mainly used in computer tracing (wiring) of printed circuit boards, connecting conductors on the surface of microcircuits. Another application of the wave algorithm is the search for the shortest distance on the map in computer strategy games.

The shortest path is a path that includes the minimum number of edges and connects the initial and final vertices of the graph.

The shortest path can be determined by using the following algorithms:
- Wave algorithm;
- Dijkstra's algorithm;
- Floyd – Warshell algorithm;
- Ian's algorithm.

In order to make the choice of the algorithm, it is necessary to take into account the positive and negative sides of the algorithm, which will allow you to find the minimum path in a random maze.

## Classical algorithms for generating mazes
Currently, there are several classical algorithms that allow generating mazes, namely:
- binary tree algorithm
- the "Sidewinder" algorithm
- the Aldous-Broder algorithm
- Wilson's algorithm

First, let's consider the binary tree algorithm, the meaning of which is to stretch a path in a random direction from any cell.
The algorithm processes only 1 cell, which allows you to generate infinite mazes while preserving only the final version of the maze.

The following "Sidewinder" algorithm is similar to the previous one, but without diagonal displacement, the presence of an empty passage not individually, but in sets. Here the mazes are presented with a horizontal or vertical offset, as well as with a lack of dead ends.

The meaning of the Aldous-Broker algorithm is to find the vertex of the tree and attach another vertex and randomly check in the lab to find the attached vertex. There is no bias in this algorithm, which suggests that they are random and equally probable and are absolutely not similar to each other.

And finally, the last Wilson algorithm is difficult to implement, unlike previous algorithms. The purpose of the Wilson algorithm is the possibility of generating an equally probable random spanning tree.

### Comparison of the advantages of binary tree and "Sidewinder" algorithms
| Binary Tree algorithm | The "Sidewinder" algorithm | 
| :---      | :---     | 
| easy implementation of the algorithm  | generation of endless mazes     | 
| fast execution    | the presence of 1 empty passage       | 
| generation of endless mazes   | high complexity of the drawing       | 

### Comparison of the disadvantages of binary tree and "Sidewinder" algorithms
| Binary Tree algorithm | The "Sidewinder" algorithm | 
| :---      | :---     | 
| low complexity of the drawing  | complex algorithm implementation     | 
| powerful diagonal displacement    | lack of displaced dead ends       | 
| ack of displaced dead   | powerful vertical displacement       | 
| ends monotony of generated mazes   |        | 

### Comparison of the advantages of the Aldous-Broder and Wilson algorithms
| The Aldous-Broder algorithm | Wilson's algorithm | 
| :---      | :---     | 
| no offsets  | no offsets     | 
| random mazes    | random mazes       | 
| the complexity of the solution for people   | the complexity of the solution for people       | 
| simple implementation   | high speed operation       | 

### Comparison of the disadvantages of the Aldous-Broder and Wilson algorithms
| The Aldous-Broder algorithm | Wilson's algorithm | 
| :---      | :---     | 
| slow processing speed  | complex implementation of the algorithm     | 
| no generation of endless mazes    | reduction of generation speed       | 
| reduction of generation efficiency   | high memory requirements       | 

Summing up, I would like to highlight the following conclusions that all the presented algorithms clearly show the various possibilities of constructing mazes.
