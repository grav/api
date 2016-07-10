---
name: cljs.core/memoize
---

## Signature
[f]


## Details

Returns a memoized version of a referentially transparent function.

A memoized version of a function keeps a cache of the mappings from arguments to
results in memory. When calls with the same arguments are repeated often, a
memoized function has higher performance at the expense of higher memory usage.