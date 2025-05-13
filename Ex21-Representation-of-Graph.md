# Ex21 Representation of Graph

## DATE: 22.04.25

## Aim:

To write a C program to display the adjacency matrix of the given graph by supplying the edges and the number of vertices.

## Algorithm:

1. Start the program.

2. Read the value of V (number of vertices).

3. Declare an adjacency matrix adjMatrix[V][V].

4. Initialize the matrix to 0 using the init function.

5. Calculate the maximum number of edges me as n * (n - 1) / 2.

6. For each edge, read e1 and e2, add the edge to the adjacency matrix, and stop if e1 == -1 && e2 == -1.

7. Print the adjacency matrix.

8. End the program.

## Program:
```
/*
Program to display the adjacency matrix of the given graph
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013  
*/
#include <stdio.h>

int V;

void init(int arr[][V]) {
    int i, j;
    for (i = 0; i < V; i++) {
        for (j = 0; j < V; j++) {
            arr[i][j] = 0;
        }
    }
}

void addEdge(int arr[][V], int e1, int e2) {
    arr[e1][e2] = 1;
    arr[e2][e1] = 1;
}

void printAdjMatrix(int arr[][V]) {
    int i, j;
    for (i = 0; i < V; i++) {
        for (j = 0; j < V; j++) {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }
}

int main() {
    int e1, e2, me, n, i;
    scanf("%d", &V);

    int adjMatrix[V][V];
    init(adjMatrix);

    n = V;
    me = n * (n - 1) / 2;

    for (i = 0; i < me; i++) {
        scanf("%d%d", &e1, &e2);
        if (e1 == -1 && e2 == -1) {
            break;
        }
        addEdge(adjMatrix, e1, e2);
    }

    printAdjMatrix(adjMatrix);

    return 0;
}
```

## Output:

![437700639-b2313ef0-0ec6-45fc-8ce6-adeecaf22504](https://github.com/user-attachments/assets/b9f33d55-48d4-495f-a300-f3acb805627b)

## Result:

Thus, the C program to print the adjacency matrix of the given graph is implemented successfully.
