# DAA-21110114


JUSTIFICATION


FOR THE GIVEN GRAPH WE HAVE RECIEVED THE CORRECT OUTPUT AS SHOWN IN THE RESULT PHOTO.

Prim's algorithm is designed to work on undirected graphs, not directed graphs. The main reason it cannot be used on directed graphs is that the edges in a directed graph have a specific direction, while the edges in an undirected graph do not.

In Prim's algorithm, it starts with an arbitrary vertex, and at each step it adds the next closest vertex that is not yet in the tree, along with the edge connecting them. This process is done by maintaining a priority queue of vertices and repeatedly selecting the vertex with the smallest key.

In a directed graph, the edges have a specific direction and weight, and the path between two vertices can have different weight in different direction. So, when Prim's algorithm is applied on directed graph, it will only consider the edges of the connected vertices, ignoring the direction and weight of edges. This makes the result of the algorithm not meaningful.

Additionally, in undirected graph the edges are bidirectional and they connect two vertices in both directions, while in directed graph the edges are unidirectional and they connect two vertices only in one direction.

Kruskal's algorithm is a minimum spanning tree algorithm that is typically used to find the minimum spanning tree (MST) of an undirected graph. It starts with an empty set of edges, and at each step adds the next smallest edge that connects two disjoint sets of vertices, until all vertices are connected.

Like Prim's algorithm, Kruskal's algorithm is designed to work on undirected graphs and cannot be used on directed graphs. The main reason is that the edges in a directed graph have a specific direction, while the edges in an undirected graph do not.

**Therefore, Prim's/kruskal's algorithm cannot be used in directed graphs, as it is not designed to work with the characteristics of directed graphs.but the given graph is treated as an undirected graph even though it is an directed graph due to its uni-directional path and due to its weight distribution.if there is any change in the direction of the graph .this algorithm may not work**

Dijkstra's algorithm is a shortest path algorithm that is typically used to find the shortest path from a source vertex to all other vertices in a non-negative weighted graph. It starts with the source vertex, and at each step relaxes the edges that connect the current vertex to its neighbors, by updating the distance estimates of the neighboring vertices if a shorter path is found.

Dijkstra's algorithm does not work in graphs with negative weight cycles because it relies on the assumption that the weight of edges in the graph are non-negative. In graphs with negative weight cycles, there are paths with negative total weight, which means that the distance estimate can decrease indefinitely if the algorithm continues running.

In a negatively weighted cycle the total weight of the cycle is negative, meaning that the algorithm will find a path with a decreasing distance estimate, which will lead to an infinite loop. Hence, Dijkstra's algorithm will not terminate and will not give any meaningful result.

**for this given question ,since the total weight of the cycle is positive (15) ,this cycle is treated as a non negative weighted graph and due to its uni directional path,djikstra's algorithm works for the given graph.if the graph is an negative weighted graph,this algorithms will not work.an alternative of djikstra's algorithm is bellman-ford algorithm which will work for negative weighted graph**
