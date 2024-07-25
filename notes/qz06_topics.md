---
layout: page
title: QZ06 topics
description: QZ06 topics
parent: Notes
# nav_exclude: true
---

# QZ06 topics

This quiz will be 35-40 minutes. Note that it is slightly cumulative. For example, trees are graphs, so you will need to remember some tree content. This quiz will contain some proofs (due to being more math-oriented content), but only easy ones that were covered in class.

Two proof questions that <span style="color: red">will be on the quiz</span> are written in <span style="color: red">red</span>. For one, it is recommended that you do a proof **by induction**. Two short answer questions that will also show up are written in <span style="color: green">green</span> below.

All other bolded text below should be interpreted as questions that might show up on the quiz.

L20's P and NP content from slide 33 and onward will not be on the quiz. On a side note, I had drawn P and NP as intersecting circles in class, but $$P \subseteq NP$$, so I added that on slide 35.

1. L17 - Graph concepts
    - Graph definition
        - Be able to draw the graph represented by a mathematical description ($$G = (V, E)$$, and $$V$$ and $$E$$ are given)
    - Adjacency
    - Path, path length
    - Cycle
    - DAG
        - **Given a graph, be able to identify whether it is or is not DAG**
    - Simple cycle detection algorithm
    - Connected (undirected), strongly and weakly connected (directed)
        - <span style="color: green">**Make an implication statement (i.e. $$p \implies q$$) using SC and WC**</span>
    - Complete graph
        - <span style="color: red">**Show that the number of edges in an undirected complete graph is $$\frac{v(v-1)}{2}$$ (can be done in a few words/symbols)**</span>
    - Planarity
        - **Given a graph or description of one, be able to identify whether it is planar or not**
        - If a graph is drawn and looks planar, then it is planar. If it does not look planar, it may still be planar (drawn differently).
    - Bipartite
        - **Given a graph or a description of one, be able to identify whether or not it is bipartite**
        - <span style="color: red">**Show that a tree (acyclic graph) is bipartite**</span> (may use induction)
            - This proof was done in class
            - Base case
                - 1 node, color it black, and it is bipartite
            - Inductive hypothesis
                - Every tree $$T$$ with $$n$$ nodes is bipartite
            - Inductive step
                - Show that $$T'$$ with $$n+1$$ nodes is bipartite
                - Consider $$T = T'$$, less a leaf node $$v$$. $$T$$ is a tree with $$N$$ nodes so by IH is bipartite.
                - Finish the rest of the proof. It will, of course, involve $$v$$.
2. L18 - Graphs
    - Adjacency matrix
        - Time complexity of operations and space complexity (similar to slide 12)
        - **Represent an undirected graph in a matrix containing 0's and 1's, what is a property of the matrix?**
    - Adjacency list
        - Time complexity of operations and space complexity (similar to slide 23, 24)
    - Sparse, dense
        - **Given a graph or description of one, identify whether it is sparse or dense**
    - Topological sort
        - **Properties of topo sort** (e.g., slide 28)
        - <span style="color: green">**Under what condition can two vertices in a DAG be in either order in a topological sort?**</span>
        - **Given a graph, be able to provide a topo sort if it exists, or assert that it does not exist**
        - **Given a graph and sequence of vertices, be able to identify whether the sequence is a topo sort**
        - Topo sort algorithm
            - Time complexity
            - How to implement it efficiently
        - Shortest path problem description
3. L19 - Graph algorithms
    - Unweighted shortest path
    - Traversals on graph
        - Depth-first
            - **Which data structure can we use to implement?**
        - Breadth-first
            - **Which data structure can we use to implement?**
        - **Given a graph, be able to state a depth-first and breadth-first traversal**
        - **Given a graph and sequence of vertices, be able to identify whether the sequence is a depth-first or breadth-first traversal**
    - Dijkstra's algorithm
        - **Be able to do it by hand**
        - **Be able to describe why we need the `known` and `prev` fields**
    - (M)ST
        - Know properties of spanning tree and minimum spanning tree (e.g., slides 17, 19, 22, 23)
            - E.g., unique edge weights $$\implies$$ unique MST
        - **Be able to do Kruskal's algorithm and Prim's algorithm by hand**
        - **Know the difference between how we efficiently reject cycles in Kruskal's algorithm and in Prim's algorithm**
            - Kruskal's: disjoint set (L20)
            - Prim's: for edge candidate $$(u, v)$$, simply check that $$v$$ is not in the MST so far
                - `HashSet`/`HashMap` `contains` method
                - Or if the vertices are numbered 0 to n-1, can use a boolean array of size n
        - **Know how Kruskal's algorithm selects edges in sorted order by increasing weight**
        - Greedy algorithm
4. L20 - Finish MST, Euler, Hamiltonian
    - EP/EC
        - Theorems 1, 2, 3
        - **Given a graph, be able to identify whether it has an Euler path and/or circuit**
        - Be able to identify whether a sequence of vertices is an EP/EC
        - If a graph has 2 odd vertices, know that those are the start/end vertices
        - Know that EP/EC can be found in $$O(\\|V\\|+\\|E\\|)$$ time (which we call linear for graphs)
    - HP/HC
        - Be able to identify whether a sequence of vertices is an HP/HC
        - **Apply theorems 1, 2, 3 to determine whether a statement about a possible HP/HC in a graph could be true or must be false**
        - Know that the best known algorithms to find HP/HC take exponential time

## Useful math facts

* $$\sum_{i=1}^n i = 1 + 2 + \ldots + n = \frac{n(n+1)}{2}$$
* $$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$
* For $$k=2$$, we have $$\binom{n}{2} = \frac{n!}{2!(n-2)!} = \frac{n(n-1)}{2}$$
