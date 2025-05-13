# Ex25 Adjacency List Representation

## DATE: 22.04.25

## Aim:

To write a C program to represent the given graph using the adjacency list.

## Algorithm:

1. Read the number of vertices and number of edges.

2. Read all edge pairs (source and destination) and store them.

3. Create a graph using the input edge list.

4. Print the adjacency list representation of the graph.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013 
*/
int main(void)
{ int n,i;
 scanf("%d",&N);
 scanf("%d",&n);
 // input array containing edges of the graph (as per the above diagram)
 // (x, y) pair in the array represents an edge from x to y
 struct Edge edges[n];
 for (i = 0; i < n; i++)
 {
 // get the source and destination vertex
 scanf("%d",&edges[i].src);
 scanf("%d",&edges[i].dest);
 
 }
 
 // construct a graph from the given edges
 struct Graph *graph = createGraph(edges, n);
 // Function to print adjacency list representation of a graph
 printGraph(graph);
 return 0;
}
```

## Output:

![438606858-1cf60013-4b24-454e-a674-56704e72d3ac](https://github.com/user-attachments/assets/e59895cd-ce13-476e-9b57-7431ebcc1b50)


## Result:

Thus, the C program to represent the given graph using the adjacency list is implemented successfully.
