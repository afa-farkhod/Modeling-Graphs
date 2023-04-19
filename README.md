# Modeling-Graphs
Modeling Graphs, Graph interface, AbstractGraph, UnweightedGraph

The Graph interface defines the common operations for a graph. The Java Collections Framework serves as a good example for designing complex data structures. The common features of data structures are defined in the interfaces (e.g., Collection, Set, List, Queue), as shown in below Figure. Abstract classes (e.g., AbstractCollection, AbstractSet, AbstractList) partially implement the interfaces. Concrete classes (e.g., HashSet, LinkedHashSet, TreeSet, ArrayList, LinkedList, PriorityQueue) provide concrete implementations. This design pattern is useful for modeling graphs. I will define an interface named Graph that contains all the common operations of graphs and an abstract class named AbstractGraph that partially implements the Graph interface. Many concrete graphs can be added to the design. For example, we will define such graphs named UnweightedGraph and WeightedGraph. The relationships of these interfaces and classes are illustrated in the following Figure.

![image](https://user-images.githubusercontent.com/24220136/232947173-3b98f5c0-9eca-4252-901f-6e18c25d76fd.png)

First we implement Graph.interface. For convenience, we assume the graph is a simple graph, i.e., a vertex has no edge to itself and there are no parallel edges from vertex u to v. AbstractGraph implements all the methods from Graph, and it does not introduce any
new methods except a convenient addEdge(edge) method that adds an Edge object to the adjacency edge list. UnweightedGraph simply extends AbstractGraph with five constructors for creating the concrete Graph instances. Finally with the TestGraph.java we check the successful implementation in the following UML diagram:

![image](https://user-images.githubusercontent.com/24220136/232947459-1bd44e39-d65f-41ab-b5a3-11fa3baa53d1.png)

The program creates graph1 for the graph in lines 3–23. The vertices for graph1 are defined in lines 3–5. The edges for graph1 are defined in 8–21. The edges are represented using a two-dimensional array. For each row i in the array, edges[i][0] and edges[i][1]
indicate that there is an edge from vertex edges[i][0] to vertex edges[i][1]. For example, the first row, {0, 1}, represents the edge from vertex 0 (edges[0][0]) to vertex 1 (edges[0][1]). The row {0, 5} represents the edge from vertex 0 (edges[2][0]) to vertex 5 (edges[2][1]). The graph is created in line 23. Line 31 invokes the printEdges() method on graph1 to display all edges in graph1.
The program creates graph2 for the graph in lines 34–43. The edges for graph2 are defined in lines 37–40. graph2 is created using a list of Edge objects in line 43. Line 47 invokes the printEdges() method on graph2 to display all edges in graph2. Note that both graph1 and graph2 contain the vertices of strings. The vertices are associated with indices 0, 1, . . . , n-1. The index is the location of the vertex in vertices. For example, the index of vertex Miami is 9.

The AbstractGraph class defines the data field vertices (line 4) to store vertices and neighbors (line 5) to store edges in adjacency lists. neighbors.get(i) stores all edges adjacent to vertex i. Four overloaded constructors are defined in lines 9–42 to create a default graph, or a graph from arrays or lists of edges and vertices. The createAdjacencyLists(int[][] edges, int numberOfVertices) method creates adjacency lists from edges in an array (lines 45–50). The createAdjacencyLists(List<Edge> edges, int numberOfVertices)
method creates adjacency lists from edges in a list (lines 53–58). 
  
The getNeighbors(u) method (lines 81–87) returns a list of vertices adjacent to vertex u. The clear() method (lines 106–110) removes all vertices and edges from the graph. The addVertex(u) method (lines 112–122) adds a new vertex to vertices and returns true. It returns false if the vertex is already in the graph (line 120). 
  
The addEdge(e) method (lines 124–139) adds a new edge the adjacency edge list and returns true. It returns false if the edge is already in the graph. This method may throw IllegalArgumentExcepiton if the edge is invalid (lines 126–130).
  
The printEdges() method (lines 95–104) displays all vertices and edges adjacent to each vertex. 
  
The code in lines 164–293 gives the methods for finding a depth-first search tree and a breadth-first search tree, which will be introduced in Sections 28.7 and 28.9, respectively. 
 
Following is the Demo run of the TestGraph.java:
  
![image](https://user-images.githubusercontent.com/24220136/232948145-62b42f14-44c7-45c8-88ee-23cfcc67e18f.png)
  
