## Description of the wave algorithm operation
The wave algorithm is an algorithm that allows you to find the minimum path in a graph. The breadth-first search algorithm is at the heart of this method. Basically, the wave algorithm is used to find the shortest path in the graph, in general, it finds only its length.
The purpose of the wave algorithm (like most other algorithms) is the task of laying or finding a path on the map between the starting and ending point (cell).
The description of the wave algorithm can be read in more detail at this link: http://orionxl.ru/volnovoj-algoritm.html

![Lee_algorithm](https://user-images.githubusercontent.com/61186198/162254905-3b3d6b8e-c6a0-41b5-baba-2f6588a74c96.png)

### Requirements for functional characteristics
For the interaction of the program and the user, the implementation of the following functions is necessary:
- reading data from an xml file
- maze generation (taking into account user input)
- search for the minimum path (using the wave algorithm)
- displaying the exit from the maze

Primary information: random maze with voids and obstacles.
Received information: displaying the minimum path in a random maze in console mode.

## Description of the program
In this project, the minimum route is selected by applying the Lie algorithm (wave algorithm). At the beginning of the work, the program outputs a table (regular grid) with the size read from the file, where 99 is the designation of an obstacle, and -1 is a free cell. Next, the algorithm suggests entering the coordinates of the start and end points (from 1 to 13 in x and y for this example). After the input, the program outputs a table to the console, in which zeros show the path from the start to the end point. And at the end, the coordinates of the points of the route connecting the beginning and the end.

![cursach](https://user-images.githubusercontent.com/61186198/162578079-ffad3a5e-0112-4f96-9aae-86ba3a5e6866.gif)

The found shortest path is marked with zeros.

![cursach2](https://user-images.githubusercontent.com/61186198/162578127-d780d515-af53-4069-a473-052547614450.gif)

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
