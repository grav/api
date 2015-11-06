## clojure.walk/walk



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.walk/walk</samp>](http://clojure.github.io/clojure/branch-master/clojure.walk-api.html#clojure.walk/walk)
</td>
</tr>
</table>


 <samp>
(__walk__ inner outer form)<br>
</samp>

---





Source docstring:

```
Traverses form, an arbitrary data structure.  inner and outer are
functions.  Applies inner to each element of form, building up a
data structure of the same type, then applies outer to the result.
Recognizes all Clojure data structures. Consumes seqs as with doall.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/clojure/walk.cljs#L37-L48):

```clj
(defn walk
  [inner outer form]
  (cond
   (seq? form) (outer (doall (map inner form)))
   (coll? form) (outer (into (empty form) (map inner form)))
   :else (outer form)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1449
└── src
    └── cljs
        └── clojure
            └── <ins>[walk.cljs:37-48](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/clojure/walk.cljs#L37-L48)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.walk/walk` @ clojuredocs](http://clojuredocs.org/clojure.walk/walk)<br>
[`clojure.walk/walk` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.walk/walk/)<br>
[`clojure.walk/walk` @ crossclj](http://crossclj.info/fun/clojure.walk/walk.html)<br>
[`clojure.walk/walk` @ crossclj](http://crossclj.info/fun/clojure.walk.cljs/walk.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.walk/walk.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "clojure.walk",
 :name "walk",
 :signature ["[inner outer form]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "clojure.walk/walk",
 :source {:code "(defn walk\n  [inner outer form]\n  (cond\n   (seq? form) (outer (doall (map inner form)))\n   (coll? form) (outer (into (empty form) (map inner form)))\n   :else (outer form)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1449",
          :filename "src/cljs/clojure/walk.cljs",
          :lines [37 48]},
 :full-name "clojure.walk/walk",
 :clj-symbol "clojure.walk/walk",
 :docstring "Traverses form, an arbitrary data structure.  inner and outer are\nfunctions.  Applies inner to each element of form, building up a\ndata structure of the same type, then applies outer to the result.\nRecognizes all Clojure data structures. Consumes seqs as with doall."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.walk/walk"]))
```

-->