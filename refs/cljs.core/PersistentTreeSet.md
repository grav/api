## cljs.core/PersistentTreeSet



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/PersistentTreeSet</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/PersistentTreeSet.java)
</td>
</tr>
</table>


 <samp>
(__PersistentTreeSet.__ meta tree-map __hash)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L5650-L5716):

```clj
(deftype PersistentTreeSet [meta tree-map ^:mutable __hash]
  Object
  (toString [this]
    (pr-str this))

  IWithMeta
  (-with-meta [coll meta] (PersistentTreeSet. meta tree-map __hash))

  IMeta
  (-meta [coll] meta)

  ICollection
  (-conj [coll o]
    (PersistentTreeSet. meta (assoc tree-map o nil) nil))

  IEmptyableCollection
  (-empty [coll] (with-meta cljs.core.PersistentTreeSet/EMPTY meta))

  IEquiv
  (-equiv [coll other]
    (and
     (set? other)
     (== (count coll) (count other))
     (every? #(contains? coll %)
             other)))

  IHash
  (-hash [coll] (caching-hash coll hash-iset __hash))

  ISeqable
  (-seq [coll] (keys tree-map))

  ISorted
  (-sorted-seq [coll ascending?]
    (map key (-sorted-seq tree-map ascending?)))

  (-sorted-seq-from [coll k ascending?]
    (map key (-sorted-seq-from tree-map k ascending?)))

  (-entry-key [coll entry] entry)

  (-comparator [coll] (-comparator tree-map))

  IReversible
  (-rseq [coll]
    (map key (rseq tree-map)))

  ICounted
  (-count [coll] (count tree-map))

  ILookup
  (-lookup [coll v]
    (-lookup coll v nil))
  (-lookup [coll v not-found]
    (if (-contains-key? tree-map v)
      v
      not-found))

  ISet
  (-disjoin [coll v]
    (PersistentTreeSet. meta (dissoc tree-map v) nil))

  IFn
  (-invoke [coll k]
    (-lookup coll k))
  (-invoke [coll k not-found]
    (-lookup coll k not-found)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1449
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:5650-5716](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L5650-L5716)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/PersistentTreeSet` @ clojuredocs](http://clojuredocs.org/clojure.lang/PersistentTreeSet)<br>
[`clojure.lang/PersistentTreeSet` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/PersistentTreeSet/)<br>
[`clojure.lang/PersistentTreeSet` @ crossclj](http://crossclj.info/fun/clojure.lang/PersistentTreeSet.html)<br>
[`cljs.core/PersistentTreeSet` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/PersistentTreeSet.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/PersistentTreeSet.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "PersistentTreeSet",
 :signature ["[meta tree-map __hash]"],
 :history [["+" "0.0-1211"]],
 :type "type",
 :full-name-encode "cljs.core/PersistentTreeSet",
 :source {:code "(deftype PersistentTreeSet [meta tree-map ^:mutable __hash]\n  Object\n  (toString [this]\n    (pr-str this))\n\n  IWithMeta\n  (-with-meta [coll meta] (PersistentTreeSet. meta tree-map __hash))\n\n  IMeta\n  (-meta [coll] meta)\n\n  ICollection\n  (-conj [coll o]\n    (PersistentTreeSet. meta (assoc tree-map o nil) nil))\n\n  IEmptyableCollection\n  (-empty [coll] (with-meta cljs.core.PersistentTreeSet/EMPTY meta))\n\n  IEquiv\n  (-equiv [coll other]\n    (and\n     (set? other)\n     (== (count coll) (count other))\n     (every? #(contains? coll %)\n             other)))\n\n  IHash\n  (-hash [coll] (caching-hash coll hash-iset __hash))\n\n  ISeqable\n  (-seq [coll] (keys tree-map))\n\n  ISorted\n  (-sorted-seq [coll ascending?]\n    (map key (-sorted-seq tree-map ascending?)))\n\n  (-sorted-seq-from [coll k ascending?]\n    (map key (-sorted-seq-from tree-map k ascending?)))\n\n  (-entry-key [coll entry] entry)\n\n  (-comparator [coll] (-comparator tree-map))\n\n  IReversible\n  (-rseq [coll]\n    (map key (rseq tree-map)))\n\n  ICounted\n  (-count [coll] (count tree-map))\n\n  ILookup\n  (-lookup [coll v]\n    (-lookup coll v nil))\n  (-lookup [coll v not-found]\n    (if (-contains-key? tree-map v)\n      v\n      not-found))\n\n  ISet\n  (-disjoin [coll v]\n    (PersistentTreeSet. meta (dissoc tree-map v) nil))\n\n  IFn\n  (-invoke [coll k]\n    (-lookup coll k))\n  (-invoke [coll k not-found]\n    (-lookup coll k not-found)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1449",
          :filename "src/cljs/cljs/core.cljs",
          :lines [5650 5716]},
 :full-name "cljs.core/PersistentTreeSet",
 :clj-symbol "clojure.lang/PersistentTreeSet"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/PersistentTreeSet"]))
```

-->