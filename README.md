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
Binary Tree algorithm | The "Sidewinder" algorithm 
:---      | :---     
easy implementation of the algorithm  | generation of endless mazes     
fast execution    | the presence of 1 empty passage       
generation of endless mazes   | high complexity of the drawing       

### Comparison of the disadvantages of binary tree and "Sidewinder" algorithms
Binary Tree algorithm | The "Sidewinder" algorithm  
:---      | :---     | 
low complexity of the drawing  | complex algorithm implementation      
powerful diagonal displacement    | lack of displaced dead ends       
ack of displaced dead   | powerful vertical displacement       
ends monotony of generated mazes   |        

### Comparison of the advantages of the Aldous-Broder and Wilson algorithms
The Aldous-Broder algorithm | Wilson's algorithm 
:---      | :---     
no offsets  | no offsets     
random mazes    | random mazes       
the complexity of the solution for people   | the complexity of the solution for people       
simple implementation   | high speed operation       

### Comparison of the disadvantages of the Aldous-Broder and Wilson algorithms
The Aldous-Broder algorithm | Wilson's algorithm 
:---      | :---     
slow processing speed  | complex implementation of the algorithm     
no generation of endless mazes    | reduction of generation speed       
reduction of generation efficiency   | high memory requirements        

Summing up, I would like to highlight the following conclusions that all the presented algorithms clearly show the various possibilities of constructing mazes.

## Description of the wave algorithm operation
The wave algorithm is an algorithm that allows you to find the minimum path in a graph. The breadth-first search algorithm is at the heart of this method. Basically, the wave algorithm is used to find the shortest path in the graph, in general, it finds only its length.
The purpose of the wave algorithm (like most other algorithms) is the task of laying or finding a path on the map between the starting and ending point (cell).
The description of the wave algorithm can be read in more detail at this link: http://orionxl.ru/volnovoj-algoritm.html

### Requirements for functional characteristics
For the interaction of the program and the user, the implementation of the following functions is necessary:
- reading data from an xml file
- maze generation (taking into account user input)
- search for the minimum path (using the wave algorithm)
- displaying the exit from the maze

Primary information: random maze with voids and obstacles.
Received information: displaying the minimum path in a random maze in console mode.

# Practical implementation
## Description of the program
In this project, the minimum route is selected by applying the Lie algorithm (wave algorithm). At the beginning of the work, the program outputs a table (regular grid) with the size read from the file, where 99 is the designation of an obstacle, and -1 is a free cell. Next, the algorithm suggests entering the coordinates of the start and end points (from 1 to 13 in x and y for this example). After the input, the program outputs a table to the console, in which zeros show the path from the start to the end point. And at the end, the coordinates of the points of the route connecting the beginning and the end.

The main methods in the program:
- WaveAlg method – building a wave algorithm
- block method – filling the map with obstacles
- findPath method – implementation of the shortest path search
- WaveOut method – output of the coordinates of the path in the maze
- traceOut method – output of the maze in the form of a table

The shortest path search is implemented using the following data structures, namely: a list, a file and an array. A list is a set of elements of the same type, where the number of elements is greater than or equal to 0. In our program, this structure is used for the wave object. Basically, lists are implemented based on another structure - arrays, in our case – a two-dimensional array (matrix) that generates a maze, and also outputs a table that displays the shortest path from the start to the end point. In order to generate a maze, you need to get data from an xml file.

## Testing the program
During the development of the program "finding the shortest path in the maze", an error detection check was carried out, the program functions correctly, while no additional testing was carried out. Checking the operation of the program consisted in entering various source data and obtaining the corresponding results.

Initial data | Received data
:---      | :---     
1, 1, 13, 13  | 1 - 1, 2 -1, 3 - 1, 4 - 1, 5 -1, 6 - 1, 7 - 1, 8 - 1, 8 - 2, 8 - 3, 8 - 4, 8 - 5, 9 - 5, 10 - 5, 10 - 6, 11 - 6, 12 - 6, 13 - 6, 13 - 7, 13 - 8, 13 - 9, 13 - 10, 13 - 11, 13 -12, 13 – 13   
! and other symbols    | an error message about the entered values is displayed       
       
![gsh](https://user-images.githubusercontent.com/61186198/162037071-abe4dbfe-84a6-4fcd-9ef7-8a642733bb7a.png)

The results obtained show the effectiveness and quality of the developed program. But for more detailed testing, it is necessary to conduct several tests.
