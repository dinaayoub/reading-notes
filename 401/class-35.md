# Read 35: Graphs

## Terminology

* Complete graph - all nodes are connected to all other nodes
* Connected graph - all nodes are connected to at least one other node
* Disconnected - some nodes aren't connected to other nodes.

--------

* Undirected Graph - all edges are undirected or bi-directional
* Directed Graph / DiGraph - each edge has a direction

--------

* Acyclic: directed graph without any cycles, i.e can't end up at a node twice while traversing.
* Cyclic: has cycles, where we can go over the same node multiple times.

--------

* sparse graph: Few connections
* dense graph: Many connections

--------

* Adjacency Matrix - a 2 D array with all of the nodes on both axes, and a 0 or 1 to represent whether those nodes have an edge with the other node, like 
<img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjMatrix.PNG"/>
* Adjacency List - Most common way to represent graphs - a collection of linked lists or array that lists all of the other vertices that are connected. This makes it easy to see if one node connects to another, like 
<img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjList.PNG">

--------

* Weighted graphs - graphs with numbers assigned to the edges. 
  * To represent this in adjacency matrix, instead of 0 or 1, it would be 0 or the weight.
  * To represent this in an adjacency list, the linked list must show both the node and the number.

## Traversal

* Breadth first - like trees but we need to add a 'visited' flag on each node so we don't get stuck in an infinite loop. Uses a queue.

```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    breadth.Enqueue(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                child.Visited <-- true
                breadth.Enqueue(child)   

    return nodes;
```

* Depth first - uses a stack so it's different from traversing a tree

The algorithm for a depth first traversal is as follows:

Push the root node into the stack
Start a while loop while the stack is not empty
Peek at the top node in the stack
If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
If the top node does not have any unvisited children, Pop that node off the stack
repeat until the stack is empty.

## Real world uses

* GPS and Mapping
* Driving Directions
* Social Networks
* Airline Traffic
* Netflix uses graphs for suggestions of products