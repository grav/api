## cljs.core/odd?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/odd?</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/odd?)
</td>
</tr>
</table>


 <samp>
(__odd?__ n)<br>
</samp>

---

Returns true if `n` is an odd number.

Throws an exception if `n` is not an integer.



---


###### See Also:

[`cljs.core/even?`](../cljs.core/evenQMARK.md)<br>

---


Source docstring:

```
Returns true if n is odd, throws an exception if n is not an integer
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L2179-L2181):

```clj
(defn ^boolean odd?
  [n] (not (even? n)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1449
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:2179-2181](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L2179-L2181)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/odd?` @ clojuredocs](http://clojuredocs.org/clojure.core/odd_q)<br>
[`clojure.core/odd?` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/odd%3F/)<br>
[`clojure.core/odd?` @ crossclj](http://crossclj.info/fun/clojure.core/odd%3F.html)<br>
[`cljs.core/odd?` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/odd%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/oddQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns true if `n` is an odd number.\n\nThrows an exception if `n` is not an integer.",
 :return-type boolean,
 :ns "cljs.core",
 :name "odd?",
 :signature ["[n]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/even?"],
 :full-name-encode "cljs.core/oddQMARK",
 :source {:code "(defn ^boolean odd?\n  [n] (not (even? n)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1449",
          :filename "src/cljs/cljs/core.cljs",
          :lines [2179 2181]},
 :full-name "cljs.core/odd?",
 :clj-symbol "clojure.core/odd?",
 :docstring "Returns true if n is odd, throws an exception if n is not an integer"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/odd?"]))
```

-->