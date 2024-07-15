---
layout: page
title: QZ04 topics
description: QZ04 topics
parent: Notes
# nav_exclude: true
---

# QZ04 topics

Note at the bottom a question that **will** show up and questions that **might** show up.

Be able to do all operations listed under heap operations and heapsort **by hand**. Know all time complexities (worst and average cases).

This quiz will be 30-35 minutes.

1. L11 - BST pt. 2, priority queue
    - BST content not covered by QZ03
        - BST time complexities
        - BST balanced condition (AVL)
        - BST sort and its time complexity
        - Using BST to implement `PrQueue` ADT
2. L12/13 - Heap
    - Everything is fair game, but specifically:
    - Heap invariants
        - Heap structure (complete)
        - Heap order
        - Subtrees are heaps
    - Parent/child index calculations, array representation of complete tree
    - Heap operations
        - `getMin`
        - `insert`
        - `delMin`
        - `increaseKey`/`decreaseKey`
    - Heapsort
        - Naive approach without efficient build algorithm
        - Faster approach using `buildMinHeap` (efficient build algorithm)
            - `minHeapify`
3. Cumulative in that earlier topics (besides recursion tree) won't be explicitly tested, but I expect you to be able to recall basic concepts
4. Question that will show up
    - In lecture, we saw that `minHeapify`'s worst-case running time can be expressed as $$T(n) \leq T\left(\frac{2n}{3}\right) + \Theta(1)$$. Show that its solution is $$O(\log n)$$ using a recursion tree.
5. Questions that might show up
    - In a perfect (all layers completely filled) binary tree with large height, roughly what proportion of the nodes are in the bottom 3 layers? We draw the binary tree from top-to-bottom, so the root is at the top. Write your answer as a fraction, e.g., $$\frac{1}{2}$$.
    - Given the following min-heap (no duplicate values) structure with values omitted (but assume that the heap is valid), which of the following nodes could have values that are
        - the smallest in the heap?
        - the second-smallest in the heap?
        - the third-smallest in the heap?
        - the largest in the heap?
    - Show your answers by shading the nodes in the diagrams below (one diagram per subquestion)

```text
      O
     / \
    /   \
   /     \
  O       O
 / \
O   O
```
