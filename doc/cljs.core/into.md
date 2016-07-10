---
name: cljs.core/into
related:
  - cljs.core/conj
---

## Signature
[to from]
[to xform from]


## Details

Returns a new collection consisting of `to` with all of the items of `from`
"added" using `conj`.

A transducer may be supplied as `xform`.