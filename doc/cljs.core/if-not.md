---
name: cljs.core/if-not
related:
  - special/if
  - cljs.core/when-not
---

## Signature
[test then]
[test then else]


## Details

If `test` is false or nil, evaluates and returns `then`. Otherwise, evaluates
and returns `else`. `else` defaults to nil if not provided.