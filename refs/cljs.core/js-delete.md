## cljs.core/js-delete



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__js-delete__ obj key)<br>
</samp>

---

Deletes property `key` in JavaScript object `obj`.

Equivalent to `delete obj[key]` in JavaScript.



---

###### Examples:

```clj
(def a #js {:foo 1 :bar 2})
(js-delete a "foo")

a
;;=> #js {:bar 2}
```



---

###### See Also:

[`cljs.core/dissoc`](../cljs.core/dissoc.md)<br>

---




Source code @ [github](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L929-L930):

```clj
(defn js-delete [obj key]
  (js* "delete ~{obj}[~{key}]"))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1449
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:929-930](https://github.com/clojure/clojurescript/blob/r1449/src/cljs/cljs/core.cljs#L929-L930)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/js-delete` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/js-delete.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/js-delete.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Deletes property `key` in JavaScript object `obj`.\n\nEquivalent to `delete obj[key]` in JavaScript.",
 :ns "cljs.core",
 :name "js-delete",
 :signature ["[obj key]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :related ["cljs.core/dissoc"],
 :full-name-encode "cljs.core/js-delete",
 :source {:code "(defn js-delete [obj key]\n  (js* \"delete ~{obj}[~{key}]\"))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1449",
          :filename "src/cljs/cljs/core.cljs",
          :lines [929 930]},
 :examples [{:id "5b24ea",
             :content "```clj\n(def a #js {:foo 1 :bar 2})\n(js-delete a \"foo\")\n\na\n;;=> #js {:bar 2}\n```"}],
 :full-name "cljs.core/js-delete"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/js-delete"]))
```

-->