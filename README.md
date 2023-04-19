# Modeling-Graphs
Modeling Graphs, Graph interface, AbstractGraph, UnweightedGraph

The Graph interface defines the common operations for a graph. The Java Collections Framework serves as a good example for designing complex data structures. The common features of data structures are defined in the interfaces (e.g., Collection, Set, List, Queue), as shown in below Figure. Abstract classes (e.g., AbstractCollection, AbstractSet, AbstractList) partially implement the interfaces. Concrete classes (e.g., HashSet, LinkedHashSet, TreeSet, ArrayList, LinkedList, PriorityQueue) provide concrete implementations. This design pattern is useful for modeling graphs. I will define an interface named Graph that contains all the common operations of graphs and an abstract class named AbstractGraph that partially implements the Graph interface. Many concrete graphs can be added to the design. For example, we will define such graphs named UnweightedGraph and WeightedGraph. The relationships of these interfaces and classes are illustrated in the following Figure.

![image](https://user-images.githubusercontent.com/24220136/232947173-3b98f5c0-9eca-4252-901f-6e18c25d76fd.png)

First we implement Graph.interface, then comes AbstractGraph.java then UnweightedGraph.java finally with the TestGraph.java we check the successful implementation in the following UML diagram:

![image](https://user-images.githubusercontent.com/24220136/232947459-1bd44e39-d65f-41ab-b5a3-11fa3baa53d1.png)


