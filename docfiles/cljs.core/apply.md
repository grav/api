---
name: cljs.core/apply
see also:
  - cljs.core/map
---

## Summary

## Details

Applies function `f` to the argument list formed by prepending intervening
arguments to `args`.

## Examples

```clj
(max 1 2 3)
;;=> 3

(apply max [1 2 3])
;;=> 3

(apply max 1 [2 3])
;;=> 3
```
