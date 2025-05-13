# Ex22 Breadth First Graph

## DATE: 22.04.25

## Aim:

To write a printQueue C function of the given graph that is to be traversed in the breadth first manner.

![image](https://github.com/user-attachments/assets/f483f48c-6af0-4027-a993-01c108a50933)


## Algorithm:

1. Start the program.

2. Start from the front index of the queue.

3. If the queue is empty, print "Queue is empty".Otherwise, print "Queue contains" and display all items from front to rear.

4. Return after printing the queue contents.

5. End the program.

## Program:
```
/*
Program to traverse graph using BFS
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013 
*/
#include <stdio.h>
#include <stdlib.h>

#define SIZE 40

struct queue {
    int items[SIZE];
    int front;
    int rear;
};

struct queue* createQueue();
void enqueue(struct queue* q, int);
int dequeue(struct queue* q);
void display(struct queue* q);
int isEmpty(struct queue* q);
void printQueue(struct queue* q);

struct node {
    int vertex;
    struct node* next;
};

struct node* createNode(int);

struct Graph {
    int numVertices;
    struct node** adjLists;
    int* visited;
};

void printQueue(struct queue* q) {
    int i = q->front;
    if (isEmpty(q)) {
        printf("Queue is empty");
    } else {
        printf("Queue contains ");
        for (i = q->front; i <= q->rear; i++) {
            printf("%d", q->items[i]);
        }
    }
}
```

## Output:

![438605504-f4696907-cc6d-4511-b582-caee292ac39e](https://github.com/user-attachments/assets/b1e21b57-b8e8-4af3-a01f-e108a6ed1fc9)

## Result:

Thus, the code for the printQueue function of the following graph that is to be traversed in the breadth first manner is implemented successfully.
