---
layout: page
title: QZ02 topics
description: QZ02 topics
parent: Notes
# nav_exclude: true
---

# QZ02 topics

Note: Number of bullet points per topic does not necessarily indicate how much space that topic takes on the quiz. For example, since we already had a quiz on big O, I've written few points about big O here. But big O will be a significant part of the quiz.

There will be few definition questions because the quiz is open-note. There will be more short-answer "how", "why", and "what if" questions.

1. Big O
    - All big O concepts that you have learned are fair game (and same holds for all future quizzes)
    - Additionally, logarithmic time complexity (as seen in L8 - Sorting) is now fair game
    - Time complexity of divide-and-conquer algorithms such as quicksort and mergesort (or similar) also fair game
2. EX04 - LL pt. 1
    - Given code similar to what you've seen on EX04, describe what it does
    - Given a problem similar to (or same as) one on EX04, describe an approach for solving it
3. L6 - List
    - Everything on slides (including PEW) is fair game
    - Array, ArrayList, and LinkedList details and behaviors. Also, time complexities for operations on these data structures (worst-case and amortized)
        - Details such as inserting into array(list) at index that isn't `size-1` requires shifting the elements
        - Cannot simply memorize time complexities from the given table (or another that you find online). May ask you to explain a given operation's time complexity and/or the assumption(s) needed for that time complexity to hold. May also ask the time complexity of an operation but with a twist (e.g., instead of random index $$i$$, how about index `0` or `size-1`?)
    - Array - how does indexing work, and why is it $$\mathcal{O}(1)$$?
    - ArrayList - why doesn't it run out of space?
    - How do ArrayList and LinkedList look in memory (stack and heap)?
    - Stack and queue basic operations
    - Using stack to solve the balanced parentheses problem (e.g., `()` valid, `(())` valid, `(()` invalid, etc.)
4. L7 - LSQ pt. 2
    - Stack and queue implementation with array(list) and linked list
        - May be asked to give an implementation. If so, must describe details, such as whether you are using array or ArrayList, is the linked list singly or doubly linked, etc.
        - May be asked to choose the implementation that works better in a given scenario
    - Explain stack and queue operation time complexities given some implementation
    - Basics of deque and deque implementation
5. L8 - Sorting
    - Time complexities (worst, average, best) of bubblesort, insertion sort, mergesort, and quicksort
    - How do these sorting algorithms work?
        - May be asked to describe them at a high level
        - May be asked to give an example of an input or situation that would cause the worst-case time complexity (or best or average)
    - When to use a particular sorting algorithm
        - May be asked to choose the best sorting algorithm for a given scenario
        - Note: not necessarily just the one with the best time complexity
            - For example, insertion sort is $$\mathcal{O}(n^2)$$ but may be better than quicksort for small $$n$$
            - Big O notation hides the constants behind the terms
    - Stability, in-place
        - Understand the definitions
        - May be asked whether a given sorting algorithm is stable and/or in-place
    - Invariant
        - May be asked to describe invariant(s) of a sorting algorithm
    - Be able to understand and/or write a recurrence for a given algorithm
    - For simple recurrences such as the ones we've seen in class, you should be able to solve them (e.g., with a recurrence tree, as shown in L8)
6. L9 - Tree
    - Fair game, but less emphasis, and very likely (a) simple question(s)
7. Small amount of code writing in Java, but for a very simple problem (maybe one you've seen)
8. "Cumulative" in that I won't explicitly quiz on topics from previous lectures, but I may expect you to recall basic concepts
9. Useful basic math facts
    - The sum of the first $$n$$ natural numbers is $$\sum_{i=1}^n i = 1 + 2 + \ldots + n = \frac{n(n+1)}{2}=\Theta(n^2)$$
    - Exponent rules
        - \\(a^ba^c=a^{b+c}\\)
        - \\((a^b)^c=a^{bc}\\)
