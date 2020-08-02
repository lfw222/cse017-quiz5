# CSE 017 - Quiz 5

Due: 8/3 by end of day

Make one commit per question (at least).

## Question 1 

Consider the Depth First Search graph algorithm versus the Breadth First Search algorithm. They are very similar, except one uses a stack and the other uses a queue. How does the choice of datastructure in the affect the execution of the respective algorithms?

    - This choice matters because it affects the way nodes will be pushed and popped, and thereby the work and time the program will need to comlete to acceess a certain node. A stack is a LIFO type meaning that the last node added to the list will be the first node off, where as a queue is of the FIFO type meaning that the first node added will be the first node off. Because stacks and queues have different adding and removing structures it greatly affects the way each algorithm is executed.

## Question 2

What is the difference between a tree and a graph?

## Question 3

In the circular queue datastructure we have `front` and `back` variables. What is their purpose? Why do we design the queue this way?

## Question 4

Encode the following graph as an adjacency matrix

![Graph](https://github.com/cmontella/cse017-quiz5/blob/master/graph.png?raw=true)

## Question 5

For the graph in the previous question, write out the steps of Dijkstra's Algorithm to find the shortest path between Node 1 and Node 11. For each step, write down the Unvisited set U, the Visited set V, and the current tenative distance vector D.
