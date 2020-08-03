# CSE 017 - Quiz 5

Due: 8/3 by end of day

Make one commit per question (at least).

## Question 1 

Consider the Depth First Search graph algorithm versus the Breadth First Search algorithm. They are very similar, except one uses a stack and the other uses a queue. How does the choice of datastructure in the affect the execution of the respective algorithms?

    - This choice matters because it affects the way nodes will be pushed and popped, and thereby the work and time the program will need to comlete to acceess a certain node. A stack is a LIFO type meaning that the last node added to the list will be the first node off, where as a queue is of the FIFO type meaning that the first node added will be the first node off. Because stacks and queues have different adding and removing structures it greatly affects the way each algorithm is executed.

## Question 2

What is the difference between a tree and a graph?

    - The difference between a tree anda graph is that a tree has a defined root, parent nodes, and children nodes, where as a graph do not neccessarily have this linear directionality. A graph's root can be any node and does not have to flow in the same linear manner as a tree. Where trees have defined parents and children nodes graphs do not, a node can point/connect with as many other nodes as desired. Lastly, a graph can be directed or undirected allowing for the connections between nodes to be defined as one on to another or undefined as in any movement or path through connections are possible.

## Question 3

In the circular queue datastructure we have `front` and `back` variables. What is their purpose? Why do we design the queue this way?

    - The front and the back variable of the queue are important because they maintain the length of list allowing for an error to be thrown is the list is only 1 element, preventing the list from being emptied in its entirety. Additionally it allows for us to not exceed the lists capacity. Essentially the front and the rear varibles allow us to keep track of the nuber of elements in the list and which elements were just added or are being removed.

## Question 4

Encode the following graph as an adjacency matrix

![Graph](https://github.com/cmontella/cse017-quiz5/blob/master/graph.png?raw=true)

    1   2   3   4    5   6   7   8   9   10   11
----------------------------------------------------   
1 | 0   0   0   13   0   0   2   0   0    0    0
2 | 1   0   0   0    0   0   0   0   0    0    0 
3 | 25  2   0   0    30  0   0   0   0    0    0
4 | 0   0   0   0    0   0   0   0   0    0    0
5 | 0   5   0   0    0   4   0   14  0    0    0
6 | 0   0   11  0    0   0   0   0   9    0    0
7 | 0   0   0   12   0   17  0   0   0    8    0
8 | 0   0   0   0    0   0   0   0   3    0    6
9 | 0   0   0   0    15  0   0   0   0    0    0
10| 0   0   0   0    0   0   0   0   8    0    0
11| 0   0   0   0    0   0   0   0   0    7    0 

## Question 5

For the graph in the previous question, write out the steps of Dijkstra's Algorithm to find the shortest path between Node 1 and Node 11. For each step, write down the Unvisited set U, the Visited set V, and the current tenative distance vector D.
// I == infinity, C == current
1:
U = {1,2,3,4,5,6,7,8,9,10,11}
D = [I,I,I,I,I,I,I,I,I,I,I]
V = {}
C = 1

2:

U = {2,3,4,5,6,7,8,9,10,11}
V = {1}
D = [0,I,I,13,I,I,2,I,I,I,I]
C = 7

3:

U = {2,3,4,5,6,8,9,10,11}
V = {1,7}
D=[0,I,I,13,I,19,2,I,I,10,I]
C = 10

4:

U = {2,3,4,5,6,8,9,11}
V = {1,7,10}
D=[0,I,I,13,I,19,2,I,18,10,I]
C  = 4

5:

U = {2,3,4,5,6,8,11}
V = {1,7,10,4}
D=[0,I,I,13,33,19,2,I,18,10,I]
C  =  9 

//4 dead ends back track

6:

U = {2,3,4,5,6,8,11}
V = {1,7,10,4,9}
D=[0,I,I,13,33,19,2,I,18,10,I]
C  =  6 

7:

U = {2,3,4,5,8,11}
V = {1,7,10,4,9,6}
D=[0,I,30,13,33,19,2,I,18,10,I]
C  =  3

8:

U = {2,4,5,8,11}
V = {1,7,10,4,9,6,3}
D=[0,32,30,13,33,19,2,I,18,10,I]
C  =  2






