---
layout: page
title: L04 - Canonical operation applied to non-canonical operation
description: L04 - Canonical operation applied to non-canonical operation
parent: Notes
# nav_exclude: true
---

# Canonical operation applied to non-canonical operation

Note about today's question regarding a canonical operation applied to a non-canonical operation (i.e., when creating axioms, why do we figure out only what happens for any non-canonical applied to any canonical and not the other way around?).

For example, for a list, why do we not explicitly specify a rule for `ins` applied to `rem`?

`rem` is a non-canonical constructor, so any list constructed with `rem` can be rewritten without `rem` (i.e., just the canonicals `ins` and `new`). In fact, this is what the [code for rem](https://github.com/jesse-wei/lecture_code/blob/main/src/main/java/comp210/L04/ListSML.sml#L23) does. It recurses through a sequence of `ins` and removes one `ins`, leaving only `ins` and `New` (i.e., the `rem` is gone).

For example (and you can run this SML code on the online [SOSML editor](https://sosml.org/editor)),

```sml
datatype ('e) LIST = New
    | ins of ('e LIST) * 'e * int;

exception ERR;

fun rem(New, _) = raise ERR
    | rem(ins(L, e, i), j) = if i = j then L
                             else if j < i then ins(rem(L, j), e, i-1)
                             else ins(rem(L, j-1), e, i);

val l1 = ins(ins(New, 5, 0), 3, 0);  (* [3, 5] *)
val l2 = rem(l1, 0);  (* evaluates to ins(New, 5, 0) *)
                      (* i.e., rem is gone           *)
```

So we do not specify a rule for `ins` applied to `rem` because `rem` will actually remove itself. `ins` will never be applied to a `rem`.

Another simpler example might be `ins` applied to `size` (non-canonical examiner), e.g., `val l3 = ins(l2, 1, size(l2))`. But `size(l2)` returns `1`, so this is simply `ins(l2, 1, 1)`, which we already have a rule for (the definition of `ins`).

In sum, if we follow the procedure on the slides correctly, we won't end up in a situation where we have to specify behavior for when a canonical is applied to a non-canonical. This should be automatically handled by our other rules.
