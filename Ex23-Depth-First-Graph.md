# Ex23 Depth First Graph

## DATE: 22.04.25

## Aim:

To compose the code for the function createNode to traverse the graph below in the depth first fashion.

![image](https://github.com/user-attachments/assets/63552824-d0a3-49c6-a473-6db27d1f03e4)

## Algorithm:

1. Use malloc to allocate memory for a new node of type struct node.

2. Set the vertex field of the new node to the value v.

3. Set the next pointer of the new node to NULL.

4. Return the pointer to the newly created node.

5. Complete the function execution.

## Program:
```
/*
Program to traverse the graph below in the depth first fashion
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013
*/
struct node* createNode(int v) {
  struct node* newNode = malloc(sizeof(struct node));
  newNode->vertex = v;
  newNode->next = NULL;
  return newNode;
}
```

## Output:

![438606086-5896c580-b2c3-4aeb-8a4c-57be4a0d2c8b](https://github.com/user-attachments/assets/1890d95d-a6cd-4012-b8fe-8c0da5eef029)


## Result:

Thus, the C code for the function createNode to traverse the graph below in the depth first fashion is implemented successfully.
