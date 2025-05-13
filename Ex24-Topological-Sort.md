# Ex24 Topological Sort

## DATE: 22.04.25

## Aim:

To compose the code to determine whether the topological ordering for the following graph is possible or not.

![image](https://github.com/user-attachments/assets/c74a7111-9b59-475c-aad4-9baf23d50ec0)

## Algorithm:

1. Start the program.

2. Create the graph using create_graph() function.

3. Calculate the indegree for each vertex. If the indegree is 0, insert the vertex into the queue.

4. Initialize count to 0 and begin processing vertices from the queue.

5. Dequeue a vertex, add it to the topo_order array, and remove all its outgoing edges.

6. For each adjacent vertex, decrease its indegree. If the indegree becomes 0, enqueue it.

7. If there is a cycle (i.e., not all vertices are processed), print an error message and exit.

8. Print the vertices in topological order.

9. End the program.

## Program:
```
/*
Program to determine whether the topological ordering for the following graph is possible or not
Developed by: Amruthavarshini Gopal 
RegisterNumber: 212223230013 
*/
//#include<stdio.h>
//#include<stdlib.h>
//#define MAX5
//int n; /*Number ofverticesinthegraph*/
//int adj[MAX][MAX];/*AdjacencyMatrix*/
//void create_graph();
//int queue[MAX], front =-1,rear =-1;
//void insert_queue(int v);
//int delete_queue();
//int isEmpty_queue();
//int indegree(int v); 
int main()
{
int i,v,count,topo_order[MAX],indeg[MAX]; 
create_graph();
/*Find the indegreeofeachvertex*/ 
for(i=0;i<n;i++)
{
indeg[i]=indegree(i); 
if( indeg[i] == 0 )
insert_queue(i);
}
count =0;
while( !isEmpty_queue()&&count <n)
{
v= delete_queue();
topo_order[++count]= v;/*Add vertex vto topo_order array*/
/*Delete alledgesgoing fromvertexv*/ 
for(i=0; i<n; i++)
{
if(adj[v][i]==1)
{
adj[v][i] = 0; 
indeg[i]=indeg[i]-1; 
if(indeg[i] == 0)
insert_queue(i);
}
}
}
if( count <n)
{
printf("No topologicalordering possible, graphcontains cycle\n"); 
exit(1);
}
printf("Verticesintopologicalorder are :\n"); 
for(i=1; i<=count; i++)
printf( "%d",topo_order[i]); 
printf("\n");
return0;
}/*Endofmain()*/
```

## Output:

![438606442-087b9072-74cc-44ad-95a0-4de7a19fada5](https://github.com/user-attachments/assets/40a3e4d0-6c75-4a02-b25c-7a34215a22b8)


## Result:

Thus, the C program for determining whether the topological ordering for the following graph is possible or not, is implemented successfully.
