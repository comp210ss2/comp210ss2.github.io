---
layout: page
title: QZ05 topics
description: QZ05 topics
parent: Notes
# nav_exclude: true
---

# QZ05 topics

This quiz will be 25-30 minutes. It should be a bit shorter than the previous quizzes.

1. L14/15 - AVL
    - Everything is fair game
    - Be able to do AVL insert by hand, similar to the slides' examples and practice problem 1
        - Recognize whether there is imbalance
        - Recognize any of the 4 cases, LL, RR, LR, RL
        - Apply the fix
    - Be able to do AVL delete by hand, similar to practice problems 2 and 3
        - Same as above
        - NOTE: Use the **updated** slide 28 to recognize the case after remove
        - Must do R subtree method
    - May be a similar question to the final slide (possibly using the same diagram)
        - You should be able to identify a value that when inserted will not cause a rotation, cause a single rotation, or cause a double rotation
        - A value that when deleted will not cause a rotation, will cause a single rotation, or will cause a double rotation
    - Must be able to explain why AVL tree operations are worst-case $$O(\log n)$$ rather than $$O(n)$$ like BST
2. L16 - Hashing
    - All fair game
    - Be able to diagram inserting into hash table with chaining
        - Insert either at head or tail of list
        - Similar to example on slides
    - Be able to diagram inserting into hash table with probing (linear and quadratic)
        - Similar to two probing examples at the end of the slides
    - More chaining/probing [questions](https://www.cs.unc.edu/~stotts/410/exams/probsFhash.html) and [solutions](https://www.cs.unc.edu/~stotts/410/exams/probsFhash-ans.html) from Stotts' site
        - On a side note, since we're close to the final now, you should do some final exam practice problems from [here](https://www.cs.unc.edu/~stotts/COMP410-f20/examinfo.html)
    - Understand how to calculate load factor $$\lambda$$ for both chaining and hashing and what it means in both approaches
        - Note that for chaining, the numerator is the number of elements in the hash table (as with probing), not the number of lists
    - Know and be able to explain time complexities for `put` and `get` operations in hash table (chaining and probing)
    - Know good properties of hash functions
    - Understand how to perform `put`, `find`, and `remove` for chaining and probing
        - Trivial for chaining
        - Understand how to do `find` in probing
        - Understand why lazy deletion is required for `remove` in probing (e.g., what happens if you actually delete an element and then attempt to `find`/`put`)
3. Cumulative in that I won't explicitly test earlier topics, but I expect you to recall basic concepts. Specifically, for AVL tree insertion and removal, you have to understand BST insertion and removal
