---
layout: page
title: L04 - Non-canonical operation applied to canonical operation
description: L04 - Non-canonical operation applied to canonical operation
parent: Notes
# nav_exclude: true
---

# Non-canonical operation applied to canonical operation

Note about today's question regarding a canonical operation applied to a non-canonical operation (i.e., when creating axioms, why do we figure out only what happens for any non-canonical applied to any canonical and not the other way around?).

For example, for a list, why do we not explicitly specify a rule for `ins` applied to `rem`?

`rem` is non-canonical, so any sequence of statement using `rem` can be rewritten to one without `rem` (i.e., just the canonicals `ins` and `new`). In fact, this is what the [code for rem](https://github.com/jesse-wei/lecture_code/blob/main/src/main/java/comp210/L04/ListSML.sml#L23) does. It recurses through a sequence of `ins` and removes one `ins`, leaving only `ins` and `New` (i.e., the `rem` is gone).

For example (and you can run the code on [SOSML](https://sosml.org/editor)),

```sml
datatype ('e) LIST = New
    | ins of ('e LIST) * 'e * int;

exception ERR;

fun rem(New, _) = raise ERR
    | rem(ins(L, e, i), j) = if i = j then L
                             else if j < i then ins(rem(L, j), e, i-1)
                             else ins(rem(L, j-1), e, i);

val l1 = ins(ins(New, 3, 0), 5, 0);
val l2 = rem(l1, 0);  (* results in ins(New, 3, 0) *)
                      (* i.e., rem is gone         *)
```

So we do not specify a rule for `ins` applied to `rem` because `rem` will actually remove itself. `ins` will never be applied to a `rem`.

Another simpler example might be `ins` applied to a `find`, e.g., `val l3 = ins(l2, 1, find(l2, 3))`. But `find` returns `int`, so this is simply `ins(l2, 1, 0)`, which we already have a rule for (the definition of `LIST`/`ins`).

In sum, if we follow the procedure on the slides correctly, we won't end up in a situation where we have to specify a rule for when a canonical is applied to a non-canonical. This should be automatically handled by our other rules.
