---
layout: page
title: QZ01 topics
description: QZ01 topics
parent: Notes
# nav_exclude: true
---

# QZ01 topics

1. L3 - OOP
    - Classes/objects (`this`)
    - Encapsulation
    - Interface
    - Concrete implementations of interface
2. L4 - ADT
    - Interface
        - Visibility of methods when programming to an interface (i.e., the type is the name of the interface)
    - Axiomatic specification
        - Guttag's method (the steps for specifying an ADT, outlined in the slides)
        - Functional specification
        - Canonical / non-canonical operations
        - Given the axioms for a `MultiSet`, be able to apply the rules to a multiset given in axiomatic notation, and be able to write the result in axiomatic notation.
            - E.g., might be given `val ms = add(add(New, 1), 2)`. If I ask for the output of `rem(ms, 1)`, the correct answer is `add(New, 2)` (NOT `{2}`).
3. L5 - Big O
    - Everything on slides is fair game
    - Practice big O questions on [Prof. Stotts' COMP 210 website](https://www.cs.unc.edu/~stotts/COMP410-f20/)
        - Click on [exam info](https://www.cs.unc.edu/~stotts/COMP410-f20/examinfo.html)
        - Find what is relevant in our class so far and do that. May ignore the rest for now (or study it, may come up later)
    - Divide-and-conquer recursion big O not on this quiz, but recursion similar to Fibonacci, the quiz 0 `recur` question, recursive methods similar to those given in the 210 website above, etc., is fair game
4. L6 - List
   - Fair game, but less emphasis, and very likely (a) simple question(s).
5. "Cumulative" in that I won't explicitly quiz on topics from previous lectures, but I may expect you to recall basic concepts such as `public` and `private`.

## Multiset code

This SML code for a multiset will be on the quiz. Before the quiz, you may run this code on [SOSML](https://sosml.org/editor) to prep. However, you may not use SOSML (or any other SML interpreter) during the quiz. You should be able to hand-trace through simple code like the `rem` example above. You could practice tracing through some function calls on paper like we did in lecture, and you can check your work using the interpreter.

```sml
(*
MULTISET of E (collection of non-unique elements; the number of each element is tracked)

new :           --> MSET
add : MSET x E  --> MSET
rem : MSET X E  --> MSET
card: MSET      --> nat     (naturals, int >= 0) (card means cardinality)
mem : MSET X E  --> nat     (naturals, int >= 0) (mem means member, how many times is e in the mset?)
*)

datatype ('e) MSET = New
  | add of ('e) MSET * 'e;

fun rem(New, i) = New
  | rem(add(MS, i), j) = if i=j then MS else add(rem(MS, j), i);

fun card(New) = 0
  | card(add(MS, i)) = card(MS)+1;

fun mem(New, i) = 0
  | mem(add(MS, i), j) = if i=j then mem(MS, i)+1 else mem(MS, j);
```

Here are some test data points and test cases for the above code. You can simply paste this code below the axiom definitions.

Our testing is very simple: we create a bunch of multisets, call the functions on them, and check the outputs. For example, `card(ms1)=1;` is a true statement, so the interpreter prints `val it = true` for this line. All given test cases are correct, so you should see only `true` (no `false`).

```sml
(*---------------------------------------*)
(*   test data points                    *)
(*---------------------------------------*)

val ms = New;
val ms1 = add(ms, 1);   (* {1} *)
val ms2 = add(ms1, 2);  (* {1, 2} *)
val ms3 = add(ms2, 3);  (* {1, 2, 3} *)
val ms4 = add(ms3, 2);  (* {1, 2, 3, 2} *)
val ms5 = add(ms4, 3);  (* {1, 2, 3, 2, 3} *)
val ms6 = add(ms5, 2);  (* {1, 2, 3, 2, 3, 2} *)
val ms7 = rem(ms6, 2);  (* {1, 3, 2, 3, 2} *)
val ms8 = rem(ms7, 2);  (* {1, 3, 3, 2} *)
val ms9 = rem(ms8, 2);  (* {1, 3, 3} *)
val ms10 = add(ms9, 2); (* {1, 3, 3, 2} *)
val ms11 = rem(ms10, 3); (* {1, 3, 2} *)

(*---------------------------------------*)
(*   test cases                          *)
(*---------------------------------------*)

(*
Note: add and rem, used above, are tested implicitly in the card and mem tests.
*)

print("card tests");
card(ms)=0;
card(ms1)=1;
card(ms2)=2;
card(ms3)=3;
card(ms4)=4;
card(ms5)=5;
card(ms6)=6;
card(ms7)=5;
card(ms8)=4;
card(ms9)=3;
card(ms10)=4;
card(ms11)=3;

print("mem tests");
mem(ms, 1)=0;
mem(ms, 2)=0;
mem(ms, 3)=0;
mem(ms1, 1)=1;
mem(ms1, 2)=0;
mem(ms1, 3)=0;
mem(ms2, 1)=1;
mem(ms2, 2)=1;
mem(ms2, 3)=0;
mem(ms3, 1)=1;
mem(ms3, 2)=1;
mem(ms3, 3)=1;
mem(ms4, 1)=1;
mem(ms4, 2)=2;
mem(ms4, 3)=1;
mem(ms5, 1)=1;
mem(ms5, 2)=2;
mem(ms5, 3)=2;
mem(ms6, 1)=1;
mem(ms6, 2)=3;
mem(ms6, 3)=2;
mem(ms7, 1)=1;
mem(ms7, 2)=2;
mem(ms7, 3)=2;
mem(ms8, 1)=1;
mem(ms8, 2)=1;
mem(ms8, 3)=2;
mem(ms9, 1)=1;
mem(ms9, 2)=0;
mem(ms9, 3)=2;
mem(ms10, 1)=1;
mem(ms10, 2)=1;
mem(ms10, 3)=2;
mem(ms11, 1)=1;
mem(ms11, 2)=1;
mem(ms11, 3)=1;
(* Test mem called with non-existent element is 0 *)
mem(ms11, 0)=0;
mem(ms11, 4)=0; 
```
