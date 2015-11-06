## clojure.core.reducers/Cat



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1236"><img valign="middle" alt="[+] 0.0-1236" title="Added in 0.0-1236" src="https://img.shields.io/badge/+-0.0--1236-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__Cat.__ cnt left right)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/clojure/core/reducers.cljs#L182-L202):

```clj
(deftype Cat [cnt left right]
  cljs.core/ICounted
  (-count [_] cnt)

  cljs.core/ISeqable
  (-seq [_] (concat (seq left) (seq right)))
  
  cljs.core/IReduce
  (-reduce [this f1] (-reduce this f1 (f1)))
  (-reduce
    [_  f1 init]
    (-reduce
     right f1
     (-reduce left f1 init)))

  #_
  CollFold
  #_
  (coll-fold
    [this n combinef reducef]
    (-reduce this reducef)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1449
└── src
    └── cljs
        └── clojure
            └── core
                └── <ins>[reducers.cljs:182-202](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/clojure/core/reducers.cljs#L182-L202)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core.reducers/Cat` @ crossclj](http://crossclj.info/fun/clojure.core.reducers.cljs/Cat.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.core.reducers/Cat.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.core.reducers",
 :name "Cat",
 :type "type",
 :signature ["[cnt left right]"],
 :source {:code "(deftype Cat [cnt left right]\n  cljs.core/ICounted\n  (-count [_] cnt)\n\n  cljs.core/ISeqable\n  (-seq [_] (concat (seq left) (seq right)))\n  \n  cljs.core/IReduce\n  (-reduce [this f1] (-reduce this f1 (f1)))\n  (-reduce\n    [_  f1 init]\n    (-reduce\n     right f1\n     (-reduce left f1 init)))\n\n  #_\n  CollFold\n  #_\n  (coll-fold\n    [this n combinef reducef]\n    (-reduce this reducef)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1449",
          :filename "src/cljs/clojure/core/reducers.cljs",
          :lines [182 202]},
 :full-name "clojure.core.reducers/Cat",
 :full-name-encode "clojure.core.reducers/Cat",
 :history [["+" "0.0-1236"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.core.reducers/Cat"]))
```

-->